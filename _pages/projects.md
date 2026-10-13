---
layout: archive
title: "Current projects"
permalink: /research-projects/
author_profile: true
---
My current work focuses on applying **Machine Learning** and **Deep Learning** techniques to address reliability challenges in **Metal Additive Manufacturing**. The process that I am working on is Directed Energy Deposition, a laser and blown powder process. 

## In-situ prediction of 316L-CuCr1Zr multi-material composition with Deep Learning

<p align="center">
  <img src='/images/projects/2026 multimaterial prediction/graphabstract.png' width=500>
</p>

This work investigates the use of hyperspectral imaging and deep learning to monitor material composition during laser-based Directed Energy Deposition (DED). A convolutional neural network (CNN) was developed to analyse in-situ near-infrared hyperspectral images and predict local composition during the fabrication of 316L stainless steel–CuCr1Zr copper multi-material structures. The approach enables real-time identification of compositional transitions and deviations from the designed material gradient, paving the way for closed-loop process control and more reliable manufacturing of functionally graded metallic components. See [publication](https://www.sciencedirect.com/science/article/pii/S2214860426002952).

## Reinforcement Learning-based MIMO control

<p align="center">
  <img src='/images/projects/2024 RL control/chap5_RL_POCstructure.png' width=500>
</p>

Metal Additive Manufacturing requires precise control of process variables to insure stable process conditions and avoid defects. However, the complexity of the process physics and the non-stationary nature of the process dynamics pose significant challenges to conventional control techniques. Reinforcement Learning (RL), a machine learning paradigm well-suited for control applications, offers greater adaptability and flexibility compared to conventional control techniques.

<p align="center">
  <img src='/images/projects/2024 RL control/methods_sim_3Dview.png' width=500>
</p>

To address the challenges regarding DED control, this project uses a **RL control framework** based on a **finite element simulation of the metal Additive Manufacturing process**. In this framework, the simulation computes the temperature field based on the laser power and scanning speed provided by the agent at every timestep. The agent uses the temperature information to steer the DED process towards stable conditions and correct problematic states as they are detected. The state space, action space and reward function of the environment are described to promote learning. A RL agent is trained successfully on the proposed environment and is able to control the melt pool temperature for several complex scanning paths. These results pave the way to an experimental RL controller of the DED process.

## Deep Learning-based in-situ anomaly detection

<p align="center">
  <img src='/images/projects/2023 anomaly detection/anomaly detection_graphabstract.png' width=700>
</p>

Metal Additive Manufacturing requires process monitoring to ensure the highest part quality. Detecting and avoiding material defects to meet high material requirements remains a challenge due to the complexity of the process.

To address this challenge, this study presents a novel approach that combines hyperspectral imaging with **Convolutional Neural Networks to classify process anomalies**. Hyperspectral in-situ monitoring captures the light emitted from the melt pool over the 2 spatial axis, but also over the spectral axis. The proposed classification model reaches an accuracy in excess of 94% over the validation set. The classification mechanism of the proposed model is investigated thanks to the Guided GradCAM visualization method and links with the melt pool temperature distribution are formulated. The inference speed of the optimized model is measured and shown to be compatible with realtime applications. See [publication](https://ieeexplore.ieee.org/document/10769412).

## Melt pool temperature estimation with multicolor pyrometry

Multicolor pyrometry is a non-contact temperature measurement technique that fits a greybody spectrum to the spectral radiance of an object at multiple wavelengths to determine its temperature. Unlike single-color or two-color pyrometry, multicolor pyrometry can account for variations in emissivity by solving for both temperature and emissivity simultaneously, improving accuracy in dynamic and high-temperature environments. This technique is particularly useful in cases where emissivity is unknown or changing, such as in Metal Additive Manufacturing.

$$ \hat T = \arg \min_T\sum^N_{i=1} \left | \frac{L_{\lambda,i}}{L_{\lambda,n}} - \frac{B(\lambda_i,T)}{B(\lambda_n,T)} \right |^2$$

This technique is used in Directed Energy Deposition for in-situ monitoring of the melt pool temperature and stability. Real-time temperature measurements help to detect defects like lack of fusion or overheating, optimize process parameters for better mechanical properties, and ensure repeatability. This technique was implemented in MATLAB, see the [GitHub repository](https://github.com/chsny/mosaic-temp).

<p align="center">
  <img src='/images/projects/2021 temperature estimation/chap2_exp_temp_2d.png' width=300>
</p>

# Past projects
{% include base_path %}


{% for post in site.portfolio reversed %}
  {% include archive-single.html %}
{% endfor %}



