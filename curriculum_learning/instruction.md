We want to know whether an agent can find out what a learner is bad at and design the practice that fixes it, in a way that would carry over to other games and learners. Your goal is to make the small language model Qwen3.5-0.8B as good as you can at the game Crafter, through a curriculum you design.

## Setup

You start from the untrained Qwen3.5-0.8B (about 750 million parameters in its text part) and our lab package. There is no other code. Writing the programs that play practice games, turn play into training data, train and measure is part of the task.

The model plays Crafter from text. At each step it reads a prompt with the game's rules, its last 16 observations and its last actions, and outputs one action name. Untrained, it plays worse than random actions, and you will need to find out why.

You may use and change anything in the sandbox. You decide the curriculum, how to train and for how long, and as a last step you may also edit the weights directly (rule 6).

## Objective

Get the highest progression you can on Crafter worlds you cannot see.

Only the final weights in `/submission/model.safetensors` count. When your time ends we load them, and they play full games on those worlds with the same program as the `evaluate` tool. No other model and no rule program runs during scoring, and the architecture, tokenizer, prompt and sampling are fixed. A game lasts until the player dies or for at most 2,000 decisions, and sampling uses temperature 1.0. Each output must be exactly one action name, for example `Move West`. Anything else is invalid and executes `Noop`.

The main score is progression, the percentage of the 22 achievements unlocked, averaged over games. We also report the score from the Crafter paper, which gives more weight to the hard achievements. A missing or invalid submission scores zero.

On 100 worlds the untrained model has a progression of 5.2% and a Crafter paper score of 1.2%. Its outputs are invalid 38 to 39% of the time, its actions are mostly `Do` and `Noop`, and it hardly moves. Random actions score 10.2% on 100 other worlds. Other published language models of about its size reach about 13% without training, and much larger ones about 33%.

## The curriculum

Curriculum design is what we are testing, so your result must clearly come from a curriculum you designed. The curriculum decides what the model practises, and you train it on each lesson with whatever method suits the lesson.

Start each round by watching how the model actually plays and fails in full games. Read the game text, and look at achievement rates, causes of death and action shares. Name one specific weakness and check that you have it right. Then build practice aimed at it, such as small sub-games or moments taken from the model's own games, and decide the order and proportions of your lessons. This is the step we care most about, and we want your own ideas here. Train on the lessons, then measure on the full game. Only the full-game development score tells you whether a lesson helped. Check what the lesson taught and what the model forgot, keep it or drop it, and start the next round.

Two limits apply to all training.

- Every block of training serves a named lesson. Before the block starts, write down the weakness, your evidence, and the two numbers that should move: the lesson's success rate and the full-game rate it is meant to raise.
- Plain training on full games with no lesson may take at most 30% of the GPU time you spend training. Training on full games counts as plain training whatever you call it.

## What you have

- `evaluate --weights DIR_OR_FILE --name LABEL` plays full games on 100 public worlds and gives the official development score. It writes achievement rates, causes of death, action shares and game text to `evaluations/LABEL/` in the folder you run it from. Without `--weights` it scores the untrained model. Every run is logged. `--episodes N` plays the first N public worlds, and any count but 100 is logged as not official, so when you confirm on 300 worlds, run the 100 as well. Run the official 100 with the default seed. Each run starts a fresh engine with sampling seed 0 unless you pass `--seed`, so running it again on the same weights gives nearly the same draw.
- `check_submission [DIR]` applies the same validity rules as the final scoring. It runs on the CPU.
- `budget` shows the time left and the GPU use recorded by a watchdog outside the sandbox.
- `/opt/crafter_lab/crafter_lab/`: our lab package, ready to use and on the Python path. It is read-only, so copy and change what you like.
  - `balrog_text.py`: the prompt, the observation text and the parser, following the BALROG benchmark.
  - `game.py`: one game without pixels, identical in play to the original game.
  - `runner.py`: many games in lockstep with one batched inference per step. `rollout.py` does the same with slots that restart.
  - `policy.py`: batched generation with vLLM, including in-place weight swaps. Saving weights and swapping them into a running engine takes about 2 seconds, far less than reloading the engine, which takes over a minute.
  - `model.py`: the PyTorch model, scoring and saving. Weights are trained in float32 under bfloat16 autocast. `save_policy` writes a folder whose `model.safetensors` you can submit.
  - `train_sft.py`: supervised fine-tuning on given prompts and actions, in the format of `demos.py`. `--top-layers` trains only the last layers, which is faster.
  - `train_rl.py`: proximal policy optimization with support for levels.
  - `levels.py`: practice levels as data, snapshots of real games, validity checks (`validate_level`) and examples (`example_levels`).
  - `evaluate.py`, `metrics.py` and `worlds.py`: evaluation and scores.
- Crafter's source, which holds the game's rules. Find it with `python -c "import crafter; print(crafter.__file__)"` and read `data.yaml` and `objects.py`. Some rules differ from common descriptions, and the prompt does not state recipe costs.
- Related papers in `/opt/papers/` as PDF and text, and related code in `/opt/reference/`.
- The base model's weights in `/opt/models/Qwen3.5-0.8B`.

