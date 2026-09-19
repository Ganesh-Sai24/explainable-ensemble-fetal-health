# IUGC Image Dataset

This folder contains documentation about the IUGC Ultrasound Image Dataset used in the **Explainable Ensemble Fetal Health** project.

The dataset is used for fetal ultrasound image analysis and supports experiments involving image preprocessing, deep learning, feature extraction, and automated ultrasound assessment.

## Dataset Overview

The IUGC Ultrasound Dataset contains fetal ultrasound images collected for research in intrapartum ultrasound analysis.

The images can be used to develop and evaluate AI and deep learning methods for automated analysis of fetal ultrasound images.

The dataset is associated with the **IUGC MICCAI 2025 challenge**.

## Dataset Source

**Kaggle Dataset:**  
https://www.kaggle.com/datasets/aspirexxx/iugc-ultrasound-dataset-miccai-2025

**Dataset Name:** IUGC Ultrasound Dataset – MICCAI 2025

**Number of Images:** 28,919 ultrasound images

**License:** CC BY-NC 4.0

## Dataset Characteristics

The dataset contains ultrasound images that can be used for automated fetal ultrasound analysis.

Important characteristics include:

- Ultrasound images related to fetal assessment
- Images collected for research purposes
- Large-scale image collection
- Suitable for computer vision experiments
- Useful for deep learning model development
- Supports automated image analysis

## Purpose in Our Project

The IUGC Image Dataset is used as one of the ultrasound-related datasets in the project.

It supports:

- Fetal ultrasound image analysis
- Image classification
- Image preprocessing
- Feature extraction
- Deep learning experiments
- Computer vision research
- Automated ultrasound assessment

## Image Processing

Before using the images for model training, preprocessing can be performed.

Typical preprocessing steps include:

1. Loading ultrasound images
2. Checking image quality
3. Removing or handling invalid images
4. Resizing images
5. Normalizing pixel values
6. Preparing training and validation data
7. Applying data augmentation when required

## Processing Workflow

```text
IUGC Ultrasound Images
          ↓
Data Collection
          ↓
Image Quality Check
          ↓
Image Preprocessing
          ↓
Resize & Normalization
          ↓
Data Augmentation
          ↓
Feature Extraction
          ↓
Deep Learning Model
          ↓
Image Analysis
          ↓
Ultrasound Assessment
```

## Model Development

Deep learning and computer vision techniques can be applied to this dataset.

Possible approaches include:

- Convolutional Neural Networks (CNN)
- Transfer Learning
- EfficientNet
- ResNet
- Vision Transformers
- Image Classification Models
- Feature Extraction Networks

The processed images can be used to train and evaluate models for automated ultrasound image analysis.

## Training and Evaluation

The dataset can be divided into different subsets for machine learning experiments.

```text
Dataset
   ↓
Training Set
   ↓
Validation Set
   ↓
Test Set
```

Model performance can be evaluated using metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

For image segmentation tasks, additional metrics such as **IoU** and **Dice Score** can be used when applicable.

## Project Relevance

Ultrasound imaging provides important visual information for fetal assessment.

The IUGC Image Dataset helps extend the project from CTG-based fetal risk assessment to **AI-based ultrasound image analysis**.

This supports the overall goal of developing an explainable AI framework that can work with multiple types of fetal health data.

## Role in the Overall Project

```text
                    Fetal Health AI
                          ↓
        ┌─────────────────┼─────────────────┐
        ↓                 ↓                 ↓
       CTG          Ultrasound Images   Ultrasound Videos
        ↓                 ↓                 ↓
   Risk Analysis     Image Analysis    Video Analysis
        └─────────────────┼─────────────────┘
                          ↓
                  Explainable AI
                          ↓
               Clinical Decision Support
```

## Dataset Usage

The dataset is used for **research and academic purposes** in this project.

The original dataset and its associated resources belong to their respective authors and organizations.

Users should follow the original dataset's license and usage conditions when using or redistributing the data.

## Dataset Link

**Kaggle:**  
https://www.kaggle.com/datasets/aspirexxx/iugc-ultrasound-dataset-miccai-2025

## Summary

The IUGC Image Dataset provides a large collection of fetal ultrasound images for research and AI-based analysis.

In this project, it is used to support ultrasound image processing and deep learning experiments as part of the broader **Explainable Ensemble Fetal Health** framework.
