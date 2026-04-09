---
permalink: /
title: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
  .page__title, #page-title {
    display: none !important;
  }
</style>

<div style="display: flex; flex-wrap: wrap; gap: 30px; align-items: flex-start;">

<div style="flex: 1 1 400px;" markdown="1">

# About Me
***

I am a Master's student in Informatics at the **University of Zurich (UZH)**, majoring in Artificial Intelligence and minoring in Data Science. My research interests lie at the intersection of **Computer Vision**, **Robotics**, and **Multimodal Models**.

Currently, I am a student researcher at:
* [**Computer Vision and Geometry Group (ETHZ CVG)**](https://cvg.ethz.ch/), working on Real-time Visual-Inertial-LiDAR Gaussian Splatting SLAM.
* [**Robotics and Perception Group (UZH RPG)**](https://rpg.ifi.uzh.ch/), focusing on Event Camera-Enhanced Robot Motor Control Policies.

I have a experience in:
* **Robotics & RL**: Deep experience in RL/IL training and deployment on robot arms and drones.
* **3D Vision & SLAM**: Expertise in Gaussian Splatting (3DGS), Visual Odometry, and SLAM pipelines.
* **Foundation Models**: Familiarity with VLA models, LLMs, and multimodal pre-training.

Previously, I worked as a Computer Vision Algorithm Intern at [**IntSig Information Co., Ltd.**](https://www.intsig.com/en/)

Feel free to reach out to me at [jianwen.cao@uzh.ch](mailto:jianwen.cao@uzh.ch).

</div>

<div style="flex: 1 1 0; min-width: 300px; border-left: 1px solid #ddd; padding-left: 20px;" markdown="1">

# Publications
***
* **[Accepted]** **Jianwen Cao**, et al. [**Generative Event Pretraining with Foundation Model Alignment.**](https://arxiv.org/abs/2603.23032) *CVPR 2026.*
* **[Under Review]** ..., **Jianwen Cao**, et al. [**Memory Over Maps: 3D Object Localization Without Reconstruction.**](https://ruizhou-cn.github.io/memory-over-maps/) *IROS 2026.*
* **[Published]** **Jianwen Cao**, et al. [**Fuse Tune: Hierarchical Decoder Towards Efficient Transfer Learning.**](https://link.springer.com/chapter/10.1007/978-981-99-8540-1_17) *PRCV 2023.*

</div>

</div>

<style>
  .project-item {
    display: flex;
    flex-direction: row;
    margin-bottom: 30px;
    gap: 25px;
    align-items: flex-start;
  }
  .project-teaser {
    flex: 0 0 280px; /* --- 修改这里：调整图片宽度 --- */
    height: 120px;   /* --- 修改这里：调整图片高度 --- */
    overflow: hidden;
    border-radius: 6px;
  }
  .project-teaser img {
    width: 100%;
    height: 100%;
    object-fit: fill; /* 允许不保持宽高比的压缩 */
    display: block;
  }
  .project-content {
    flex: 1;
  }
  .project-content h3 {
    margin-top: 0;
    margin-bottom: 8px;
    font-size: 1.25em;
  }
  .project-content p {
    margin: 0;
    font-size: 0.95em;
    line-height: 1.5;
  }
  @media (max-width: 768px) {
    .project-item {
      flex-direction: column;
    }
    .project-teaser {
      flex: 0 0 auto;
      width: 100%;
      height: 200px;
    }
  }
</style>

<br>

# Projects
***
{% include base_path %}
{% assign sorted_portfolio = site.portfolio | sort: "order" %}
{% for post in sorted_portfolio %}
  <div class="project-item">

    <div class="project-teaser">
      {% if post.teaser %}
        <img src="{{ base_path }}/images/{{ post.teaser }}" alt="{{ post.title }}">
      {% else %}
        {% assign excerpt_parts = post.excerpt | split: "src='" %}
        {% if excerpt_parts.size > 1 %}
          {% assign img_path = excerpt_parts[1] | split: "'" | first %}
          <img src="{{ base_path }}{{ img_path }}" alt="{{ post.title }}">
        {% endif %}
      {% endif %}
    </div>
    <div class="project-content">
      <h3>
        {% if post.paperurl %}
          <a href="{{ post.paperurl }}">{{ post.title }}</a>
        {% else %}
          <a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a>
        {% endif %}
      </h3>
      <div class="archive__item-excerpt">
        {% assign excerpt_text = post.excerpt | split: "<br/>" | first %}
        {{ excerpt_text | markdownify | remove: '<p>' | remove: '</p>' }}
      </div>
    </div>
  </div>
{% endfor %}