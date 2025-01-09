---
layout: pub
type: inproceedings
key: MACCA
title: >
    MACCA: Offline Multi-agent Reinforcement Learning with Causal Credit Assignment
author: Wang, Ziyan and Du, Yali and Zhang, Yudi and Fang, Meng and Huang, Biwei
abbr: NeurIPS'24 CRL Workshop
# equalauthor: 
# correspondence: Yali Du
# website: https://probio-dataset.github.io/
arxiv: 2312.03644
year: 2024
selected: False
priority: 444
booktitle: NeurIPS 2024 Causal Representation Learning Workshop (NeurIPS CRL)
# code: https://github.com/jiemingcui/probio/
abstract: >
    Offline Multi-agent Reinforcement Learning (MARL) is valuable in scenarios where online interaction is impractical or risky. While independent learning in MARL offers flexibility and scalability, accurately assigning credit to individual agents in offline settings poses challenges because interactions with an environment are prohibited. In this paper, we propose a new framework, namely Multi-Agent Causal Credit Assignment (MACCA), to address credit assignment in the offline MARL setting. Our approach, MACCA, characterizing the generative process as a Dynamic Bayesian Network, captures relationships between environmental variables, states, actions, and rewards. Estimating this model on offline data, MACCA can learn each agent's contribution by analyzing the causal relationship of their individual rewards, ensuring accurate and interpretable credit assignment. Additionally, the modularity of our approach allows it to seamlessly integrate with various offline MARL methods. Theoretically, we proved that under the setting of the offline dataset, the underlying causal structure and the function for generating the individual rewards of agents are identifiable, which laid the foundation for the correctness of our modeling. In our experiments, we demonstrate that MACCA not only outperforms state-of-the-art methods but also enhances performance when integrated with other backbones.
bibtex: >
    @inproceedings{wang2023macca,
        title={MACCA: Offline Multi-agent Reinforcement Learning with Causal Credit Assignment},
        author={Wang, Ziyan and Du, Yali and Zhang, Yudi and Fang, Meng and Huang, Biwei},
        booktitle={arXiv preprint arXiv:2312.03644},
        year={2024}
    }
---