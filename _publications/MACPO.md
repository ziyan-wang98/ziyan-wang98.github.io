---
layout: pub
type: inproceedings
key: MACCA
title: >
    Multi-Agent Constrained Policy Optimisation
author: Gu, Shangding and Kuba, Jakub and Wen, Muning and Chen, Ruiqing and Wang, Ziyan and Tian, Zheng and Wang, Jun and Knoll, Alois and Yang, Yaodong
abbr: Preprint
# equalauthor: 
# correspondence: Yali Du
# website: https://probio-dataset.github.io/
arxiv: 2110.02793
year: 2021
selected: false
code: https://github.com/chauncygu/Multi-Agent-Constrained-Policy-Optimisation
booktitle: arXiv preprint
# code: https://github.com/jiemingcui/probio/
abstract: >
    Developing reinforcement learning algorithms that satisfy safety constraints is becoming increasingly important in real-world applications. In multi-agent reinforcement learning (MARL) settings, policy optimisation with safety awareness is particularly challenging because each individual agent has to not only meet its own safety constraints, but also consider those of others so that their joint behaviour can be guaranteed safe. Despite its importance, the problem of safe multi-agent learning has not been rigorously studied; very few solutions have been proposed, nor a sharable testing environment or benchmarks. To fill these gaps, in this work, we formulate the safe MARL problem as a constrained Markov game and solve it with policy optimisation methods. Our solutions -- Multi-Agent Constrained Policy Optimisation (MACPO) and MAPPO-Lagrangian -- leverage the theories from both constrained policy optimisation and multi-agent trust region learning. Crucially, our methods enjoy theoretical guarantees of both monotonic improvement in reward and satisfaction of safety constraints at every iteration. To examine the effectiveness of our methods, we develop the benchmark suite of Safe Multi-Agent MuJoCo that involves a variety of MARL baselines. Experimental results justify that MACPO/MAPPO-Lagrangian can consistently satisfy safety constraints, meanwhile achieving comparable performance to strong baselines.
bibtex: >
    @inproceedings{Gu2021MultiAgentCP,
        title={Multi-Agent Constrained Policy Optimisation},
        author={Gu, Shangding and Kuba, Jakub and Wen, Muning and Chen, Ruiqing and Wang, Ziyan and Tian, Zheng and Wang, Jun and Knoll, Alois and Yang, Yaodong},
        booktitle={arXiv preprint},
        year={2021},
        url={https://api.semanticscholar.org/CorpusID:238407788}
    }
---