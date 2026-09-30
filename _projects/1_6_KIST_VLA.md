---
layout: page
title: "LLM-Driven Embodied AI for Task Planning and Navigation"
description: "A hierarchical LLM + VLM agent for long, multi-step tasks in simulated homes (KIST)."
date: 2025-07-01
category: research
importance: 1
img: assets/img/thumb_KIST_VLA.png
related_publications: false
---

## Overview

This was my main project at KIST. The goal was to let an embodied agent in the **OmniGibson** simulator carry out long, multi-step requests such as "Tidy the house and take out the trash." We built a hierarchical framework: an LLM plans at a high level, and a spatially aware VLM agent perceives the scene and acts.

## Questions

- How can an agent move efficiently through several rooms to finish a request that takes many steps?
- How can the system build a spatial map of the house from what it sees, and use that map to plan?
- How can an LLM planner break a vague command into sub-goals the agent can actually carry out?

## Method
<div class="row justify-content-center">
  <div class="col-auto">
    {% include figure.liquid path="assets/img/proj/KIST_VLA.png" title="Hierarchical Framework Diagram" class="img-fluid" %}
  </div>
</div>
<div class="caption">
  The hierarchical framework. The LLM planner (top) gives sub-goals, the spatial memory (left) stores a topological map, and the spatially aware agent (right) perceives and acts.
</div>

The framework has three parts that run in a loop:

1. **High-level planner (LLM).** It turns the user's request into a sequence of sub-goals, for example `GOTO Bedroom`, `FIND Clothes`, `PLACE Clothes`.
2. **Spatial memory (topological graph).** Nodes are waypoints stored with their visual embeddings, and edges are paths the agent can travel. The LLM uses the graph to map a goal like "kitchen" to a specific node.
3. **Low-level policy (VLM + RL).** Our spatially aware VLM from the [earlier project](/projects/1_5_KIST_VLM/) handles perception. An RL policy runs motor actions such as `move` and `grasp`. The agent reports `Success` or `Failure` back to the LLM, which re-plans when needed.

## Status

While I was at KIST, we were implementing the topological graph memory and connecting the LLM planner to the VLM policy inside OmniGibson.
