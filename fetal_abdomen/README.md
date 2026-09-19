# Fetal Abdomen Dataset

This folder contains documentation about the **Fetal Abdomen Ultrasound Dataset** used in the Explainable Ensemble Fetal Health project.

The dataset is used for fetal abdomen detection and segmentation from ultrasound images. It supports the development of computer vision and deep learning methods for automated fetal ultrasound analysis.

## Dataset Overview

Fetal abdominal ultrasound images provide important information for assessing fetal growth and development.

In this project, the dataset is used to develop and evaluate deep learning models that can identify and segment the fetal abdomen in ultrasound images.

The segmentation output can help identify the fetal abdominal region and support automated ultrasound measurements.

## Dataset Source

The dataset was obtained from **Kaggle**.

Kaggle:
https://www.kaggle.com/datasets/orvile/fetal-abdominal-structures-segmentation-dataset

## Dataset Contents

The dataset generally contains:

- Fetal ultrasound images
- Corresponding segmentation masks
- Image and mask pairs
- Training data
- Validation or test data, depending on the dataset organization

The ultrasound images contain the fetal abdomen, while the corresponding masks identify the abdominal region.

## Purpose in Our Project

The Fetal Abdomen Dataset is used for:

- Fetal abdomen detection
- Fetal abdomen segmentation
- Ultrasound image analysis
- Deep learning experiments
- Region-of-interest extraction
- Automated fetal measurement support
- Computer vision research

## Segmentation Task

The main task is **image segmentation**.

The model learns to identify the fetal abdomen from the ultrasound image.

```text
Ultrasound Image
       ↓
Image Preprocessing
       ↓
Segmentation Model
       ↓
Predicted Mask
       ↓
Fetal Abdomen Region
       ↓
Measurement / Analysis
```

## Image and Mask Pair

Each training example consists of an ultrasound image and its corresponding segmentation mask.

```text
Input Image                 Ground Truth Mask

Ultrasound Image            Abdomen Mask
      ↓                           ↓
      └────────── Model ──────────┘
                     ↓
              Predicted Mask
```

The ground-truth mask is used to teach the model which pixels belong to the fetal abdomen.

## Data Preprocessing

Before training the segmentation model, the images can be processed using steps such as:

1. Loading ultrasound images
2. Loading corresponding masks
3. Checking image-mask pairs
4. Resizing images
5. Normalizing pixel values
6. Converting masks into suitable formats
7. Splitting the dataset into training and validation sets
8. Applying augmentation when required

## Segmentation Model

A **U-Net based architecture** can be used for fetal abdomen segmentation.

U-Net is suitable for medical image segmentation because it can learn both:

- Overall image information
- Detailed boundary information

```text
Input Ultrasound
       ↓
   Encoder
       ↓
Feature Extraction
       ↓
   Decoder
       ↓
Segmentation Mask
       ↓
Fetal Abdomen
```

## Model Training

During training, the model compares its predicted segmentation mask with the ground-truth mask.

The model parameters are updated to reduce the difference between the prediction and the ground truth.

Common segmentation loss functions include:

- Binary Cross-Entropy Loss
- Dice Loss
- Combined BCE + Dice Loss

## Evaluation Metrics

Segmentation performance can be evaluated using:

### Dice Score

Measures the overlap between the predicted mask and the ground-truth mask.

### Intersection over Union (IoU)

Measures the intersection between the predicted and actual regions compared with their union.

### Precision

Measures how much of the predicted fetal abdomen region is correct.

### Recall

Measures how much of the actual fetal abdomen region was detected.

## Evaluation Workflow

```text
Ground Truth Mask
        +
Predicted Mask
        ↓
   Comparison
        ↓
 ┌──────┼────────┐
 ↓      ↓        ↓
Dice    IoU   Precision/Recall
```

## Data Augmentation

Data augmentation can be used to improve model generalization.

Possible techniques include:

- Horizontal flipping
- Small rotations
- Scaling
- Cropping
- Brightness adjustment
- Contrast adjustment

Augmentation should preserve the anatomical information of the fetal abdomen.

## Project Relevance

Fetal abdomen segmentation is an important part of automated fetal ultrasound analysis.

The segmented region can be used as a basis for extracting measurements and analyzing fetal growth-related information.

This dataset therefore supports the ultrasound component of the overall **Explainable Ensemble Fetal Health** framework.

## Role in the Overall Project

```text
Fetal Health AI Framework
          ↓
   Ultrasound Analysis
          ↓
   Fetal Abdomen Image
          ↓
    Abdomen Segmentation
          ↓
      Region Detection
          ↓
    Measurement Analysis
          ↓
    Explainable Results
```
<img width="399" height="501" alt="image" src="https://github.com/user-attachments/assets/d4c8e3d3-9990-4b41-81b6-9a1c7b5497f4" />

## Dataset Usage

The dataset is used for research and academic purposes in this project.

The original dataset belongs to its respective authors and source organization.

Users should follow the original dataset's license and usage conditions.

## Summary

The Fetal Abdomen Dataset provides ultrasound images and segmentation information for identifying the fetal abdomen.

In this project, it supports the development of an AI-based fetal abdomen segmentation system and contributes to the ultrasound analysis component of the Explainable Ensemble Fetal Health framework.
