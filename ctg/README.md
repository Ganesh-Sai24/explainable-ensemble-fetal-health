# CTG Dataset

## Overview

The **Cardiotocography (CTG) dataset** is used in the **Explainable Ensemble Fetal Health** project for fetal health risk classification.

CTG is a fetal monitoring method that provides information related to:

- Fetal Heart Rate (FHR)
- Uterine Contractions (UC)
- Fetal movements
- Heart-rate variability
- Accelerations and decelerations

The dataset contains **2,126 fetal cardiotocograms** with extracted diagnostic features.

## Dataset Information

| Property | Details |
|---|---|
| Dataset | UCI Cardiotocography |
| Download Source | Kaggle |
| Original Source | UCI Machine Learning Repository |
| Records | 2,126 |
| Features | 21 |
| Task | Classification |
| Fetal Health Classes | Normal, Suspect, Pathologic |

The CTGs were classified by three expert obstetricians, with a consensus classification assigned to each record. The dataset can be used for both 3-class fetal-state classification and 10-class morphological-pattern classification.

## Kaggle Dataset

The dataset used in this project was downloaded from Kaggle:

**UCI Cardiotocography – Kaggle**

https://www.kaggle.com/datasets/propanon/uci-cardiotocography

## Original Dataset

The original Cardiotocography dataset is available from the UCI Machine Learning Repository:

https://archive.ics.uci.edu/dataset/193/cardiotocography

**DOI:** https://doi.org/10.24432/C51S4N

The UCI dataset is licensed under **CC BY 4.0**.

## CTG Concept

```text
              CTG Monitoring
                    |
          +---------+---------+
          |                   |
          v                   v
   Fetal Heart Rate    Uterine Contractions
          |                   |
          +---------+---------+
                    |
                    v
            Feature Extraction
                    |
                    v
           Machine Learning
                    |
                    v
       Fetal Health Classification
                    |
          +---------+---------+
          |         |         |
          v         v         v
       Normal    Suspect   Pathologic
```

## Important CTG Features

The dataset contains features related to:

- FHR baseline (LB)
- Accelerations (AC)
- Fetal movements (FM)
- Uterine contractions (UC)
- Light decelerations (DL)
- Severe decelerations (DS)
- Prolonged decelerations (DP)
- Short-term variability
- Long-term variability
- FHR histogram characteristics

The UCI documentation provides the complete variable descriptions.

## Fetal Health Classes

| Class | Description |
|---|---|
| Normal | Normal fetal state |
| Suspect | Suspected fetal state |
| Pathologic | Pathological fetal state |

## Dataset Distribution

The commonly reported class distribution is:

| Class | Records |
|---|---:|
| Normal | 1,655 |
| Suspect | 295 |
| Pathologic | 176 |
| **Total** | **2,126** |

This shows that the dataset is class-imbalanced, with Normal cases forming the largest class.

## Use in This Project

The CTG dataset is used for:

- Data preprocessing
- Exploratory data analysis
- Fetal health classification
- Machine learning model training
- Ensemble learning
- Model evaluation
- Explainable AI analysis

Models used/evaluated in the project include:

- Random Forest
- XGBoost
- LightGBM
- Gradient Boosting
- Soft Voting Ensemble

## Project Workflow

```text
Kaggle CTG Dataset
        |
        v
   Data Cleaning
        |
        v
 Feature Preparation
        |
        v
 Train / Test Split
        |
        v
 Machine Learning Models
        |
        v
 Soft Voting Ensemble
        |
        v
 Fetal Health Prediction
        |
        v
 Explainable AI
```

## Dataset License and Attribution

The Kaggle copy originates from the UCI Cardiotocography dataset. The original UCI dataset is licensed under **CC BY 4.0**. Please follow the original dataset's attribution and usage requirements.

### References

- Kaggle: UCI Cardiotocography  
  https://www.kaggle.com/datasets/propanon/uci-cardiotocography

- UCI Machine Learning Repository: Cardiotocography  
  https://archive.ics.uci.edu/dataset/193/cardiotocography

- DOI: https://doi.org/10.24432/C51S4N