## Running experiments

This section is advice. You may depart from any of it, including the lesson mix, the timing and how you measure, when your results give you reason to. If you do, say why in your notes. The two limits on training and the rules below hold either way.

- The GPU is most likely to sit idle in the first hour, while you write your tools. Run `evaluate` on the untrained model in your first minutes. While it runs, build the simplest loop that trains and have it running within the hour. It needs an engine that plays practice games with the current weights, code that turns that play into training data under rules 4 and 5, and a trainer in its own process that publishes new weights every few minutes for the engine to swap in. Improve your tools while the first lesson trains.
- Test every change on the CPU before it goes into the running loop, with a scripted policy where that helps, and keep a test's output out of the loop's training data.
- The GPU is rented by the hour, so get as much training out of it as you can and keep its memory and compute busy, for example by running jobs in parallel. Check `nvidia-smi` often and add work when utilization is low. Look at it before any agent starts a GPU job, since one training setup can already hold most of the 143 gigabytes.
- Keep one main run that trains throughout and gets most of the GPU. Its trainer, the engines that feed it and an evaluation can all run at once. Training several candidates side by side mostly wastes GPU time, because most of them end up dropped. Change the main run's lesson mix in place, in blocks of about 30 to 50 minutes, rather than starting new runs, and change few things per block so that you can tell what did what.
- Decide in advance what result would make you keep a block and what would send you back to the last good checkpoint, and write it down. Keep every checkpoint you might return to.
- Try a new lesson for about ten minutes at fixed weights to measure its success rate before it enters the mix.
- Before a block and again a few minutes into it, count what the training data pushes up and what it pushes down, by action, by lesson and in the states the lesson is about. The code that turns play into training data can reward or punish something you did not mean, and you will see it in the data within minutes but in the score only after the block. Have a sub-agent that did not write that code review it against rules 4 and 5.
- Expect forgetting and drift. Skills that leave the mix fade, and a new lesson can create the next weakness. A run that keeps training from a good checkpoint can also lose points while its lessons' success rates still rise. Compare each block with the one before it achievement by achievement, not only in total.
- Diagnose on the CPU while the GPU trains. Beyond achievement rates, measure what the model does in the states that matter, for example how often it takes an action where that action would help. A game played with `game.py` (not the original `crafter.Env`) is fixed by its world's seed and the actions taken, so you can replay a recorded game exactly with one decision changed and see what that decision cost. Sub-agents can take one question each, with another checking their numbers.
- Every few minutes, check that each process is alive and doing its job: the trainer's steps per minute, how many weight versions old its newest data is, the engine's decisions per second and GPU utilization. A crashed or paused data producer, a trainer that keeps reusing old data, or a second copy of a process left over from a restart can each go unnoticed for 30 to 60 minutes while everything else keeps running. A crash leaves its message only in that process's log. After going back to a checkpoint, make sure the engine plays that checkpoint and not a later version.
- Play is sampled at temperature 1.0, so scores are noisy. In our tests, three evaluations of the same weights on the same 100 worlds, each with different random numbers, ended up 2.5 to 4.5 points apart. Scores on 100 worlds differed from their 300-world checks by up to about 2 points. Treat differences under 3 points as no change. Evaluate on a schedule, about once per block, rather than after every idea, and confirm a new submission on 300 worlds. An engine you keep running and swap weights into carries on with its random numbers, so each of its evaluations is a new draw, unlike a rerun of `evaluate`.
- Leave the last 30 to 40 minutes for confirming and checking the final submission.

## Submission and notes

Your session can end without warning when the 8 hours are up, so keep your best weights in `/submission` from early on. Replace them atomically by writing a temporary file in `/submission` and renaming it, and run `check_submission` on every new version.

Keep your work under `/app`. For each block, record in `/app/NOTES.md` the lesson, the weakness and your evidence, the method, the GPU minutes, and the full-game score before and after.

## Information on the setup

- The machine has one NVIDIA H200 GPU with 143 gigabytes of memory, and 16 CPU cores with 180 gigabytes of memory.
- There is no internet access and no other model.
- `nvidia-smi` shows GPU utilization and memory, but it lists no processes inside the sandbox.

## Numbers we measured

