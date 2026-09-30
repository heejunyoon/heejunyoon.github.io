---
layout: page
title: "Deep Learning-Based Semiconductor Product Inspection"
description: "My M.S. thesis: a lightweight twin network that finds defects on IC substrates in real time."
date: 2024-06-01
category: research
importance: 3
img: assets/img/thumb_thesis.PNG
related_publications: true
bibliography: [thesis]
---

## Overview

For my master's thesis {% cite thesis %}, I built a **lightweight twin network that detects defects on IC substrates**. It needed to stay accurate when the test and reference images are slightly misaligned or differ in color, and it needed to be fast enough for a real inspection line.

## The problem

IC substrates have repeating patterns, so you can find defects by comparing a test image with a reference image and looking for changes. Twin (Siamese) networks, which run the same encoder on both images and compare the features, are the usual tool for this kind of change detection. They have two weak points here:

- Small misalignments between the two images (mis-registration) and differences in color or brightness show up as fake changes, and those make tiny real defects hard to spot.
- Fixes such as co-attention modules take a lot of memory and time, which rules them out on a factory floor.

<div class="row justify-content-center">
  <div class="col-auto">
    {% include figure.liquid path="assets/img/publication_preview/thesis_CCTSNet.png" title="Image 1" class="img-fluid" %}
  </div>
  <div class="col-auto">
    {% include figure.liquid path="assets/img/publication_preview/thesis_coatt.png" title="Image 2" class="img-fluid" %}
  </div>
</div>
<div class="caption">
    Proposed network structure - C-CTSNet and ch-co-att module
    
</div>

## What I proposed

- **C-TSNet**, which combines a twin network with a single network. Merging the two decoders' outputs makes the model less sensitive to mis-registration and color differences while keeping latency low.
- **CC-TSNet**, which adds a channel co-attention module to C-TSNet so it copes better with characteristic differences between the images.

<div class="row justify-content-center">
  <div class="col-md-5">
    {% include figure.liquid path="assets/img/publication_preview/thesis_rep.png" title="Image 1" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-md-5">
    {% include figure.liquid path="assets/img/publication_preview/thesis_pseudo.png" title="Image 2" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Example IC substrates, and samples from the dataset with registration errors and characteristic differences 🕵️
    
</div>

## Tools

TensorFlow and PyTorch on NVIDIA GPUs. Techniques: Siamese (twin) networks, change detection, attention.

## Results

- On a real industrial IC substrate dataset, both models had higher F1 scores and fewer false positives than U-Net and a baseline twin network.
- The channel co-attention module cut false positives caused by characteristic differences.
- Accuracy was close to the heavier module-based methods at about one third of their latency, fast enough for a production line.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/thesis_logit1.png" title="result image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qualitative results. Merging the logits of the single decoder and the twin decoder reduces errors caused by misalignment.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/thesis_logit2.png" title="result image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Qualitative results. C-TSNet alone could not fix these errors, but adding the channel co-attention module did.
</div>

## Things that didn't make it into the thesis

- I tried knowledge distillation and Vision Transformers (ViT). Neither worked well for this inspection problem.
- Some products don't have repeating patterns, so there is no reference image to compare against. I tried to improve a single ViT-based network for that case. It didn't get the results I wanted, but it showed me how much harder defect detection is without a reference. I'd like to come back to it someday.
- I labeled more than 100,000 images for this project. 🤪
