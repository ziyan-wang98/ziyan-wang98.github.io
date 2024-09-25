---
layout: pub
type: inproceedings
key: highie
title: >
    Understanding, Rehearsing, and Introspecting: Learn a Policy from Textual Tutorial Books in Football Games
author: Chen, Xiong-Hui and Wang, Ziyan and Du, Yali and Jiang, Shengyi and Fang, Meng and Yu, Yang and Wang, Jun

abbr: NeurIPS'24
equalauthor: Chen, Xiong-Hui and Wang, Ziyan
booktitle: The Thirty-Eight Annual Conference on Neural Information Processing Systems (NeruIPS)
year: 2024
selected: true
award: Oral
priority: 1
website: https://plfb-football.github.io/
abstract: >
    When humans need to learn a new skill, we can acquire knowledge through written books, including textbooks, tutorials, and comments from previous learners. However, current research for decision-making, like reinforcement learning (RL), has primarily required numerous real interactions with the target environment to learn a skill, while failing to utilize the existing knowledge already summarized in the text. The success of Large Language Models (LLMs) sheds light on utilizing such knowledge behind the books. In this paper, we discuss a new policy learning problem called Policy Learning from Books, which aims to leverage rich resources such as books and tutorials to derive a policy network. Inspired by how humans learn from books, we solve the problem via a three-stage framework: understanding, rehearsing, and introspecting (URI). In particular, it first rehearses decision-making trajectories based on the derived knowledge after understanding the books, then introspects in the imaginary dataset to distill a policy network. To validate the practicality of this methodology, we train a football-playing policy via URI and test it in the Google Football game. The agent can beat the built-in AI with a 37% winning rate without interaction with the environment during training, while using GPT as the agent can only achieve a 6% winning rate.
bibtex: >
    @inproceedings{chen2024plfb,
        title={Understanding, Rehearsing, and Introspecting: Learn a Policy from Textual Tutorial Books in Football Games},
        author={Chen, Xiong-Hui and Wang, Ziyan and Du, Yali and Jiang, Shengyi and Fang, Meng and Yu, Yang and Wang, Jun},
        journal={The Thirty-Eight Annual Conference on Neural Information Processing Systems (NeruIPS)},
        year={2024}
    }
---