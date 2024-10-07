---
layout: about
title: about
permalink: /

profile:
  align: right
  image: profile.jpg
  email: >
    <p>Email: ziyan.wang<code>[at]</code>kcl<code>[dot]</code>ac<code>[dot]</code>uk</p>

news: true  # includes a list of news items
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page

---
I am currently the second-year Ph.D. student at [Cooperative AI Lab](https://coopai.kcl.ac.uk/), [King's College London](https://www.kcl.ac.uk/). I am supervised by [Dr Yali Du](https://yalidu.github.io/) and [Prof. Sanjay Modgil](https://nms.kcl.ac.uk/sanjay.modgil/). I received my M.S. degree from the [University College London](https://www.ucl.ac.uk/), where I was supervised by [Prof. Jun Wang](http://www0.cs.ucl.ac.uk/staff/jun.wang/). I have also been fortunate to work closely with [Prof. Fei Fang](https://feifang.info/) at the Carnegie Mellon University.

My research interests lie in the intersection of Multi-agent Reinforcement Learning, Large Language Models, and Robotics. Current research themes include:

- **Multi-agent Reinforcement Learning**: Developing algorithms that enable agents to learn to collaborate and compete in complex environments.
- **Human Robot Cooperation**: Bridging the gap between human and robot communication, enabling robots to understand huamn's free-form instructions.
- **Safe Reinforcement Learning**: Ensuring that agents learn policies that satisfy given constraints while accomplishing tasks.
- **Large Language Models**: Exploring the capabilities of large language models in multi-agent settings.

<div id="news" class="section_break"></div>

## News

{% if page.news %}
<!-- <div id="news" class="post"> -->
  {% include news.html %}
<!-- </div> -->
{% endif %}

<div id="publications" class="section_break"></div>

## Selected Publications

{% if page.selected_papers %}
<!-- <div id="publications" class="post"> -->
  {% include selected_papers.html %}
<!-- </div> -->
{% endif %}


<div id="services" class="section_break"></div>

## Professional Services

- <b>Conference reviewer</b> for ICML 2024, NeurIPS 2024, ICLR 2025, AISTATS 2025
- <b>Journal reviewer</b> for IEEE Transactions on Knowledge and Data Engineering (TKDE), IEEE Transactions on Artificial Intelligence (TAI)

