---
layout: pub
type: inproceedings
key: highie
title: >
    Chessgpt: Bridging policy learning and language modeling
author: Feng, Xidong and Luo, Yicheng and Wang, Ziyan and Tang, Hongrui and Yang, Mengyue and Shao, Kun and Mguni, David and Du, Yali and Wang, Jun
abbr: NeurIPS'23
booktitle: The Thirty-Seventh Annual Conference on Neural Information Processing Systems Datasets and Benchmarks Track (NeurIPS D&B Track)
year: 2023
selected: true
code: https://github.com/waterhorse1/ChessGPT
website: https://huggingface.co/Waterhorse/chessgpt-base-v1
arxiv: 2306.09200
abstract: >
    Humans talk in free-form while negotiating the expressed meanings or common ground. Despite the impressive conversational abilities of the large generative language models, they do not consider the individual differences in contextual understanding in a shared situated environment. In this work, we propose MindDial, a novel conversational framework that can generate situated free-form responses to negotiate common ground. We design an explicit mind module that can track three-level beliefs -- the speaker's belief, the speaker's prediction of the listener's belief, and the common belief based on the gap between the first two. Then the speaking act classification head will decide to continue to talk, end this turn, or take task-related action. We augment a common ground alignment dataset MutualFriend with belief dynamics annotation, of which the goal is to find a single mutual friend based on the free chat between two agents. Experiments show that our model with mental state modeling can resemble human responses when aligning common ground meanwhile mimic the natural human conversation flow. The ablation study further validates the third-level common belief can aggregate information of the first and second-order beliefs and align common ground more efficiently.
bibtex: >
    @inproceedings{feng2024chessgpt,
        title={Chessgpt: Bridging policy learning and language modeling},
        author={Feng, Xidong and Luo, Yicheng and Wang, Ziyan and Tang, Hongrui and Yang, Mengyue and Shao, Kun and Mguni, David and Du, Yali and Wang, Jun},
        journal={The Thirty-Seventh Annual Conference on Neural Information Processing Systems Datasets and Benchmarks Track (NeurIPS D&B 2023)},
        volume={36},
        year={2024}
    }
---