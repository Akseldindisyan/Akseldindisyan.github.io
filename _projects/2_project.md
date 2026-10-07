---
layout: page
title: Autonomous Vehicle 3D Vision Detection
description: Deployed the BEVFusion hybrid camera-LiDAR object detection model for Ford Otosan's ADAS team.
img: assets/img/BEVFUSION Diagram.png
importance: 2
category: Internship
---

**TL;DR:** Evaluated and deployed the BEVFusion 3D vision detection algorithm for the Advanced Driver-Assistance Systems (ADAS) team at Ford Otosan.

![BEVFusion Inference](assets/img/BEVFUSION Inference.jpg)

### Technologies & Methodology
* **Hardware:** NVIDIA T4 GPU, Google Cloud Virtual Machines, and remote SSH servers.
* **Software & Frameworks:** Python, Nvidia Toolkit 11.1, TensorRT, and Netbird.
* **Algorithms & Datasets:** BEVFusion (hybrid camera and LiDAR inputs), nuScenes (v-1.0 mini) dataset.

### Key Contributions & Results
* Conducted an extensive literature review covering monocular, stereo, multi-camera, and fusion-based 2D and 3D vision detection architectures.
* Resolved library dependency conflicts and repaired repository code to successfully execute BEVFusion inference for 3D object detection and Bird-Eye-View (BEV) map segmentation.
* Overcame local GPU memory constraints by configuring a remote SSH connection via Netbird and deploying a Google Cloud virtual machine to process the models.
* Authored comprehensive technical documentation detailing the inference pipeline, visualization steps, and troubleshooting procedures for CUDA and TensorRT acceleration.

<a href="{{ '/assets/pdf/CS395_FinalReport_Aksel_Dindisyan_30September2025_Internship1.pdf' | relative_url }}" class="btn z-depth-0" role="button" target="_blank">Download Full Internship Report (PDF)</a>
