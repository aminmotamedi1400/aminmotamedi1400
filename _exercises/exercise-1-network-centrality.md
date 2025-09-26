---
layout: exercise # We will create this layout in the next step.
title: "Exercise 1: Network Centrality"
date: "2025-10-01"
file: "/assets/files/ex1.ipynb"
description: "An introduction to degree, betweenness, and closeness centrality."
---

## Overview
In this exercise, you will explore the concept of **network centrality** — a set of measures that indicate the importance of nodes within a network.  
We will focus on three major types of centrality used in social network analysis:

1. **Degree Centrality** – Measures the number of direct connections a node has.
2. **Betweenness Centrality** – Identifies nodes that act as bridges between different parts of the network.
3. **Closeness Centrality** – Reflects how close a node is to all other nodes in the network.

---

## Objectives
By completing this exercise, you will be able to:
- Calculate degree, betweenness, and closeness centrality for given networks.
- Compare the different measures and understand in which scenarios each is most relevant.
- Visualize centrality values to gain insights into network structure.

---

## Tasks
1. Load a sample social network dataset (provided as `.ipynb`).
2. Compute **degree centrality** for all nodes.
3. Compute **betweenness centrality** and identify nodes with highest values.
4. Compute **closeness centrality** and analyze the spread of values.
5. Plot the network and color nodes based on centrality scores.

---

## Submission Guidelines
- Submit your completed Jupyter Notebook (`.ipynb`) with all code cells executed.
- Include explanations and interpretations for your results.
- Plots should be clear and well-labeled.

---

**Due Date:** October 1, 2025

---
> _Tip:_ Remember, centrality measures are often normalized. Make sure you check the documentation of your chosen library (NetworkX or similar) to understand the scaling.