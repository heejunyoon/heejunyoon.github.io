---
layout: page
title: "AI-JAM Korea 2020: NLP-Based YouTube Comment Analysis"
description: Gold Medal for an NLP model that clusters real YouTube comments
img: assets/img/proj/AIJAM_3.png
importance: 6
category: fun
date: 2020-08-01
---

## Overview

At **AI-JAM Korea 2020**, our team built a system that clusters YouTube comments with natural language processing. We won the **Gold Medal**.

## What we did

- Scraped real comments from YouTube with Python.
- Tokenized the Korean text with KoNLPy, embedded it with FastText, and trained clustering models in TensorFlow.

I worked on the overall algorithm, wrote the scraper and the tokenization, and gave the final presentation.

## Code

The code is on <a href="https://github.com/ottlseo/AI-JAM_KOREA_2020" target="_blank"><i class="fab fa-github"></i> **GitHub**</a>.

## Results

Gold Medal at AI-JAM Korea 2020.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj/AIJAM_1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Nouns from each comment embedded as 300-dimensional vectors
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj/AIJAM_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Final clusters, reduced with t-SNE and plotted with Bokeh
</div>
