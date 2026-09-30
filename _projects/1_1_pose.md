---
layout: page
title: "Action Recognition from 3D Point Clouds"
date: 2022-09-01
description: "Recognizing human actions from 3D point clouds built from FMCW radar signals (IPIU 2023)."
category: research
importance: 6
img: assets/img/publication_preview/thumb_IPIU.gif
related_publications: true
bibliography: [2023IPIU]
---

## Overview

In this paper, we recognize human actions from **3D point clouds** built from frequency modulated continuous wave (FMCW) radar signals. A support tensor machine (STM) classifies each action from the spatial and temporal information in the point clouds.

## What I did

- Built 3D point clouds from FMCW radar data with 3D Capon beamforming, and subsampled them to cut computation without losing much accuracy.

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

- Classified the actions with an STM and looked through the misclassified cases to see where the model went wrong.

## Setup

- Radar: Texas Instruments IWR6843-ODS
- Actions: sitting, standing up, walking, raising hands, crouching
- Participants: 11 people, each performing every action 0.5 to 2 m from the radar

## Results

The STM reached **82% accuracy** on the five actions. Most errors came from actions whose movement patterns overlap, which is the first thing I'd work on next.

## Poster (in Korean)

<iframe src="/assets/pdf/IPIU2023_poster.pdf" width="100%" height="600px">
    Your browser does not support embedding PDFs. You can <a href="/assets/pdf/IPIU2023_poster.pdf">download the PDF here</a>.
</iframe>

## Takeaways

FMCW radar can recognize actions reasonably well, and unlike a camera it doesn't record anyone's face. It's also cheap. {% cite 2023IPIU %}

I also tried fall detection on the same 3D point clouds with RNN and LSTM models. The hardest part of every radar project was the same: collecting enough data. 😇
