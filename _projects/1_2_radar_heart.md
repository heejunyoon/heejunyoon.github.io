---
layout: page
title: "Vital Sign Monitoring with FMCW Radar"
description: "Estimating breathing and heart rates with 3D beamforming on FMCW radar signals."
date: 2022-11-01
category: research
importance: 5
img: assets/img/thumb_radarconf.png
related_publications: false
---

## Overview

We estimated breathing and heart rates from frequency modulated continuous wave (FMCW) radar signals, using **3D beamforming** to focus on specific parts of the body.

## Method

- 3D Bartlett beamforming points the radar at different sections of the body so breathing and heartbeat signals can be separated.
- From each focused signal we extracted and unwrapped the phase to get the vital sign waveform.

## Results

We tested the method on **seven people**. Compared with conventional 2D beamforming, 3D beamforming gave lower mean absolute error for both heart rate and breathing rate across our test scenarios.

I was second author on a paper about this work. We submitted it to an IEEE conference and it was rejected, but I still learned a lot from it about radar signal processing.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/Radar_2.png" title="data image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/Radar_1.png" title="data image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample data 📈
</div>
