---
layout: pub
type: inproceedings
title: >
    Interpretable Reward Redistribution in Reinforcement Learning: A Causal Approach
author: Zhang, Yudi and Du, Yali and Huang, Biwei and Wang, Ziyan and Wang, Jun and Fang, Meng and Pechenizkiy, Mykola
arxiv: 2305.18427
abbr: NeurIPS'23
correspondence: Zheng, Zilong
website: https://reedzyd.github.io/GenerativeReturnDecomposition/
booktitle: The Thirty-Seventh Annual Conference on Neural Information Processing Systems (NeruIPS)
year: 2023
selected: false
abstract: >
    A major challenge in reinforcement learning is to determine which state-action pairs are responsible for future rewards that are delayed. Reward redistribution serves as a solution to re-assign credits for each time step from observed sequences. While the majority of current approaches construct the reward redistribution in an uninterpretable manner, we propose to explicitly model the contributions of state and action from a causal perspective, resulting in an interpretable reward redistribution and preserving policy invariance. In this paper, we start by studying the role of causal generative models in reward redistribution by characterizing the generation of Markovian rewards and trajectory-wise long-term return and further propose a framework, called Generative Return Decomposition (GRD), for policy optimization in delayed reward scenarios. Specifically, GRD first identifies the unobservable Markovian rewards and causal relations in the generative process. Then, GRD makes use of the identified causal generative model to form a compact representation to train policy over the most favorable subspace of the state space of the agent. Theoretically, we show that the unobservable Markovian reward function is identifiable, as well as the underlying causal structure and causal models. Experimental results show that our method outperforms state-of-the-art methods and the provided visualization further demonstrates the interpretability of our method. The project page is located at https://reedzyd. github. io/GenerativeReturnDecomposition/.
bibtex: >
    @inproceedings{NEURIPS2023_402e1210,
        author = {Zhang, Yudi and Du, Yali and Huang, Biwei and Wang, Ziyan and Wang, Jun and Fang, Meng and Pechenizkiy, Mykola},
        booktitle = {The Thirty-Seventh Annual Conference on Neural Information Processing Systems (NeruIPS)},
        editor = {A. Oh and T. Neumann and A. Globerson and K. Saenko and M. Hardt and S. Levine},
        pages = {20208--20229},
        publisher = {Curran Associates, Inc.},
        title = {Interpretable Reward Redistribution in Reinforcement Learning: A Causal Approach},
        url = {https://proceedings.neurips.cc/paper_files/paper/2023/file/402e12102d6ec3ea3df40ce1b23d423a-Paper-Conference.pdf},
        volume = {36},
        year = {2023}
    }

---