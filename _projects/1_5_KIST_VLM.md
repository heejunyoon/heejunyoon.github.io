---
layout: page
title: "Robust 3D Scene Understanding for Multi-View VLMs"
description: "Enhancing Vision-Language Models (VLMs) with 3D position embeddings to improve spatial reasoning in multi-view scenes."
date: 2025-06-30
category: research
importance: 2
img: assets/img/thumb_KIST_VLM.PNG
related_publications: true
---

## Overview

Standard Vision-Language Models (VLMs) struggle to understand 3D spatial relationships (e.g., "behind," "under") when presented with multiple 2D images. This project, which serves as a foundation for my current embodied AI research, successfully developed a method to **inject 3D geometric information** into a 2D VLM (NVILA-based). This enhancement allows the VLM to build a robust **3D spatial awareness** from multi-view inputs.

## Objectives (Key Questions)

- **To achieve 3D spatial awareness from 2D images**: How can a VLM understand that image patches from separate views (e.g., front, left, right) belong to the same continuous 3D space?
- **To integrate geometric data efficiently**: How can we inject 3D geometric information (from LiDAR/point clouds) into a pre-trained VLM **without costly full-scale retraining**?

## Core Methodology

- **1. Data Pipeline Development:**
    - Created an automated sampling pipeline to generate structured, multi-view (8-image) training samples from point-cloud-based datasets (e.g., ScanNet).
- **2. 3D Position Embedding:**
    - Derived 3D coordinates from point clouds corresponding to each 2D image patch.
    - Projected these coordinates into a high-dimensional `3D Position Embedding` vector.
- **3. Geometric-Visual Fusion:**
    - Fused geometric awareness by **summing** the new `3D Position Embedding` with the existing `2D Position Embedding` of the ViT tokens.
- **4. Efficient Fine-Tuning:**
    - Froze the entire pre-trained VLM (ViT and LLM) and **fine-tuned only the projection head** to efficiently learn this new, spatially-aware representation.

## Results

The proposed method significantly outperformed strong baselines on 3D spatial reasoning benchmarks:

- **ScanQA:** Achieved **44.78% Refined EM@1** (outperforming Gemini 2.5 Pro at 40.86%).
- **MuirBench:** Achieved **64.52% Accuracy** (outperforming Gemini 2.5 Pro at 59.14%).