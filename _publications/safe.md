---
layout: pub
type: inproceedings
title: >
    Safe Reinforcement Learning with Free-form Natural Language Constraints and Pre-Trained Language Models
author: Lou, Xingzhou and Zhang, Junge and Wang, Ziyan and Huang, Kaiqi and Du, Yali
arxiv: 2401.07553
abbr: AAMAS'24
booktitle: The 23rd International Conference on Autonomous Agents and Multi-Agent Systems (AAMAS)
year: 2024
selected: false
priority: 666
abstract: >
    Safe reinforcement learning (RL) agents accomplish given tasks while adhering to specific constraints. Employing constraints expressed via easily-understandable human language offers considerable potential for real-world applications due to its accessibility and non-reliance on domain expertise. Previous safe RL methods with natural language constraints typically adopt a recurrent neural network, which leads to limited capabilities when dealing with various forms of human language input. Furthermore, these methods often require a ground-truth cost function, necessitating domain expertise for the conversion of language constraints into a well-defined cost function that determines constraint violation. To address these issues, we proposes to use pre-trained language models (LM) to facilitate RL agents' comprehension of natural language constraints and allow them to infer costs for safe policy learning. Through the use of pre-trained LMs and the elimination of the need for a ground-truth cost, our method enhances safe policy learning under a diverse set of human-derived free-form natural language constraints. Experiments on grid-world navigation and robot control show that the proposed method can achieve strong performance while adhering to given constraints. The usage of pre-trained LMs allows our method to comprehend complicated constraints and learn safe policies without the need for ground-truth cost at any stage of training or evaluation. Extensive ablation studies are conducted to demonstrate the efficacy of each part of our method.
bibtex: >
    @article{Lou2024SafeRL,
        title={Safe Reinforcement Learning with Free-form Natural Language Constraints and Pre-Trained Language Models},
        author={Lou, Xingzhou and Zhang, Junge and Wang, Ziyan and Huang, Kaiqi and Du, Yali},
        journal={The 23rd International Conference on Autonomous Agents and Multi-Agent Systems (AAMAS)},
        year={2024},
        volume={abs/2401.07553},
        url={https://api.semanticscholar.org/CorpusID:266999399}
    }
---