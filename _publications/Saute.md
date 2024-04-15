---
layout: pub
type: inproceedings
key: highie
title: >
    Sauté rl: Almost surely safe reinforcement learning using state augmentation
author: Sootla, Aivar and Cowen-Rivers, Alexander I and Jafferjee, Taher and Wang, Ziyan and Mguni, David H and Wang, Jun and Ammar, Haitham
abbr: ICML'22
booktitle: International Conference on Machine Learning (ICML)
year: 2022
selected: true
arxiv: 2202.06558
abstract: >
    Satisfying safety constraints almost surely (or with probability one) can be critical for the deployment of Reinforcement Learning (RL) in real-life applications. For example, plane landing and take-off should ideally occur with probability one. We address the problem by introducing Safety Augmented (Saute) Markov Decision Processes (MDPs), where the safety constraints are eliminated by augmenting them into the state-space and reshaping the objective. We show that Saute MDP satisfies the Bellman equation and moves us closer to solving Safe RL with constraints satisfied almost surely. We argue that Saute MDP allows viewing the Safe RL problem from a different perspective enabling new features. For instance, our approach has a plug-and-play nature, i.e., any RL algorithm can be "Sauteed". Additionally, state augmentation allows for policy generalization across safety constraints. We finally show that Saute RL algorithms can outperform their state-of-the-art counterparts when constraint satisfaction is of high importance.
bibtex: >
    @inproceedings{sootla2022saute,
        title={Saut{\'e} rl: Almost surely safe reinforcement learning using state augmentation},
        author={Sootla, Aivar and Cowen-Rivers, Alexander I and Jafferjee, Taher and Wang, Ziyan and Mguni, David H and Wang, Jun and Ammar, Haitham},
        booktitle={International Conference on Machine Learning},
        pages={20423--20443},
        year={2022},
        organization={PMLR}
    }
---