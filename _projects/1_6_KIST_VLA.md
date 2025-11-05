---
layout: page
title: "LLM-Driven Embodied AI for Task Planning and Navigation"
description: "A hierarchical agent framework for long-horizon task execution in dynamic simulated environments."
date: 2025-07-01
category: research
importance: 1
img: assets/img/thumb_KIST_VLA.png
related_publications: false
---

## Overview

This is my primary postdoctoral research project, focusing on enabling embodied agents (in **Omnigibson**) to understand and execute complex, long-horizon human requests (e.g., "Tidy the house and take out the trash"). We are developing a **hierarchical planning framework** that integrates a high-level LLM "brain" with a low-level, spatially-aware VLM "agent" to bridge the gap between abstract commands and concrete physical actions.

## Objectives (Key Questions)

- **To enable long-horizon, multi-room navigation**: How can an agent efficiently navigate across multiple rooms to fulfill complex user requests that require several steps?
- **To build and utilize spatial "mental maps"**: How can the system build a spatial representation of the house from visual inputs to intelligently decompose tasks and plan efficient actions?
- **To decompose abstract tasks**: How can a high-level planner (LLM) effectively break down vague commands into a logical sequence of actionable sub-goals for the agent?

## Core Methodology
<div class="row justify-content-center">
  <div class="col-auto">
    {% include figure.liquid path="assets/img/proj/KIST_VLA.png" title="Hierarchical Framework Diagram" class="img-fluid" %}
  </div>
</div>
<div class="caption">
  Overview of the hierarchical planning framework: The LLM Planner (top) provides sub-goals, the Spatial Memory (left) stores a topological map, and the Spatially-Aware Agent (right) perceives and acts.
</div>

Our framework consists of three core components that work in a hierarchical loop:

- **1. High-Level Planner (LLM):** Decomposes the abstract user request into a logical sequence of sub-goals (e.g., `GOTO Bedroom`, `FIND Clothes`, `PLACE Clothes`).
- **2. Spatial Memory (Topological Graph):** Dynamically builds a graph of the environment where **nodes** are key waypoints (locations) stored with their visual embeddings, and **edges** are navigable paths. This enables the LLM to map semantic goals (e.g., "kitchen") to specific nodes.
- **3. Low-Level Policy (VLM + RL):**
    - Employs our **Spatially-Aware VLM** (foundational work) as the "eyes" for real-time scene perception.
    - An **RL Policy** executes low-level motor actions (e.g., `move`, `grasp`) to complete each sub-goal.
    - The agent reports task status (e.g., `Success`, `Failure`) to the LLM, which can then re-plan if necessary.

## Current Status & Next Steps

This project is currently in active development. We are implementing the topological graph memory and integrating the high-level LLM planner with the low-level VLM policy within the Omnigibson simulator. Our goal is to present this framework and its results at **RSS 2026**.