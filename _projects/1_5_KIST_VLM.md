---
layout: page
title: "Robust 3D Scene Understanding for Multi-View VLMs"
description: "Adding 3D position embeddings to a VLM so it can reason about space across multiple views (KIST)."
date: 2025-06-30
category: research
importance: 2
img: assets/img/thumb_KIST_VLM.png
related_publications: true
---

## Overview

Standard vision-language models (VLMs) have trouble with 3D relations like "behind" or "under" when they see several 2D images of the same scene. In this KIST project, I added **3D geometric information** to a 2D VLM based on NVILA so it could reason about space across multiple views. The model later became the perception module of my [embodied AI project](/projects/1_6_KIST_VLA/).

## Questions

- How can a VLM tell that image patches from different views (front, left, right) belong to the same 3D space?
- Can we add 3D information from LiDAR or point clouds to a pretrained VLM without retraining the whole model?

## Method

1. **Data pipeline.** I wrote a sampling pipeline that builds multi-view training samples (8 images each) from point-cloud datasets such as ScanNet.
2. **3D position embedding.** For each 2D image patch, I took the matching 3D coordinates from the point cloud and projected them into a `3D Position Embedding` vector.
3. **Fusion.** I added the 3D position embedding to the existing 2D position embedding of the ViT tokens.
4. **Fine-tuning.** I froze the pretrained VLM (ViT and LLM) and trained only the projection head.

<div class="row justify-content-center">
  <div class="col-auto">
    {% include figure.liquid path="assets/img/proj/KIST_VLM.png" title="Model Architecture" class="img-fluid" %}
  </div>
</div>
<div class="caption">
  The model architecture with 3D position embeddings.
</div>

## Results

The model beat strong baselines on two 3D spatial reasoning benchmarks:

- **ScanQA:** 44.78% Refined EM@1 (Gemini 2.5 Pro: 40.86%)
- **MuirBench:** 64.52% accuracy (Gemini 2.5 Pro: 59.14%)