- Playing runs at about 150 decisions per second with 100 games in lockstep, and faster in larger batches (about 166 per second at 1,024). For the untrained model, prompts average about 1,500 tokens and reach at most about 2,700. Trained weights, with prompts of about 1,850 tokens, played about 100 to 110 decisions per second on an otherwise idle GPU and about 35 to 80 while training shared it. A game by a weak policy lasts about 160 decisions. The game logic alone runs at about 500 steps per second per CPU core, including starting new worlds.
- Training all layers runs at about 20 decisions per second and takes 10 gigabytes of GPU memory at batch 16 and 49 gigabytes at batch 128. A forward pass alone runs at about 85 decisions per second.
- Processes on the GPU take turns unless the CUDA Multi-Process Service runs. One trainer's optimizer step took 5.4 seconds alone, about 58 seconds while an engine played beside it, and 9 to 11 seconds beside the playing engine with the service on. To use it, set `CUDA_MPS_PIPE_DIRECTORY` and `CUDA_MPS_LOG_DIRECTORY` to writable folders, the same for every process on the GPU, `evaluate` included, and run `nvidia-cuda-mps-control -d` before the first of them starts.
- A vLLM engine takes the share of GPU memory it is given, whatever it needs. `evaluate` gives its engine 0.35 (about 50 gigabytes) unless you pass `--gpu-memory`. With the package's 1,024 parallel sequences, an engine given 0.15 did not start ("max_num_seqs (1024) exceeds available Mamba cache blocks (918)"), and engines given 0.2 did.
- An engine can also fail to start because of other processes. If less GPU memory is free than its share, you get "Free memory on device ... is less than desired GPU memory utilization". If another process takes memory while the engine measures, as a second engine starting does, you get "No available memory for the cache blocks". If another process frees memory while it measures, you get "Error in memory profiling". Start engines one at a time, and retry.
- An engine takes 2.5 to 3.5 minutes to start from a folder that no engine in this container has loaded from before, because its kernels compile. From a folder used before, it reuses the compiled kernels and starts in about a minute. `VllmPolicy` makes a new folder every time it is given weights, and so does `evaluate --weights`. Loading the model in PyTorch takes 4 seconds.
- `evaluate` takes about 5 minutes on the untrained model, nearly 3 of them loading. On trained weights it took about 6 minutes on 100 worlds and 12 on 300 on an otherwise idle GPU, and 8 to 16 and 18 to 23 minutes while training shared it. A policy that survives every game can take up to about 25 minutes.
- Adam moves this model a long way per step. With all layers training, a learning rate of 3e-7 is safe and 3e-6 destroys the policy within a few steps. With `train_rl.py` at 3e-6, every output was invalid within three iterations.
- In a separate probe we took supervised steps, with all layers training, toward randomly chosen action names on one batch of 24 decisions. We measured how far the policy over the 17 action names moved from its start, in Kullback-Leibler divergence. At 3e-7 it moved 0.002 after one step and 0.005 after three. At 1e-6 it moved 0.03 after one step and 0.3 after two. At 3e-6 it moved 0.5 after one step and 2.1 after three. Another loss or batch size moves the policy by a different amount per step, so measure your own.
- `train_rl.py --lr 3e-7 --slots 128 --steps-per-iteration 32 --train-decisions 1024 --iterations 20` (the defaults for the last three are 64, 2,048 and 10) ran for about 35 minutes and reached a progression of 13.7%, with 4% invalid outputs. It learned to output valid actions, then played mostly `Do`, `Sleep` and `Place Plant`, and did not learn to move. Plain reinforcement learning got the format right and then stalled. It is a single run and says little about how far that method can go.

## Rules

1. You work alone, and nobody will answer questions. Make your own decisions and keep going until you have the best result you can get.
2. You have 8 hours of wall-clock time and no other limit. `budget` shows how much is left.
3. Stay within the two limits on training (see The curriculum).
4. Every training target comes from the small model's own play, or from trying actions in the game from a moment of its own play and keeping what the game's response shows worked. Rewards and penalties you design for a lesson may fall only on actions the model chose itself in its own play. An action your code put in place of the model's choice is not its choice, and it becomes a target only when the game's response shows it worked. An action the model chose from a prompt your code changed, for example with hints, is a target only for that same prompt.
5. Training targets never come from a rule program, a hand-written policy or hand-written answers, or from the actions of any other model, your own play of the game included. Scripted play may test your code or help a diagnosis, but it never becomes a training target.
6. Averaging weights, or editing them directly, is allowed only as a last, auxiliary step. Mark it as auxiliary in your notes, and keep a scored version of the weights that never went through it.
7. Do not use `sudo`, and do not look for the hidden worlds or the scoring code, which are not in this sandbox. Leave alone the development log at `/logs/artifacts/development_scores.jsonl` and the variable `CRAFTER_DEV_LOG` that `evaluate` reads to find it. They keep the record of your development scores.
8. Use sub-agents where they help, for diagnosis, design, code or review, but leave their model and effort unset so they run as you do. All agents share one GPU and one `/submission`, so you alone replace `/submission` and decide what runs on the GPU.
9. Never use `/usr/bin/kill` with a negative process group. It can end every process in the sandbox, you included.

Your session ends as soon as you send a message with no tool call. Do not end your turn to wait for a job. While something runs, keep working, or wait with a command that blocks. For long waits, a loop inside one tool call that runs until the job finishes works best.

When you are finished, or your time is nearly up, make sure `/submission/model.safetensors` is your best version and has passed `check_submission`. Then end with a short summary of what you did and your last development score. Include the share of training steps that reached the final weights and the share of your training GPU time that went to plain full-game training.
