# IUGC Video Dataset

## Overview

The **IUGC Video Dataset** is used in the **Explainable Ensemble Fetal Health** project for fetal ultrasound video analysis.

The dataset contains fetal ultrasound video data that can be used to study fetal structures and ultrasound patterns across multiple video frames.

## Purpose

The dataset is used for:

- Fetal ultrasound video analysis
- Frame extraction
- Video-based classification
- Temporal information analysis
- Deep learning experiments
- Model evaluation

## Dataset Information

| Property | Details |
|---|---|
| Dataset Type | Ultrasound Video |
| Modality | Fetal Ultrasound |
| Data Type | Video |
| Main Task | Video / Frame Analysis |
| Application | Fetal Ultrasound Analysis |

## Video Processing Workflow

```text
Ultrasound Video
       |
       v
Frame Extraction
       |
       v
Image Preprocessing
       |
       v
Feature Extraction
       |
       v
Deep Learning Model
       |
       v
Frame / Video Prediction
       |
       v
Ultrasound Analysis
```
<img width="572" height="342" alt="image" src="https://github.com/user-attachments/assets/4601796e-1676-4c12-8c3e-0e06c0a80e45" />

## Frame Extraction

Video files are processed by extracting individual frames.

```text
Video
  |
  +-- Frame 1
  +-- Frame 2
  +-- Frame 3
  +-- Frame ...
  |
  v
Processed Frames
```

Frame extraction allows image-based models to analyze information contained in ultrasound videos.

## Use in This Project

The IUGC video dataset supports the video-analysis component of the project.

It is used for:

- Ultrasound video preprocessing
- Frame extraction
- Video-level analysis
- Deep learning experiments
- Evaluation of ultrasound video models

## Model Evaluation

The project evaluates the performance of the video-analysis pipeline using appropriate classification metrics.

These may include:

- Accuracy
- Precision
- Recall
- F1-score

## Dataset Source

The dataset should be accessed from its original official source and used according to its licensing and usage requirements.

**Kaggle Dataset:**

https://www.kaggle.com/datasets/aspirexxx/iugc-ultrasound-video-dataset-miccai-2024

**Dataset Name:** IUGC Ultrasound Video Dataset (MICCAI 2024)

## Dataset Files

The original ultrasound video files are not included in this GitHub repository because of their large size and dataset distribution restrictions.

This folder contains documentation about the dataset and its use in the project.
