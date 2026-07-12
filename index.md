---
layout: about
title: about
permalink: /

profile:
  align: left
  image: profile.jpg
  email: >
    <p>Email: ziyan.wang<code>[at]</code>kcl<code>[dot]</code>ac<code>[dot]</code>uk</p>

news: true
selected_papers: true
social: true
description: >
  Ph.D. Candidate · Cooperative AI Lab · King's College London
---

<div class="hero-copy">
  <p class="eyebrow">Research overview</p>
  <p>
    I am a fourth-year Ph.D. candidate at the <a href="https://coopai.kcl.ac.uk/">Cooperative AI Lab</a>,
    <a href="https://www.kcl.ac.uk/">King's College London</a>, supervised by
    <a href="https://yalidu.github.io/">Dr Yali Du</a> and
    <a href="https://nms.kcl.ac.uk/sanjay.modgil/">Prof. Sanjay Modgil</a>. My work studies how learning agents can coordinate, communicate, and act safely in complex environments.
  </p>

  <div class="research-overview" aria-label="Research overview">
    <p>
      <strong>My central question is how to distill executable policies from human knowledge.</strong>
      Human knowledge appears as thinking patterns, direct instruction, books, and collective behavior; my work asks how learning agents can turn these media into robust decision-making policies.
    </p>
    <p>
      <strong>In reinforcement learning and MARL,</strong> I study policy learning from books
      (<a href="{{ '/publication/#plfb' | relative_url }}">PLFB</a>), human feedback
      (<a href="{{ '/publication/#m3hf' | relative_url }}">M3HF</a>), causal credit assignment
      (<a href="{{ '/publication/#macca' | relative_url }}">MACCA</a>,
      <a href="{{ '/publication/#GRD' | relative_url }}">GRD</a>), and constrained decision-making
      (<a href="{{ '/publication/#macpo' | relative_url }}">MACPO</a>,
      <a href="{{ '/publication/#SMALL' | relative_url }}">SMALL</a>).
    </p>
    <p>
      <strong>In language-agent systems,</strong> I study how instructions, social interaction, and shared memory shape agent behavior, including
      <a href="{{ '/publication/#instruction-relabeling' | relative_url }}">instruction relabeling</a>,
      <a href="{{ '/publication/#werewolf' | relative_url }}">strategic discussion</a>,
      <a href="{{ '/publication/#concordia' | relative_url }}">mixed-motive generalization</a>,
      <a href="{{ '/publication/#bazaarbench' | relative_url }}">marketplace safety</a>, and
      <a href="{{ '/publication/#memento' | relative_url }}">context management</a>.
    </p>
  </div>

  <p>
    I am currently an Oxford IDAI Fellow working with <a href="https://www.robots.ox.ac.uk/~abibi/">Dr Adel Bibi</a> and
    <a href="https://www.robots.ox.ac.uk/~phst/">Prof. Philip Torr</a>, and a research intern in the Future AI Group at Microsoft Research Cambridge. I have also visited
    <a href="https://www.cmu.edu/">Carnegie Mellon University</a> with <a href="https://feifang.info/">Prof. Fei Fang</a> and worked with Microsoft Research's AI Frontier Group in Redmond.
  </p>
</div>

<div class="research-direction" aria-label="Research direction">
  <div class="research-direction-copy">
    <p class="eyebrow">Research direction</p>
    <h2>Distilling Policy from Human Knowledge</h2>
    <p>
      My research goal is to distill policies from human knowledge. Knowledge can be implicit in reasoning patterns, shaped through direct instruction, preserved in books, and amplified through collective behavior; my papers study how agents can learn from these media to coordinate, adapt, and act safely.
    </p>
    <div class="knowledge-media-list" aria-label="Human knowledge media">
      <span>Thinking patterns</span>
      <span>Direct instruction</span>
      <span>Books</span>
      <span>Collective behavior</span>
    </div>
  </div>

  <figure class="research-direction-figure">
    <img src="{{ '/assets/img/research/knowledge-media.png' | relative_url }}" alt="Four media of human knowledge: thinking patterns, direct instruction, books, and collective behavior.">
  </figure>
</div>

<div id="news" class="section_break"></div>

## <i class="fas fa-bullhorn section-icon"></i> News

{% if page.news %}
  {% include news.html %}
{% endif %}

