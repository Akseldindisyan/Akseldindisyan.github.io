---
layout: page
title: Explainable HPC Optimization for Container Terminals
description: Optimized continuous berth allocation (BAP) and container stacking (CSP) to address the operational needs of a commercial port.
img: /assets/img/Port.jpeg
importance: 1
category: Capstone Project
---

**TL;DR:** Built a berth allocation system utilizing Dynamic Programming and OpenMP-parallelized heuristics, alongside a container stacking pipeline powered by an Optuna-optimized XGBRanker model and custom stacking algorithms to minimize reshuffles.

{% include figure.liquid path="assets/img/Port.jpeg" class="img-fluid rounded z-depth-1" %}


### Technologies & Methodology
- **Software & Frameworks:** C++, Python, Optuna, scikit-learn, OpenMP, CMake.
- **Algorithms (BAP):** Dynamic Programming, Random Restart Hill Climbing, Stochastic Local Beam Search.
- **Machine Learning (CSP):** Siamese Neural Networks, XGBoost Binary Classifier, XGBRanker, RankCosine, ListNet, ListMLE.

### Key Contributions & Results

**Part 1: Berth Allocation Problem (HPC & Operations Research)**
- Engineered a Dynamic Programming solver capable of finding optimal berth allocations for small port instances, achieving execution times under one second (0.77s) for a 20-vessel horizon.
- Compressed the algorithmic state space using a Greatest Common Divisor (GCD) bollard grouping technique, reducing the state dimension by up to 80%.
- Implemented branch-and-bound and dominance pruning to bypass redundant computations and discard inferior port configurations in constant time.
- Developed and OpenMP-parallelized heuristic alternatives, including Random Restart Hill Climbing and Stochastic Local Beam Search, to rapidly evaluate large state spaces.

**Part 2: Container Stacking Problem (AI & Data Science)**
- Engineered a comprehensive data processing pipeline for port movement records, uniquely modeling container dwell time prediction as pairwise and listwise ranking problems rather than standard regression.
- Trained multiple predictive models (including PyTorch-based Siamese Networks and tree-based models) to determine optimal container exit sequences.
- Selected XGBRanker as the premier model and applied Bayesian optimization via Optuna for hyperparameter tuning, achieving a highly accurate Normalized Discounted Cumulative Gain (NDCG) score of 0.9132.
- Designed a "Minimum Gap" heuristic stacking algorithm that, when paired with the XGBRanker predictions, successfully reduced unproductive crane reshuffling operations by 13% compared to baseline port methods.
