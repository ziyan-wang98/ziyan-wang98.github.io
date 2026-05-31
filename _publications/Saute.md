---
layout: pub
type: inproceedings
key: saute
title: >
    Saute RL: Almost Surely Safe Reinforcement Learning Using State Augmentation
author: Sootla, Aivar and Cowen-Rivers, Alexander and Jafferjee, Taher and Wang, Ziyan and Mguni, David H and Wang, Jun and Ammar, Haitham
abbr: ICML'22
booktitle: Proceedings of the 39th International Conference on Machine Learning (ICML)
year: 2022
selected: False
award: Spotlight
arxiv: 2202.06558
venue_url: https://proceedings.mlr.press/v162/sootla22a.html
pdf: https://proceedings.mlr.press/v162/sootla22a/sootla22a.pdf
abstract: >
    Satisfying safety constraints almost surely (or with probability one) can be critical for the deployment of Reinforcement Learning (RL) in real-life applications. For example, plane landing and take-off should ideally occur with probability one. We address the problem by introducing Safety Augmented (Saute) Markov Decision Processes (MDPs), where the safety constraints are eliminated by augmenting them into the state-space and reshaping the objective. We show that Saute MDP satisfies the Bellman equation and moves us closer to solving Safe RL with constraints satisfied almost surely. We argue that Saute MDP allows viewing the Safe RL problem from a different perspective enabling new features. For instance, our approach has a plug-and-play nature, i.e., any RL algorithm can be "Sauteed". Additionally, state augmentation allows for policy generalization across safety constraints. We finally show that Saute RL algorithms can outperform their state-of-the-art counterparts when constraint satisfaction is of high importance.
bibtex: >
    @inproceedings{sootla2022saute,
        title={Saute RL: Almost Surely Safe Reinforcement Learning Using State Augmentation},
        author={Sootla, Aivar and Cowen-Rivers, Alexander and Jafferjee, Taher and Wang, Ziyan and Mguni, David H and Wang, Jun and Ammar, Haitham},
        booktitle={Proceedings of the 39th International Conference on Machine Learning},
        pages={20423--20443},
        year={2022},
        organization={PMLR},
        url={https://proceedings.mlr.press/v162/sootla22a.html}
    }
---
