---
layout: page
title: Brand Logo Detection in Social Media Images
description: Created a novel dataset and evaluated computer vision models for robust brand logo detection in cluttered social media environments.
img: /assets/img/Logo_page.jpg
importance: 1
category: Academic Research
---

**TL;DR:** Constructed a comprehensive social-media-focused logo detection dataset (VRL-SM-Logo) and demonstrated that models trained on highly diverse social media imagery achieve superior cross-domain generalization compared to standard benchmark datasets.

<div class="text center">
    <img src="/assets/img/Logo_page.jpg" style="width: 60%; max-width: 600px;">
</div>

### Technologies & Methodology
* **Models & Architecture:** DINOv3-ConvNext-Large backbone paired with a DETR (DEtection TRansformer) detection head.
* **Algorithms & Statistical Tools:** Weighted Box Fusion (WBF) for annotation aggregation, and Ordinary Least Squares (OLS) regression for behavioral analysis.
* **Datasets:** VRL-SM-Logo (custom dataset: 5,087 images, 9,731 logo instances across 25 brands) and FlickrLogos-27.
* **Annotation Tools:** CVAT (Computer Vision Annotation Tool).

### Key Contributions & Results
* Led the data collection and annotation pipeline, utilizing Weighted Box Fusion (WBF) to generate high-fidelity ground truth bounding boxes from multiple annotations.
* Conducted a systematic quality assurance analysis using OLS regression, revealing that annotator performance degrades significantly during late-night hours or in sessions exceeding 120 minutes.
* Trained a hybrid DINOv3+DETR object detection model to frame logo detection as a robust set-prediction problem.
* Executed a cross-dataset evaluation demonstrating that the model trained on the VRL-SM-Logo dataset suffered only a minimal performance drop (0.07 on AP@0.5:0.95) when tested on out-of-domain data, significantly outperforming the Flickr-trained model's generalization capabilities.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <a href="https://ieeexplore.ieee.org/document/11636669" class="btn z-depth-0" role="button" target="_blank">View on IEEE Xplore</a>
    </div>
</div>
