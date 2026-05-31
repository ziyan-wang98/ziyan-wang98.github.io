---
layout: pub
type: inproceedings
key: m3hf
title: >
    M3HF: Multi-agent Reinforcement Learning from Multi-phase Human Feedback of Mixed Quality
author: Wang, Ziyan and Zhang, Zhicheng and Fang, Fei and Du, Yali

arxiv: 2503.02077
venue_url: https://proceedings.mlr.press/v267/wang25el.html
pdf: https://raw.githubusercontent.com/mlresearch/v267/main/assets/wang25el/wang25el.pdf
code: https://github.com/cooperativex/M3HF
image: m3hf.png
abbr: ICML'25
booktitle: Forty-Second International Conference on Machine Learning (ICML)
year: 2025
selected: true
priority: 0
abstract: >
    Designing effective reward functions in multi-agent reinforcement learning (MARL) is a significant challenge, often leading to suboptimal or misaligned behaviors in complex, coordinated environments. We introduce Multi-agent Reinforcement Learning from Multi-phase Human Feedback of Mixed Quality (M3HF), a novel framework that integrates multi-phase human feedback of mixed quality into the MARL training process. By involving humans with diverse expertise levels to provide iterative guidance, M3HF leverages both expert and non-expert feedback to continuously refine agents' policies. During training, we strategically pause agent learning for human evaluation, parse feedback using large language models to assign it appropriately and update reward functions through predefined templates and adaptive weight by using weight decay and performance-based adjustments. Our approach enables the integration of nuanced human insights across various levels of quality, enhancing the interpretability and robustness of multi-agent cooperation. Empirical results in challenging environments demonstrate that M3HF significantly outperforms state-of-the-art methods, effectively addressing the complexities of reward design in MARL and enabling broader human participation in the training process.
bibtex: >
    @inproceedings{pmlr-v267-wang25el,
        title={M3HF: Multi-agent Reinforcement Learning from Multi-phase Human Feedback of Mixed Quality},
        author={Wang, Ziyan and Zhang, Zhicheng and Fang, Fei and Du, Yali},
        booktitle={Proceedings of the 42nd International Conference on Machine Learning},
        pages={65429--65448},
        year={2025},
        volume={267},
        series={Proceedings of Machine Learning Research},
        publisher={PMLR},
        url={https://proceedings.mlr.press/v267/wang25el.html}
    }
---
