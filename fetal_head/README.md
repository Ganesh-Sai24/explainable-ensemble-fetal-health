# Fetal Head Dataset

This folder contains documentation about the **Fetal Head Ultrasound Dataset** used in the Explainable Ensemble Fetal Health project.

The dataset is used for fetal head ultrasound image analysis and image segmentation. It supports the development of deep learning models for automatically identifying the fetal head region in ultrasound images.

## Dataset Overview

Fetal head ultrasound analysis is an important part of automated fetal assessment.

The dataset contains ultrasound images prepared for **fetal head image segmentation**. The images can be used to train computer vision and deep learning models to identify the fetal head region.

## Dataset Source

The dataset was obtained from Kaggle.

**Kaggle Dataset:**  
https://www.kaggle.com/datasets/ankit8467/fetal-head-ultrasound-dataset-for-image-segment

**Dataset Name:** Fetal Head UltraSound Dataset For Image Segment

**Data Type:** Fetal ultrasound images

**Main Task:** Fetal head image segmentation

The Kaggle dataset contains **2,335 files** organized into training and test sets.

## Dataset Structure

The Kaggle dataset contains:

```text
Fetal Head Dataset
│
├── training_set
│
└── test_set
```

The training data is used to train the segmentation model, while the test data can be used to evaluate model performance.

## Purpose in Our Project

The Fetal Head Dataset is used for:

- Fetal head detection
- Fetal head segmentation
- Ultrasound image analysis
- Deep learning experiments
- Medical image processing
- Region-of-interest extraction
- Automated fetal ultrasound analysis

## Segmentation Task

The main objective is to identify the fetal head region from an ultrasound image.

```text
Ultrasound Image
        ↓
Image Preprocessing
        ↓
Segmentation Model
        ↓
Predicted Mask
        ↓
Fetal Head Region
        ↓
Measurement / Analysis
```

## Image Preprocessing

Before training the model, the ultrasound images can be processed using steps such as:

1. Loading the images
2. Checking image quality
3. Matching images with their masks
4. Resizing images
5. Normalizing pixel values
6. Preparing training and validation data
7. Applying suitable data augmentation

Preprocessing helps provide consistent input to the deep learning model.

## Segmentation Model

A **U-Net architecture** can be used for fetal head segmentation.

U-Net is commonly used for medical image segmentation because it can preserve spatial information while learning important image features.

```text
Input Ultrasound Image
          ↓
       Encoder
          ↓
   Feature Extraction
          ↓
       Decoder
          ↓
   Predicted Mask
          ↓
     Fetal Head
```

## Model Training

During training, the predicted segmentation mask is compared with the ground-truth mask.

The model learns to reduce the difference between the predicted and actual fetal head regions.

Possible loss functions include:

- Binary Cross-Entropy Loss
- Dice Loss
- BCE + Dice Loss

## Evaluation Metrics

The segmentation model can be evaluated using:

### Dice Score

Measures the overlap between the predicted fetal head region and the ground-truth region.

### Intersection over Union (IoU)

Measures the overlap between the predicted and actual segmentation regions.

### Precision

Measures how much of the predicted fetal head region is correct.

### Recall

Measures how much of the actual fetal head region has been detected.

## Evaluation Workflow

```text
Ground Truth Mask
        +
Predicted Mask
        ↓
     Comparison
        ↓
 ┌──────┼─────────┐
 ↓      ↓         ↓
Dice    IoU    Precision/Recall
```

## Data Augmentation

Data augmentation can be applied to increase the variety of training images.

Possible techniques include:

- Horizontal flipping
- Small rotations
- Scaling
- Cropping
- Brightness adjustment
- Contrast adjustment

Augmentation should be applied carefully so that the anatomical information of the fetal head is not distorted.

## Project Relevance

Fetal head segmentation is an important component of ultrasound-based fetal assessment.

Identifying the fetal head region can support automated fetal measurements and further ultrasound analysis.

This dataset therefore contributes to the ultrasound component of the **Explainable Ensemble Fetal Health** project.

## Role in the Overall Project

```text
Explainable Ensemble Fetal Health
              ↓
       Ultrasound Analysis
              ↓
        Fetal Head Image
              ↓
       Head Segmentation
              ↓
        Region Detection
              ↓
      Measurement Analysis
              ↓
       Explainable Results
```

## Integration With Other Datasets

The Fetal Head Dataset is one of several datasets used in the project.

```text
                 Fetal Health AI
                       ↓
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
       CTG       Ultrasound Images  Ultrasound Video
        ↓              ↓              ↓
   Risk Analysis  Segmentation     Video Analysis
        └──────────────┼──────────────┘
                       ↓
                 Explainable AI
```

## Dataset Usage

The dataset is used for research and academic purposes in this project.

The original dataset belongs to its respective dataset creator and source organization.

Users should follow the dataset's terms and license conditions when using the data.

## Dataset Link

**Kaggle:**  
https://www.kaggle.com/datasets/ankit8467/fetal-head-ultrasound-dataset-for-image-segment

## Summary

The Fetal Head Ultrasound Dataset provides ultrasound images for fetal head image segmentation.

In this project, it supports the development of an AI-based fetal head segmentation system and contributes to the ultrasound analysis component of the Explainable Ensemble Fetal Health framework.
