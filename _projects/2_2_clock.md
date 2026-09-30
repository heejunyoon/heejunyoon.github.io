---
layout: page
title: Hexagonal Lattice IoT Clock
description: Memories of never-ending soldering...
img: assets/img/thumb_clock.png
importance: 2
category: fun
---

## Overview

I made an **LED clock with animations** for our club's 2020 exhibition. It is based on the RGB HexMatrix IoT Clock project on Instructables.

## How I built it

- A **WeMos D1 mini Pro** drives a **WS2812 LED strip**.
- I modeled the frame in **Fusion 360** and 3D printed it.
- The clock and the LED animations are programmed in Arduino.

## Results

The clock was shown at the 2020 club exhibition, keeping time and playing animations.

## Behind the scenes

There was a lot of soldering.
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/DDR_while2.jpg" title="while image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/DDR_while1.jpg" title="while image" class="img-fluid rounded z-depth-1" style="image-orientation: from-image;" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proj/DDR_fail.jpg" title="wrong image" class="img-fluid rounded z-depth-1" style="image-orientation: from-image;" %}
    </div>
</div>
<div class="caption">
    I worked overnight, and something went wrong 🤦
</div>

<div class="row">
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/clock_mid.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Working...</p>
  </div>  
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/clock_end_back.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Finally!</p>
  </div>
</div>
<div class="caption">
    I started all over again, and finally it worked 😇
</div>

Demo video:
<video width="640" height="360" controls>
  <source src="/assets/video/clock_demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
