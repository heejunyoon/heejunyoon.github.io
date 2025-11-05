---
layout: page
title: "Vital Sign Monitoring with FMCW Radar"
description: "A novel method for estimating breathing and heart rates using 3D beamforming radar signals."
date: 2022-11-01
category: research
importance: 5
img: assets/img/thumb_radarconf.png
related_publications: false
---

## Overview

This project explored a **novel approach for estimating breathing and heartbeat rates** using **3D beamforming-based frequency modulated continuous wave (FMCW) radar signals**.

## Key Contributions

- **3D Beamforming**:

  - Focused on different sections of the body for precise vital sign estimation.
  - Improved accuracy over traditional 2D methods in various experimental scenarios.

- **Vital Sign Estimation Framework**:

  - Proposed a method to separate and analyze breathing and heart signals using **Bartlett Beamforming**.
  - Conducted phase extraction and unwrapping to derive vital sign data.

- **Experimental Results**:
  - Validated the method on **seven human subjects**, demonstrating significant improvement in accuracy for both breathing and heart rate detection.

## Results

Our experiments showed:

- **Improved heart rate detection** using the proposed 3D beamforming over conventional 2D methods.
- Lower **Mean Absolute Error (MAE)** across varied scenarios.
- **Research Paper**: Submitted as a second author to an **IEEE conference**. Though rejected, the research showcased promising advancements in radar-based healthcare solutions.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/Radar_2.png" title="data image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/Radar_1.png" title="data image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample data📈
</div>
