---
layout: page
title: Gesture-Based Servo Control System
description: "Controlling servo motors with hand gestures, using a gyro sensor and wireless XBee modules"
img: assets/img/thumb_embeded.png
importance: 3
category: fun
---

## Overview

For this team project, we built a system that recognizes hand gestures and uses them to control servo motors over a wireless link. We had smart factory automation in mind: a worker makes a gesture, a machine moves, and a display shows what happened.

## How it works

#### 1. Sender

- A **gyro sensor (MPU6050)** measures acceleration and angular velocity while the user makes a gesture.
- A **touch sensor** marks the end of the gesture.
- An **XBee module** sends the data to the receiver.

#### 2. Receiver

- An **XBee module** receives the data.
- The system classifies the gesture from the incoming data.
- An **LCD** shows the recognized gesture, and the **servo motors** perform the matching action.

## What we built

- Recognition of 8 predefined gestures from the gyro sensor
- Wireless XBee link between the sender and the receiver
- An LCD view of the motion pattern, updated in real time from the sensor

## Tools

Arduino Zero, MPU6050 gyro sensor, XBee modules, and MATLAB for preprocessing and plotting the sensor data.

## Demo and documentation

**Full demo**

<video width="640" height="360" controls>
  <source src="/assets/video/embedded_total.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

**Receiver and sender**

<div class="row">
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/embedded_receive.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Receive</p>
  </div>
  <div class="col-lg-6">
    <video width="100%" controls>
      <source src="/assets/video/embedded_transmit.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <p class="text-center">Transmit</p>
  </div>
</div>

**Report**

You can read our team report below or [download the PDF (in Korean)](https://github.com/heejunyoon/heejunyoon.github.io/blob/main/assets/pdf/Final_project_report_embedded.pdf).

<iframe src="/assets/pdf/Final_project_report_embedded.pdf" width="100%" height="600px">
    This browser does not support PDFs. Please download the PDF to view it:
    <a href="/assets/pdf/Final_project_report_embedded.pdf">Team report (in Korean)</a>.
</iframe>

## Results

The system recognized the gestures and moved the servos as intended over the wireless link, which suggested gesture control could work for simple factory tasks. Next steps would be a machine learning classifier for the gestures and detecting the end of a gesture automatically, without the touch sensor.