{% comment %}
<div id="education" class="section_break"></div>

## <i class="fas fa-graduation-cap section-icon"></i> Education

<div class="timeline-list">
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/kcl.png' | relative_url }}" alt="King's College London logo">
    </div>
    <div>
      <h3>Ph.D. in Computer Science</h3>
      <p><strong>King's College London</strong>, Cooperative AI Lab · Dec. 2022 - present</p>
      <p>Fourth-year Ph.D. candidate, supervised by Dr Yali Du and Prof. Sanjay Modgil.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/ucl.png' | relative_url }}" alt="UCL logo">
    </div>
    <div>
      <h3>M.S. in Robotics and Computation</h3>
      <p><strong>University College London</strong> · Sep. 2020 - Dec. 2021</p>
      <p>M.S. in Robotics and Computation, graduated with Distinction; worked with Prof. Jun Wang.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/elte.png' | relative_url }}" alt="Eotvos Lorand University logo">
    </div>
    <div>
      <h3>B.S. in Computer Science</h3>
      <p><strong>Eotvos Lorand University</strong> · Sep. 2016 - Jun. 2019</p>
      <p>Graduated with GPA 4.73/5.0, ranked 3/78.</p>
    </div>
  </div>
</div>
{% endcomment %}

<div id="experience" class="section_break"></div>

## <i class="fas fa-briefcase section-icon"></i> Experience & Visits

<div class="timeline-list">
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/microsoft.png' | relative_url }}" alt="Microsoft logo">
    </div>
    <div>
      <h3>Research Internship, Future AI Group</h3>
      <p><strong>Microsoft Research Cambridge</strong>, Cambridge, UK · May 2026 - present</p>
      <p>Working on multi-agent LLM communication, coordination, and collaborative agent behavior.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/oxford.png' | relative_url }}" alt="University of Oxford logo">
    </div>
    <div>
      <h3>Oxford IDAI Fellowship</h3>
      <p><strong>University of Oxford</strong>, Oxford, UK · Feb. 2026 - present</p>
      <p>Working with Dr Adel Bibi and Prof. Philip Torr on real-time multi-agent LLM anomaly detection and monitoring.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/microsoft.png' | relative_url }}" alt="Microsoft logo">
    </div>
    <div>
      <h3>Research Internship, AI Frontier Group</h3>
      <p><strong>Microsoft Research</strong>, Redmond, US · Sep. 2025 - Dec. 2025</p>
      <p>Worked with Vaishnavi Shrivastava and Prof. Dimitris Papailiopoulos on LLM pre-training and reasoning.</p>
    </div>
  </div>
  <div class="timeline-item">
    <div class="timeline-icon timeline-logo">
      <img src="{{ '/assets/img/logos/cmu.png' | relative_url }}" alt="Carnegie Mellon University logo">
    </div>
    <div>
      <h3>Visiting Ph.D. Student</h3>
      <p><strong>Carnegie Mellon University</strong>, Pittsburgh, US · Feb. 2025 - Jun. 2025</p>
      <p>Visited Prof. Fei Fang's group, working on multi-agent learning and AI for social impact.</p>
    </div>
  </div>
</div>

<div id="publications" class="section_break"></div>

## <i class="fas fa-file-lines section-icon"></i> Selected Publications

{% if page.selected_papers %}
  {% include selected_papers.html %}
{% endif %}

<div id="honors" class="section_break"></div>

## <i class="fas fa-award section-icon"></i> Honors & Teaching

- <b>Honors</b>: Oxford IDAI Fellowship, NeurIPS 2024 Scholar Award, NeurIPS 2024 Oral Presentation
- <b>Teaching</b>: Oxford Machine Learning Summer School, Oxford MLx Fundamentals Summer School, and Optimisation Methods at King's College London

<div id="services" class="section_break"></div>

## <i class="fas fa-clipboard-check section-icon"></i> Professional Services

- <b>Conference reviewer</b> for ICML 2023/24/25/26, NeurIPS 2023/24/25/26, ICLR 2024/25/26, AISTATS 2025/26, and AAMAS 2025/26
- <b>Journal reviewer</b> for IEEE Robotics and Automation Letters, IEEE Transactions on Knowledge and Data Engineering, and IEEE Transactions on Artificial Intelligence
