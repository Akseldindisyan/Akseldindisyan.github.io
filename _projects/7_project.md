---
layout: page
title: Parallelisation of ConTree
description: Parallelized ConTree, an optimal decision tree algorithm, utilizing OpenMP and CUDA for CPU and GPU acceleration.
img: /assets/img/Simple_decision_tree.jpg
importance: 2
category: Course Project
---

**TL;DR:** Analyzed the performance bottlenecks of the ConTree optimal decision tree builder and engineered a hybrid CPU/GPU parallelization strategy using OpenMP and CUDA to accelerate its processing of continuous numeric data.

{% include figure.liquid path="assets/img/Simple_decision_tree.jpg" class="img-fluid rounded z-depth-1" %}

### Technologies & Methodology
* **Software & Frameworks:** C++, OpenMP, NVIDIA CUDA, CMake.
* **Algorithms:** Optimal Decision Trees (ODT), Dynamic Programming, Branch-and-Bound (BnB).
* **Profiling Tools:** `perf`, CLion Profiler (WSL Environment).

### Key Contributions & Results
* Profiled the original ConTree implementation to identify that the specialized solver, specifically the depth-one linear data scan, consumed up to 97% of CPU time.
* Engineered a hybrid parallelization architecture leveraging OpenMP for multi-core task parallelism across search tree features and CUDA for high-throughput GPU data parallelism.
* Re-architected the host dataset memory layout into a flattened, contiguous Structure of Arrays (SoA) format and managed a CUDA stream queue (FIFO) to eliminate redundant `cudaMemcpy` overheads.
* Developed a 4-stage CUDA kernel (Local Histograms, Global Scan, Split Evaluation, Global Reduction) to rapidly evaluate optimal split thresholds directly on the GPU.
* Implemented dynamic thread allocation logic to optimize inner and outer threading configurations based on dataset instance size and available hardware resources.
* Successfully scaled execution across large datasets, demonstrating a significant reduction in computational latency for depth-two node searches.

***

### Reference
This project is an optimization and parallelization of the original ConTree algorithm introduced in:
> Briţa, Cătălin E., Jacobus G. M. van der Linden, and Emir Demirović. "Optimal Classification Trees for Continuous Feature Data Using Dynamic Programming with Branch-and-Bound." *In Proceedings of AAAI-25* (2025). <a href="https://arxiv.org/pdf/2501.07903" target="_blank">[View PDF on arXiv]</a>
