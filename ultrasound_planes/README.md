<img width="694" height="689" alt="Screenshot 2026-09-19 112835" src="https://github.com/user-attachments/assets/b487a03f-b6da-4662-b433-c78750dd475e" />

# Ultrasound Planes Dataset

## Overview

The **Ultrasound Planes dataset** is used in the **Explainable Ensemble Fetal Health** project for fetal ultrasound image classification.

The dataset contains ultrasound images representing different standard fetal anatomical views.

## Purpose

This dataset is used for:

- Fetal ultrasound image classification
- Identification of standard ultrasound planes
- Image-based fetal analysis
- Deep learning model development
- Model evaluation

## Dataset Information

| Property | Details |
|---|---|
| Dataset Type | Fetal Ultrasound Images |
| Modality | Ultrasound |
| Data Type | Images |
| Task | Image Classification |
| Application | Fetal ultrasound analysis |

## Ultrasound Plane Classification

Ultrasound images can represent different anatomical planes or views of the fetus.

Examples include:

- Head / brain views
- Abdomen views
- Femur views
- Thorax views
- Other fetal anatomical views

The exact classes depend on the dataset version used in the project.

## Image Processing

Before model training, ultrasound images can be processed using steps such as:

- Image resizing
- Normalization
- Data cleaning
- Train-validation-test splitting
- Data augmentation where required

## Deep Learning Workflow

```text
Ultrasound Images
        |
        v
 Image Preprocessing
        |
        v
 Data Augmentation
        |
        v
 Deep Learning Model
        |
        v
 Feature Extraction
        |
        v
 Plane Classification
        |
        v
 Predicted Ultrasound Plane
```

## Use in This Project

The dataset supports the ultrasound component of the fetal health assessment system.

It is used for:

- Ultrasound image analysis
- Fetal anatomical view identification
- Deep learning experiments
- Supporting multimodal fetal health assessment
- Model evaluation

## Dataset Source

The dataset is used for academic and research purposes.

The original dataset source and license information should be followed according to the specific dataset version used in this project.

## Note

The original image files are not included in this GitHub repository because of dataset size and/or distribution restrictions.

Only dataset documentation is maintained in this repository.
