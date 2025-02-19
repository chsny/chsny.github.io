---
layout: archive
title: "Research projects"
permalink: /research-projects/
author_profile: true
---

## Current projects

### Reinforcement Learning-based control of Directed Energy Deposition

<p align="center">
  <img src='/images/projects/2024 RL control/chap5_RL_POCstructure.png' width=500>
</p>

Directed Energy Deposition is a metal additive manufacturing process that requires precise control of process variables to insure stable process conditions and avoid defects. However, the complexity of the process physics and the non-stationary nature of the process dynamics pose significant challenges to conventional control techniques. Reinforcement Learning (RL), a machine learning paradigm well-suited for control applications, offers greater adaptability and flexibility compared to conventional control techniques.

To address the challenges regarding DED control, this project uses a RL control framework based on a finite element simulation of the DED process. In this framework, the simulation computes the temperature field based on the laser power and scanning speed provided by the agent at every timestep. The agent uses the temperature information to steer the DED process towards stable conditions and correct problematic states as they are detected. The state space, action space and reward function of the environment are described to promote learning. A RL agent is trained successfully on the proposed environment and is able to control the melt pool temperature for several complex scanning paths. These results pave the way to an experimental RL controller of the DED process.

### Deep Learning-based anomaly detection in Directed Energy Deposition

<p align="center">
  <img src='/images/projects/2023 anomaly detection/anomaly detection_graphabstract.png' width=500>
</p>

In this project, a method to produce thermal anomalies with variation of process parameters is used to produce a significant dataset of labelled, raw hyperspectral melt pool signatures. Deep Learning is leveraged to build an anomaly classification model trained on the hyperspectral dataset. The performance of the model is analysed in detail, both per-class and on complete parts. Saliency metrics are used to identify the discriminatory spatial and spectral regions of the input data. This last step showcases the importance of hyperspectral data for anomaly prediction.

### Temperature estimation of the melt pool in Directed Energy Deposition using Hyperspectral Imaging
<p align="center">
  <img src='/images/projects/2021 temperature estimation/chap2_exp_temp_2d.png' width=300>
</p>

Implementation of the multicolor pyrometry method to estimate temperature using high-dimensional hyperspectral images in Metal Additive Manufacturing.

$$ \hat T = \arg \min_T\sum^N_{i=1} \left | \frac{L_{\lambda,i}}{L_{\lambda,n}} - \frac{B(\lambda_i,T)}{B(\lambda_n,T)} \right |^2$$

[Link to the GitHub repository.](https://github.com/chsny/mosaic-temp)

## Past projects
{% include base_path %}


{% for post in site.portfolio reversed %}
  {% include archive-single.html %}
{% endfor %}



