---
layout: project
type: project
image: img/growing-islands/islands.jpeg
title: "Shoreline Detection for the Growing Islands Project"
# All dates must be YYYY-MM-DD format!
date: 2025-12-01
published: true
labels:
  - Machine Learning
  - Computer Vision
  - Geospatial Foundation Models
  - Remote Sensing
  - Python
  - PyTorch
summary: "Fine tuning NASA and IBM's Prithvi-EO-2.0 geospatial foundation model to delineate shorelines of small sandy islands from Sentinel-2 satellite imagery, in support of MIT's Growing Islands project on sea level rise."
---

<img class="img-fluid" src="../img/growing-islands/islands.jpeg"

## Overview

I have been a research collaborator at MIT's [Self-Assembly Lab](https://selfassemblylab.mit.edu/) since October 2023, working on the [Growing Islands](https://selfassemblylab.mit.edu/growing-islands) project. The lab strategically places geometric structures underwater around Maldivian islands to encourage natural sand accumulation, forming sandbars that can help coastlines resist erosion and sea level rise. Deciding where to place structures depends on understanding how shorelines have shifted over years and decades, which means we need reliable ways to extract shorelines from satellite imagery.

That turns out to be hard. Existing toolkits like CoastSat and CoastSeg were built for larger, more typical coastlines, and they struggle to distinguish a small sandy island from the atoll it sits on. Modern general purpose models like SAM and YOLO cannot ingest the multispectral bands that make satellite imagery so information rich. And the imagery that is affordable and covers a long enough time range is low resolution (10m or 30m per pixel), which makes the problem harder still.

My work focuses on closing that gap using geospatial foundation models.

## What I built

I fine tuned NASA and IBM's Prithvi-EO-2.0 foundation model (both the 300M and 600M parameter versions) for shoreline segmentation on small Maldivian islands, and evaluated how the model performs as the training set shrinks, which matters a lot for real world coastal monitoring, where labeled data is scarce.

Key pieces of the project:

- Dataset. I curated and hand labeled 225 multispectral Sentinel-2 images of two Maldivian islands (Fuvahmulah and Madhirivaadhoo), tracing shorelines in Kili Technology to produce land/water masks. The dataset is publicly released [on GitHub](https://github.com/tishyac3141/Maldives-Image-Segmentation-Sentinel-2-Dataset).
- Fine tuning. I froze the Vision Transformer backbone and trained a U-Net style decoder head on top, using AdamW, bfloat16 mixed precision, and cross entropy loss on a single GPU. To study data efficiency, I fine tuned separate models on training subsets of 5, 10, 25, 50, 75, 100, 125, 150, and 181 images.
- Evaluation. All models were tested on the same 22 image held out set, measured by F1 and IoU.

## Results

Prithvi transferred remarkably well to this task, even with very little labeled data:

- With only 5 training images, the 300M model still hit F1 = 0.96 and IoU = 0.85.
- Peak performance was F1 ≈ 0.99 and IoU ≈ 0.96 at 125 training images.
- The 600M model performed only marginally better than the 300M one, suggesting the extra compute is not worth it for this task.

Practically, this means shoreline monitoring in regions with limited labeled data (like small island nations) does not require large labeled datasets or expensive high resolution imagery, a meaningful shift for the accessibility of geospatial AI in climate applications.

## Publications

Tishya Chhabra, Manisha Bajpai, Walter Zesk, Skylar Tibbits. *Utilizing a Geospatial Foundation Model for Coastline Delineation in Small Sandy Islands.* Tackling Climate Change with AI Workshop at NeurIPS 2025. [Paper (arXiv)](https://arxiv.org/pdf/2511.10177) · [CCAI page](https://www.climatechange.ai/papers/neurips2025/93) · [Poster (PDF)](https://ccai-papers.s3.us-east-1.amazonaws.com/neurips2025/93/poster.pdf)

Tishya Chhabra, Walter Zesk, Skylar Tibbits. *Utilizing a Geospatial Foundation Model for Shoreline Detection in Small Sandy Islands.* Fragile Earth AI Workshop at ACM KDD 2025. [Paper (PDF)](https://ai4good.org/wp-content/uploads/2025/08/4.pdf)

## Talk

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%;">
  <iframe src="https://slideslive.com/embed/presentation/39052607" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;" frameborder="0" allowfullscreen scrolling="no" allow="autoplay; encrypted-media; fullscreen"></iframe>
</div>

I also presented this work at Coastal GeoTools 2025 (*Novel AI Models for Shoreline Detection*) to an audience of coastal professionals from NOAA, FEMA, and USGS, and assisted in a related presentation of the Growing Islands project to the UN General Assembly in New York in September 2024.

## Collaborators

Manisha Bajpai, Walter Zesk (MIT), and Skylar Tibbits (MIT Self-Assembly Lab).

## Links

- Dataset: <a href="https://github.com/tishyac3141/Maldives-Image-Segmentation-Sentinel-2-Dataset"><i class="large github icon"></i>tishyac3141/Maldives-Image-Segmentation-Sentinel-2-Dataset</a>
- Growing Islands project: [selfassemblylab.mit.edu/growing-islands](https://selfassemblylab.mit.edu/growing-islands)