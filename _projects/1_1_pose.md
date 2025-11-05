---
layout: page
title: "Action Recognition from 3D Point Clouds"
date: 2022-09-01
description: "Presented at IPIU 2023, this paper explores action recognition using 3D point clouds generated from FMCW radar signals."
category: research
importance: 6
img: assets/img/publication_preview/thumb_IPIU.gif
related_publications: true
bibliography: [2023IPIU]
---

## Overview

This paper introduces a method for **action recognition** using **3D point clouds** generated from **Frequency Modulated Continuous Wave (FMCW) radar signals**. The approach applies **Support Tensor Machine (STM)** to classify various actions based on the 3D spatial and temporal information contained in the point clouds.

## Key Contributions

- **3D Point Cloud Generation**:

  - Applied **3D Capon Beamforming** to generate 3D point clouds from FMCW radar data.
  - Utilized **subsampling** to reduce computational complexity while maintaining accuracy.

<div class="row">
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/Ti_mPoint_crouching.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Crouching</p>
  </div>
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/Ti_mPoint_hands_up.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Hands Up</p>
  </div>
</div>

<div class="row">
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/Ti_mPoint_sit.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Sitting</p>
  </div>
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/Ti_mPoint_stand_up.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Standing Up</p>
  </div>
</div>

<div class="row">
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/Ti_mPoint_walking.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Walking</p>
  </div>
</div>

- **Action Classification**:
  - Used **Support Tensor Machine (STM)** for classification, achieving an accuracy of **82%** across five distinct actions.
  - Analyzed misclassification cases and identified potential improvements.

## Experimental Setup

- **Radar Sensor**: Texas Instruments IWR6843-ODS
- **Tested Actions**: Sitting, standing, walking, raising hands, squatting.
- **Participants**: 11 individuals performing each action within a 0.5m–2m range from the radar.

## Results

- Achieved **82% accuracy** in classifying five different actions.
- Highlighted key areas for further improvement, such as handling overlapping gesture patterns.

## Poster (in Korean)

<iframe src="/assets/pdf/IPIU2023_poster.pdf" width="100%" height="600px">
    Your browser does not support embedding PDFs. You can <a href="/assets/pdf/IPIU2023_poster.pdf">download the PDF here</a>.
</iframe>

## Conclusion

This research demonstrates the feasibility of using FMCW radar for robust action recognition, providing a cost-effective and privacy-preserving alternative to camera-based systems. {% cite 2023IPIU %}

## Additionally...

- I also worked for fall detection with 3D point cloud with LSTM and RNN structures!
- The most difficult part in radar projects is always getting large amount of dataset😇
