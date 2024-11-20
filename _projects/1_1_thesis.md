---
layout: page
title: "Deep Learning-Based Semiconductor Product Inspection"
description: "A lightweight twin network for real-time defect detection in semiconductor IC substrates."
date: 2024-06-01
category: research
importance: 1
img: assets/img/thumb_thesis.PNG
related_publications: true
bibliography: [thesis]
---

## Overview

For my Master’s degree thesis {% cite thesis %}, I developed a **lightweight twin network-based defect detection system** for **IC substrates**. This system is designed to be robust against mis-registration and characteristic differences, ensuring high accuracy and reliability in real-time semiconductor inspections.

## Objectives

- **To design a robust defect detection system for semiconductor inspection**: This research focuses on inspecting IC substrates, leveraging their repetitive patterns to implement comparison-based inspection techniques that detect changes between test and reference images.

- **To minimize mis-registration errors while maintaining lightweight computational requirements**: While twin network structures, which use two identical encoders for feature extraction and comparison, are commonly used for change detection, they are prone to pseudo changes and mis-registration errors. These issues complicate the detection of micro defects critical for accurate inspections.

- **To apply state-of-the-art deep learning techniques for real-time performance**: Existing methods, such as co-attention modules and similar architectures, demand significant memory, computational resources, and processing time, making them unsuitable for deployment in real industrial environments.

<div class="row justify-content-center">
  <div class="col-auto">
    {% include figure.liquid path="assets/img/publication_preview/thesis_CCTSNet.png" title="Image 1" class="img-fluid" %}
  </div>
  <div class="col-auto">
    {% include figure.liquid path="assets/img/publication_preview/thesis_coatt.png" title="Image 2" class="img-fluid" %}
  </div>
</div>
<div class="caption">
    Proposed network structure - C-CTSNet and ch-co-att module
    
</div>

## Key Contributions

- **Developed a Siamese Network-based architecture optimized for defect detection in repetitive patterns**: Proposed C-TSNet, a hybrid architecture combining twin and single networks to enhance robustness against mis-registration and color variations, while maintaining low computational latency.
- **Enhanced robustness using advanced attention mechanisms**: Introduced CC-TSNet, which incorporates a channel co-attention module to further improve resilience to characteristic differences.
- **Achieved real-time performance with lightweight computational requirements**: Designed the architecture to be efficient for deployment in industrial settings, ensuring fast and accurate defect detection.

<div class="row justify-content-center">
  <div class="col-md-5">
    {% include figure.liquid path="assets/img/publication_preview/thesis_rep.png" title="Image 1" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-md-5">
    {% include figure.liquid path="assets/img/publication_preview/thesis_pseudo.png" title="Image 2" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Example of IC substrates and IC substrate dataset including registration error and characteristic difference 🕵️
    
</div>

## Technologies and Tools

- **Frameworks**: TensorFlow, PyTorch
- **Key Techniques**:
  - Siamese Networks (also known as twin network)
  - Change Detection
  - Attention Mechanisms
- **Hardware**: NVIDIA GPUs for accelerated training and inference

## Results

- **Superior performance on real-world industrial datasets**: Validated the proposed methods on an IC substrate dataset, outperforming traditional models like U-Net and Base-Twin networks in terms of F1-scores and false positives.
- **Improved robustness against pseudo-changes**: The integration of the channel co-attention module significantly enhanced the model's ability to handle characteristic differences, reducing false positive rates.
- **Real-time suitability**: Achieved accuracy comparable to module-based methods, with only one-third of the computational latency, making the system highly effective for real-time manufacturing processes.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/thesis_logit1.png" title="result image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qualitative performance evaluation - by merging the logits from the single decoder and the twin network decoder, errors caused by registration discrepancies are reduced.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/thesis_logit2.png" title="result image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qualitative performance evaluation - C-TSNet did not correct these differences with the single decoder, but with the ch-co-att module, it showed that these errors were corrected.
</div>

## Additionally...

- _Exploration of advanced techniques_: Beyond the main contributions, I explored various advanced deep learning methods, including Knowledge Distillation and Vision Transformers (ViT). While these approaches showed promise, they revealed limitations when applied to the specific challenges of IC substrate inspection.
- _Efforts to improve single network performance for non-repetitive patterns_: Recognizing the need for a solution in cases where products lack repetitive patterns, I focused on enhancing single network performance using ViT. Although the experiments did not yield the desired results, they offered valuable insights into the difficulties of defect detection in non-repetitive contexts.
- _Future potential_: These explorations highlight opportunities for further research. Perhaps someday, I will revisit these techniques to develop more robust solutions for diverse inspection scenarios.
- I labelled more than 100,000 images for the project🤪
