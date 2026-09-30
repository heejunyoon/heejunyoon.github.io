---
layout: page
title: "LLM-Driven Embodied AI for Task Planning and Navigation"
description: "Why vision-language-action models lose track of long instructions, and a lightweight way to make them listen (KIST)."
date: 2025-07-01
category: research
importance: 1
img: assets/img/thumb_KIST_VLA.png
related_publications: false
---

## Overview

At KIST I worked on embodied agents in the **OmniGibson** simulator that carry out long, multi-step requests such as "Tidy the house and take out the trash." We started from the hierarchical framework in the figure below. I only built part of it, and I never used the RL component. Most of my time went into one problem that showed up early: the vision-language-action (VLA) model stopped following instructions once tasks got long.

<div class="row justify-content-center">
  <div class="col-auto">
    {% include figure.liquid path="assets/img/proj/KIST_VLA.png" title="Hierarchical Framework Diagram" class="img-fluid" %}
  </div>
</div>
<div class="caption">
  The full framework we planned: an LLM planner gives sub-goals, a spatial memory stores a topological map, and a spatially aware agent perceives and acts. I worked on part of it; the RL policy was never used.
</div>

## What went wrong

Two failure modes kept coming up when I ran the VLA model on long tasks:

- **It lost the plot.** Once a task ran for many steps, the model had no idea what to do next.
- **It ignored the instruction.** The model had memorized the training scenes. It did what it had seen in that scene before, whatever the instruction actually asked.

## What I did about it

Fully fine-tuning the VLA model was too expensive to be realistic, so I aimed for the smallest change that would make the model pay attention to the instruction. Most of the work was on the data side:

- I generated new training data where the same scene comes with different instructions, so the model can't get by on memorizing the scene.
- I split long tasks into shorter segments, each tied to its own sub-instruction.
- I brought in ideas from task planning, so a long request is decomposed into steps before the policy runs, instead of asking the policy to handle the whole thing in one go.

## Status

The project was not published. What I took away from it is that long-horizon failures in these models often come from the data: if the scene alone predicts the action, the model has no reason to read the instruction.
