---
layout: page
title: "DIY Dance Dance Revolution Pad with Arduino"
img: assets/img/DDR.gif
importance: 1
category: fun
---

## Overview

I built a **Dance Dance Revolution (DDR)** pad with an **Arduino Leonardo**. The pad acts as a keyboard, so it works as a controller for DDR games on a computer.

The idea came from Mel Huang's DIY DDR tutorial on [Medium](https://medium.com/@melhuang_/building-a-diy-dance-dance-revolution-e136265bbbfc).

## How I built it

- The pad is MDF board with copper tape and aluminum bars. Each arrow (up, down, left, right) is a sensor wired to the Arduino Leonardo.
- The Leonardo can act as a USB keyboard, so the code reads the sensors and sends key presses with the `Keyboard.h` library.
- I played a lot of songs on it to test it and tuned the input until it felt responsive.

## Results

I made two pads so two people could play against each other. In fall 2019 we set them up in the Engineering Building, and professors and students played on them between classes. 🪩🕺

## Demo

**Videos**
<video width="640" height="360" controls>

  <source src="/assets/video/ddr_test.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<video width="640" height="360" controls>
  <source src="/assets/video/ddr_test2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

**Presentation**

You can read the slides below or [download the PDF](https://github.com/heejunyoon/heejunyoon.github.io/blob/main/assets/pdf/Making%20DDR%20%20HEEJUN%20YOON.pdf).

<iframe src="/assets/pdf/Making%20DDR%20%20HEEJUN%20YOON.pdf" width="100%" height="600px">
    This browser does not support PDFs. Please download the PDF to view it:
    <a href="/assets/pdf/Making%20DDR%20%20HEEJUN%20YOON.pdf">Download PDF</a>.
</iframe>
