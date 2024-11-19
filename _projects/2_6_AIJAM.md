---
layout: page
title: "AI-JAM Korea 2020: NLP-Based YouTube Comment Analysis"
description: Awarded Gold Medal for developing an NLP model to cluster real-world YouTube comments
img: assets/img/proj/AIJAM_3.png
importance: 6
category: fun
date: 2020-08-01
---

## Overview

This project was part of the **AI-JAM Korea 2020 Competition**, where we developed a system to analyze and cluster YouTube comments using **Natural Language Processing (NLP)** techniques. Our team won the **Gold Medal** for this project.

## Key Contributions

- **Data Collection**:
  - Leveraged **Python** for web scraping to gather real-world comment data from **YouTube**.
- **NLP Model Development**:

  - Applied **tokenization**, **embedding techniques (FastText)**, and other NLP methods to build clustering models.
  - Used **TensorFlow** for model training and **Konlpy** for processing Korean text.

- **Team Role**:
  - Played a pivotal role in constructing the overall algorithm.
  - Focused on key project components such as web scraping, tokenization, and delivering the final presentation.

## Tools and Technologies

- **Python**: For web scraping and algorithm development.
- **TensorFlow**: For training the clustering models.
- **Konlpy**: For Korean language processing.
- **FastText**: For word embeddings.

## GitHub Repository

The complete project and its codebase are available on [GitHub](https://github.com/ottlseo/AI-JAM_KOREA_2020).

## Results

- **Gold Medal**: Awarded in the **AI-JAM Korea 2020 Competition** for outstanding project execution and innovation in NLP-based YouTube comment analysis.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj/AIJAM_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The result of embedding the nouns in a sentence into a 300-dimensional vector
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj/AIJAM_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Final result with dimensionality reduction using TSNE and visualization using Bokeh module
</div>
