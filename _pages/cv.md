---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **University of Zurich (UZH)**, Zurich, Switzerland
  * **M.Sc. in Informatics** (Major: Artificial Intelligence, Minor: Data Science), 2024 – Present
  * GPA: 5.57/6
  * Core Courses: Data Science (6.0/6.0), Machine Learning for Natural Language Processing (6.0/6.0), Vision Algorithms for Mobile Robotics (5.5/6.0), ETHZ 3D Vision (5.75/6.0), ETHZ Virtual Reality (6.0/6.0).
* **Nanjing University of Information Science and Technology (NUIST)**, Nanjing, China
  * **B.Eng. in Artificial Intelligence**, 2020 – 2024
  * GPA: 87.6/100

Research & Internship Experience
======
* **Computer Vision and Geometry Group (ETHZ CVG)**, Student Researcher, Mar 2025 – Feb 2026
  * *Real-time Visual-Inertial-LiDAR Gaussian Splatting SLAM*
  * Reproduced and improved GS-LIVO to achieve better geometric accuracy and mapping efficiency, reaching SOTA performance.
* **Robotics and Perception Group (UZH RPG)**, Student Researcher, Feb 2025 – Jan 2026
  * *Event Camera-Enhanced Robot Motor Control Policies*
  * Conducted autoregressive pre-training on multimodal data, significantly improving the performance and robustness of downstream vision and control tasks.
* **IntSig Information Co., Ltd.**, Computer Vision Algorithm Intern, Jul 2023 – Oct 2023
  * Developed object detection algorithms based on improved DETR series architectures.

Skills
======
* **Robot Arm & Dog Deployment**: MuJoCo IL/RL training and ROS2 deployment experience on Soarm101.
* **VLA Models**: RT-1, RT-2, Pi0, GR00T, ACT, and other Vision-Language-Action models.
* **Object Detection & Segmentation**: RCNN series (Fast, Faster, Mask, Cascade), DETR, GLIP, GLIP2, SAM.
* **Pre-training & Contrastive Learning**: Masked Modeling (BERT, MAE, BEiT, EVA), MoCo, CLIP, DINO.
* **LLMs & Multimodal Models**: GPT, MoE, RoPE, RAG, Engram; experience in pre-training Chinese corpora and RLHF post-training.
* **Generative Models**: GAN, VAE, VQ-VAE, VQGAN, Latent Diffusion Models.
* **SLAM & 3D Vision**: PTAM, FAST-LIVO2, 3DGS, HI-SLAM2, GS-LIVO.

Awards
======
* **Contemporary Undergraduate Mathematical Contest in Modeling (CUMCM)**, 2022
  * Second Prize at the National Level. Responsible for designing robust mathematical models and optimization algorithms.

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
