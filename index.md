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
      <strong>RL and MARL.</strong> I develop learning methods for agents that coordinate under feedback, constraints, and strategic interaction, including
      <a href="{{ '/publication/#m3hf' | relative_url }}">M3HF</a>,
      <a href="{{ '/publication/#macca' | relative_url }}">MACCA</a>,
      <a href="{{ '/publication/#vam' | relative_url }}">VAM</a>,
      <a href="{{ '/publication/#fisher-decorator' | relative_url }}">Fisher Decorator</a>,
      <a href="{{ '/publication/#plfb' | relative_url }}">policy learning from tutorial books</a>,
      <a href="{{ '/publication/#GRD' | relative_url }}">GRD</a>, and
      <a href="{{ '/publication/#macpo' | relative_url }}">MACPO</a>.
    </p>
    <p>
      <strong>Multi-LLM agents.</strong> I study how language-model agents communicate, reason, remember, and generalize in social or open-ended environments, including
      <a href="{{ '/publication/#werewolf' | relative_url }}">Werewolf</a>,
      <a href="{{ '/publication/#chessgpt' | relative_url }}">ChessGPT</a>,
      <a href="{{ '/publication/#concordia' | relative_url }}">Concordia</a>,
      <a href="{{ '/publication/#bazaarbench' | relative_url }}">BazaarBench</a>,
      <a href="{{ '/publication/#memento' | relative_url }}">Memento</a>,
      <a href="{{ '/publication/#instruction-relabeling' | relative_url }}">instruction relabeling</a>, and
      <a href="{{ '/publication/#confidence-competence' | relative_url }}">confidence-competence alignment</a>.
    </p>
    <p>
      <strong>Safe and aligned autonomy.</strong> I build agents that can follow human intent and respect safety constraints, from
      <a href="{{ '/publication/#SMALL' | relative_url }}">SMALL</a> and
      <a href="{{ '/publication/#safe' | relative_url }}">safe RL with free-form natural-language constraints</a> to
      <a href="{{ '/publication/#saute' | relative_url }}">Saute RL</a>, safe MARL benchmarks, and current work on multi-agent LLM monitoring.
    </p>
  </div>

  <p>
    I am currently an Oxford IDAI Fellow working with <a href="https://www.robots.ox.ac.uk/~abibi/">Dr Adel Bibi</a> and
    <a href="https://www.robots.ox.ac.uk/~phst/">Prof. Philip Torr</a>, and a research intern in the Future AI Group at Microsoft Research Cambridge, working with
    <a href="https://scholar.google.com/citations?user=tFihXQQAAAAJ&hl=en">Dr Kirill P. Kalinin</a>. I have also visited
    <a href="https://www.cmu.edu/">Carnegie Mellon University</a> with <a href="https://feifang.info/">Prof. Fei Fang</a> and worked with Microsoft Research's AI Frontier Group in Redmond.
  </p>
</div>

<div id="news" class="section_break"></div>

## <i class="fas fa-bullhorn section-icon"></i> News

{% if page.news %}
  {% include news.html %}
{% endif %}

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
      <p>Working with <a href="https://scholar.google.com/citations?user=tFihXQQAAAAJ&hl=en">Dr Kirill P. Kalinin</a> on multi-agent LLM communication, coordination, and collaborative agent behavior.</p>
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

- <b>Honors</b>: Oxford IDAI Fellowship, NeurIPS 2024 Scholar Award, NeurIPS 2024 Oral Presentation, King's PhD Scholarship, Hungarian State Scholarship
- <b>Teaching</b>: Oxford Machine Learning Summer School, Oxford MLx Fundamentals Summer School, and Optimisation Methods at King's College London

<div id="services" class="section_break"></div>

## <i class="fas fa-clipboard-check section-icon"></i> Professional Services

- <b>Conference reviewer</b> for ICML 2023/24/25/26, NeurIPS 2023/24/25/26, ICLR 2024/25/26, AISTATS 2025/26, and AAMAS 2025/26
- <b>Journal reviewer</b> for IEEE Robotics and Automation Letters, IEEE Transactions on Knowledge and Data Engineering, and IEEE Transactions on Artificial Intelligence
