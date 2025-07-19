---
layout: essay
type: essay
title: "A SAR-based flood mapping approach: application of SAR-SIFT registration and modified DeepLabV3 segmentation in flood hazard assessment"
# All dates must be YYYY-MM-DD format!
date: 2025-06-17
published: true

labels:
  - Image semantic segmentation
  - SAR
  - Deep learning
  - Flooded area
---

Zhang, Z., Xiong, J., Li, X., Li, Y., & Liu, J. (2025). A SAR-based flood mapping approach: application of SAR-SIFT registration and modified DeepLabV3 segmentation in flood hazard assessment. Geocarto International, 40(1), 2512188.

[Article Link](https://doi.org/10.1080/10106049.2025.2512188)


1. [The highlight of this article](#1-the-highlight-of-this-article)
2. [Study area and dataset](#2-study-area-and-dataset)
3. [Methods](#3-methods)
4. [Results](#4-results)

## 1. The highlight of this article
* Proposes an automated, high-resolution flood mapping framework using SAR satellite imagery, SIFT feature-based registration, and a modified DeepLabV3+ deep learning segmentation model.

* Demonstrates that the model is effective in detecting flood extents even in complex urban and vegetation-covered environments, outperforming traditional unsupervised methods.

* The approach provides timely and accurate flood hazard assessment that can assist in emergency response and planning.

## 2. Study area and dataset
<img class="img-" src="{{ site.baseurl }}/img/floodsar2025/floodsar_sa.jpg" style="width: 60%; height: auto;">

Study Area: Hainan Province, China, which experienced severe flooding from August 29 to September 1, 2022.

Focused on areas affected by Typhoon Ma-on, including both urban and agricultural zones.

Data Sources:

Sentinel-1 SAR imagery: Dual-temporal VV polarization (10 m resolution), pre-flood (August 23) and post-flood (August 31) scenes, sourced from ESA Copernicus Open Access Hub.

Sentinel-2 optical imagery: Used for reference and labeling.

Land cover data from the Chinese Academy of Sciences (CLCD).

Manual labeling of flooded areas based on Sentinel-2 images and field knowledge, used to create ground truth masks.

## 3. Methods
<img class="img-" src="{{ site.baseurl }}/img/floodsar2025/floodsar_framework.jpg" style="width: 60%; height: auto;">

The proposed SAR-based flood mapping framework includes:

1. SAR-SIFT Image Registration:

SAR-SIFT algorithm used for co-registration of multi-temporal SAR images.

Improves alignment accuracy and maintains local details better than conventional correlation-based approaches.

2. Modified DeepLabV3+ Model:

DeepLabV3+ with a ResNet-101 backbone is modified to handle binary segmentation of flooded vs. non-flooded areas.

Input: dual-temporal SAR image composites (pre-flood + post-flood).

Ground truth masks are generated from manual interpretation of Sentinel-2 and FEMA data.

Model trained with data augmentation and evaluated using precision, recall, F1-score, and IOU metrics.

3. Comparison with Unsupervised Methods:

Benchmarked against change detection techniques (e.g., logarithmic ratio, histogram thresholding).

Also compared to raw DeepLabV3+ without SAR-SIFT registration.

## 4. Results

SAR-SIFT Performance:

Achieved better co-registration accuracy than OpenCV and ENVI methods, with lower RMSE and misalignment.

Flood Segmentation Accuracy:

The modified DeepLabV3+ model with SAR-SIFT registered inputs achieved:

F1-score: 0.853, IOU: 0.743

Outperformed unsupervised methods (e.g., F1-score of histogram thresholding ~0.4).

Visual Accuracy:

The deep learning-based method produced flood maps that aligned better with FEMA boundaries, including in urban areas and complex terrains.

Generalizability:

The workflow is modular and scalable to other regions and flood events using SAR imagery.

<img class="img-" src="{{ site.baseurl }}/img/floodsar2025/floodsar_trainning.jpg" style="width: 60%; height: auto;">

<img class="img-" src="{{ site.baseurl }}/img/floodsar2025/floodsar_comp.jpg" style="width: 60%; height: auto;">
