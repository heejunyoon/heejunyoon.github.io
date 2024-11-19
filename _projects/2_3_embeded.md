---
layout: page
title: Gesture-Based Servo Control System
description: "Developed a system to control servo motors based on predefined gestures using gyro sensors and wireless communication modules"
img: assets/img/thumb_embeded.png
importance: 3
category: fun
---

## Overview

This project focused on designing and implementing a **gesture-based servo control system**. It aimed to improve smart factory automation by recognizing specific gestures and wirelessly transmitting motion data for real-time monitoring.

## Transmit and Receive Workflow

### 1. **Transmit (Sender) Part**

- **Components**:

  - **Touch Sensor**: Detects user input and triggers data transmission.
  - **Gyro Sensor (MPU6050)**: Measures acceleration and angular velocity for specific gestures.
  - **XBee Module**: Transmits the processed data to the receiver.

- **Process**:
  1. The user performs a gesture detected by the **gyro sensor**.
  2. The **touch sensor** confirms gesture completion.
  3. Data is packaged and sent via **XBee** to the receiver.

### 1. **Receive (Receiver) Part**

- **Components**:

  - **XBee Module**: Receives data transmitted by the sender.
  - **LCD Display**: Visualizes the recognized gesture and corresponding motor action.
  - **Servo Motors**: Executes actions based on the received data.

- **Process**:
  1. The **XBee receiver** module captures data.
  2. The system processes incoming data to classify gestures.
  3. Results are displayed on the **LCD** and executed by **servo motors**.

## Key Contributions

- Developed a system for **recognizing 8 predefined gestures** using **gyro sensors** and controlled servo motors based on these inputs.
- Utilized **XBee wireless communication** to transmit data between the sender and receiver units.
- Designed a system to visualize motion patterns on an LCD based on real-time sensor input.

## Tools and Technologies

- **Arduino Zero**: For controlling servo motors and integrating sensors.
- **MPU6050 Gyro Sensor**: Used for motion detection and analysis.
- **XBee Modules**: Enabled wireless communication between devices.
- **MATLAB**: For data preprocessing and visualization.

## Demo and Documentation

-- **demo**

- total
<video width="640" height="360" controls>
  <source src="/assets/video/embedded_total.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
- receive & transmit part
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

-- **presentation**
You can view the documentation below or [download the PDF(in Korean)](https://github.com/heejunyoon/heejunyoon.github.io/blob/main/assets/pdf/Final_project_report_embedded.pdf).

<iframe src="/assets/pdf/Final_project_report_embedded.pdf" width="100%" height="600px">
    This browser does not support PDFs. Please download the PDF to view it:
    <a href="/assets/pdf/Final_project_report_embedded.pdf"> Team Report written in Korean</a>.
</iframe>

## Results

- This project demonstrated the feasibility of using **wireless gesture control** for smart factories, reducing human intervention while maintaining high accuracy in servo motor control.
- Future improvements could include:
  - Enhanced classification algorithms using machine learning.
  - Self-contained gesture detection without requiring touch sensor validatio
