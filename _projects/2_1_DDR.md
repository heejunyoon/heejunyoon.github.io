---
layout: page
title: "DIY Dance Dance Revolution Pad with Arduino"
img: assets/img/DDR.gif
importance: 1
category: fun
---

## Overview

This project focused on building a custom **Dance Dance Revolution (DDR)** pad using **Arduino Leonardo**. The pad is designed to function as a controller for DDR gameplay by simulating keyboard inputs.

This project originally drew inspiration from the _DIY Dance Dance Revolution tutorial_ by Mel Huang, detailed in their Medium article.
https://medium.com/@melhuang_/building-a-diy-dance-dance-revolution-e136265bbbfc

## Key Contributions

- **Hardware Design**:
  - Built the DDR pad structure using MDF boards, copper tape, and aluminum bars.
  - Integrated sensors for directional inputs (up, down, left, right) and connected them to the Arduino Leonardo.
- **Programming**:

  - Wrote custom Arduino code to simulate keyboard input based on sensor readings.
  - Utilized the **Keyboard.h** library to map DDR pad inputs to corresponding keyboard keys.

- **Testing and Debugging**:
  - Verified functionality through various gameplay scenarios and refined input responsiveness.

## Tools and Technologies

- **Arduino Leonardo**: Used for its ability to act as a keyboard.
- **C++**: For programming the microcontroller.
- **MDF Board, Copper Tape, Aluminum Bars**: For constructing the DDR pad.

## Results

- Successfully created a functional DDR pad that responds to gameplay inputs.
- Demonstrated the project via an operating video showcasing its real-time performance.

## Final Thoughts

The project highlights a blend of hardware engineering and programming to create an interactive gaming experience. It was a hands-on exploration of integrating physical computing with game design.

## Additional Resources

-- **Demo Video**
<video width="640" height="360" controls>

  <source src="/assets/video/ddr_test.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<video width="640" height="360" controls>
  <source src="/assets/video/ddr_test2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

-- **presentation**

## Project Documentation

You can view the documentation below or [download the PDF](https://github.com/heejunyoon/heejunyoon.github.io/blob/main/assets/pdf/Making%20DDR%20%20HEEJUN%20YOON.pdf).

<iframe src="/assets/pdf/Making%20DDR%20%20HEEJUN%20YOON.pdf" width="100%" height="600px">
    This browser does not support PDFs. Please download the PDF to view it:
    <a href="/assets/pdf/Making%20DDR%20%20HEEJUN%20YOON.pdf">Download PDF</a>.
</iframe>

<iframe src="https://drive.google.com/file/d/1tkShXQXaufW7aBE3u6YjHifgKB05DoqL/preview" width="640" height="480"></iframe>
