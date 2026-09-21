## 📌 Project Overview

Fetal health monitoring is an important part of prenatal care, particularly during the third trimester of pregnancy. **Cardiotocography (CTG)** is a widely used non-invasive technique for monitoring fetal heart rate and uterine contractions.

Although CTG provides valuable information about fetal condition, its interpretation can be complex, time-consuming, and dependent on clinical expertise. Machine Learning (ML) and Artificial Intelligence (AI) can assist healthcare professionals by automatically analyzing CTG-derived features and identifying potential fetal health risks.

This project proposes an **optimized, explainable ensemble learning framework** for AI-assisted early fetal health risk assessment using CTG data.

The framework focuses on combining:

- Data preprocessing
- Class-imbalance handling
- Feature optimization
- Multiple machine learning models
- Ensemble learning
- Hyperparameter optimization
- Explainable AI (XAI)
- Robust model evaluation

The objective is not to replace clinical judgment, but to provide an **AI-assisted decision-support system** that can help healthcare professionals interpret CTG-based fetal health patterns more efficiently.

---

## 🎯 Project Objectives

The major objectives of this project are:

1. To develop an AI-based framework for fetal health assessment using CTG data.
2. To handle the class imbalance present in fetal health datasets.
3. To identify and retain informative CTG features.
4. To investigate multiple machine learning algorithms.
5. To develop an optimized ensemble learning approach.
6. To tune model hyperparameters for improved predictive performance.
7. To evaluate the model using appropriate classification metrics.
8. To incorporate Explainable AI techniques to understand model predictions.
9. To provide interpretable information about the features contributing to predictions.
10. To design the framework as an AI-assisted clinical decision-support approach.

---

## 🩺 Problem Statement

CTG records contain multiple measurements related to fetal heart rate, uterine contractions, variability, accelerations, decelerations, and histogram characteristics.

Traditional CTG interpretation can involve:

- Large amounts of physiological information
- Complex feature relationships
- Subjective interpretation
- Time-consuming manual analysis
- Difficulty in identifying subtle patterns
- Class imbalance in available datasets

A machine learning system can learn patterns from historical CTG data and classify fetal health status automatically.

However, a high-performing model alone is not sufficient for a healthcare-oriented application.

The proposed project therefore focuses on both:

> **Prediction performance + Interpretability**

---

## 💡 Proposed Solution

The proposed framework follows a structured pipeline:

```text
                 CTG Dataset
                      │
                      ▼
             Data Preprocessing
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
   Outlier Handling       Class Balancing
                                  │
                                SMOTE
                                  │
          └───────────┬───────────┘
                      ▼
             Feature Optimization
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
   Feature Selection      Feature Analysis
          │
          └───────────┬───────────┘
                      ▼
          Multiple ML Classifiers
                      │
                      ▼
          Hyperparameter Optimization
                      │
                      ▼
             Ensemble Learning
                      │
                      ▼
             Optimized Model
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
     Prediction              Explainability
          │                       │
          └───────────┬───────────┘
                      ▼
          Fetal Health Risk Assessment
````

The final framework is intended to classify fetal health status and provide interpretable information about the model's decision.

---

## 🧠 Fetal Health Classes

The CTG classification problem is formulated as a three-class classification task:

| Class            | Description                                          |
| ---------------- | ---------------------------------------------------- |
| **Normal**       | CTG pattern associated with normal fetal condition   |
| **Suspect**      | CTG pattern requiring increased attention/monitoring |
| **Pathological** | CTG pattern associated with abnormal fetal condition |

The exact interpretation of these classes follows the labeling of the dataset used in the project.

---

## 📊 Dataset

The project is based on the publicly available **UCI Cardiotocography (CTG) dataset** used extensively in fetal health classification research.

The dataset contains:

* **2,126 CTG records**
* **21 CTG-related features**
* **3 target classes**
* No missing attributes in the original dataset

### Class Distribution

| Fetal Health Class |   Samples | Approx. Percentage |
| ------------------ | --------: | -----------------: |
| Normal             |     1,655 |              77.8% |
| Suspect            |       295 |              13.9% |
| Pathological       |       176 |               8.3% |
| **Total**          | **2,126** |           **100%** |

The dataset is therefore significantly imbalanced, with the Normal class representing the majority of observations.

This makes appropriate class-imbalance handling important when developing and evaluating the model.

---

## 🧬 CTG Features

The dataset contains features derived from fetal heart rate and uterine contraction measurements, including:

* Baseline fetal heart rate
* Accelerations
* Fetal movement
* Uterine contractions
* Light decelerations
* Severe decelerations
* Prolonged decelerations
* Short-term variability
* Long-term variability
* Abnormal short-term variability
* Abnormal long-term variability
* Histogram width
* Histogram minimum
* Histogram maximum
* Histogram mean
* Histogram median
* Histogram mode
* Histogram variance
* Histogram tendency
* Number of histogram peaks
* Number of histogram zeroes

Feature selection and optimization are used to investigate which features provide the most useful information for classification.

---

## ⚙️ Methodology

### 1. Data Preprocessing

The preprocessing stage may include:

* Data inspection
* Outlier analysis
* Feature scaling
* Standardization / normalization
* Redundant feature removal
* Class balancing

---

### 2. Class Imbalance Handling

Because the fetal health dataset is imbalanced, **Synthetic Minority Oversampling Technique (SMOTE)** is considered for balancing the training data.

SMOTE generates synthetic minority-class samples rather than simply duplicating existing samples.

The objective is to improve the model's ability to learn minority classes such as:

* Suspect
* Pathological

without allowing the majority Normal class to dominate the learning process.

---

### 3. Feature Optimization

Feature optimization may involve techniques such as:

* Correlation analysis
* Feature importance
* Statistical feature selection
* Mutual Information
* Tree-based feature selection
* Dimensionality reduction

The purpose is to reduce unnecessary or redundant information while retaining features that contribute to fetal health classification.

---

### 4. Machine Learning Models

The framework investigates multiple classification algorithms, including tree-based, distance-based, kernel-based, and boosting approaches.

Candidate models include:

* Random Forest
* Extra Trees
* Support Vector Machine
* K-Nearest Neighbors
* LightGBM
* Gradient Boosting
* Decision Tree
* Other suitable classifiers

The final model selection will be based on experimental evaluation rather than assuming that a particular algorithm is optimal beforehand.

---

### 5. Ensemble Learning

The project focuses on **ensemble learning**.

Instead of depending on a single classifier, predictions from multiple models can be combined to improve robustness and predictive performance.

Possible ensemble strategies include:

* Voting
* Stacking
* Other suitable ensemble mechanisms

A stacking architecture can be represented as:

```text
        Model 1 ─────┐
                     │
        Model 2 ─────┼──► Meta Learner ──► Final Prediction
                     │
        Model 3 ─────┘
```

The base models learn different patterns from the CTG data, while the meta-model learns how to combine their predictions.

---

### 6. Hyperparameter Optimization

Model hyperparameters can significantly affect predictive performance.

The project therefore investigates systematic hyperparameter optimization techniques such as:

* Grid Search
* Cross-validation-based tuning
* Model-specific parameter optimization

The objective is to identify suitable model configurations rather than relying only on default parameters.

---

### 7. Explainable AI

Explainability is a major component of the proposed framework.

A prediction system used in a healthcare context should provide more information than simply:

```text
Prediction: Pathological
```

The system should also help answer:

> **Why did the model make this prediction?**

Explainable AI techniques may be used to identify:

* Important features
* Features contributing to individual predictions
* Global feature importance
* Local prediction explanations
* Relationships between CTG characteristics and predictions

Possible techniques include:

* SHAP
* LIME
* Feature importance
* Other suitable XAI methods

The final XAI technique will depend on the implemented model and experimental results.

---

## 🔬 Model Evaluation

The framework will be evaluated using multiple classification metrics rather than relying only on accuracy.

### Accuracy

Measures the proportion of correctly classified samples.

### Precision

Measures how many predicted positive instances are actually positive.

### Recall

Measures how many actual positive instances are correctly identified.

### F1-score

Provides a combined measure of precision and recall.

### Balanced Accuracy

Particularly useful for imbalanced classification because it considers performance across classes rather than allowing the majority class to dominate the metric.

### ROC-AUC

Measures the ability of the model to distinguish between classes across classification thresholds, where applicable.

### Confusion Matrix

Used to examine class-wise prediction behavior and identify misclassification between:

* Normal
* Suspect
* Pathological

---

## 🔄 Validation Strategy

Cross-validation will be used where appropriate to obtain a more robust estimate of model generalization.

A five-fold cross-validation strategy can be represented as:

```text
Fold 1 → Validation
Fold 2 → Validation
Fold 3 → Validation
Fold 4 → Validation
Fold 5 → Validation
```

Each fold is used as the validation portion once while the remaining folds are used for training.

When SMOTE is applied, it should be performed only on the relevant training portion to reduce the risk of data leakage.

---

## 🏗️ Proposed Framework

The overall proposed framework can be summarized as:

```text
CTG Data
   │
   ▼
Data Cleaning & Preprocessing
   │
   ▼
Class Imbalance Analysis
   │
   ▼
SMOTE on Training Data
   │
   ▼
Feature Selection / Optimization
   │
   ▼
Multiple ML Models
   │
   ▼
Hyperparameter Tuning
   │
   ▼
Ensemble Learning
   │
   ▼
Cross-Validation & Evaluation
   │
   ▼
Optimized Ensemble Model
   │
   ├──────────────► Fetal Health Prediction
   │
   └──────────────► Explainable AI
                           │
                           ▼
                  Feature Contributions
                           │
                           ▼
                 Interpretable Decision Support
```

---

## 📚 Literature Review

The project is supported by research on:

* CTG-based fetal health classification
* Machine learning for fetal monitoring
* Deep learning for CTG analysis
* Class imbalance handling
* SMOTE
* Feature selection
* Ensemble learning
* Hyperparameter optimization
* Explainable AI
* AI-assisted healthcare decision support

Detailed analysis of the selected papers is maintained separately in the `docs/` directory.

### Literature Documentation

```text
docs/
├── base-paper-analysis.md
├── supporting-paper-1-analysis.md
├── supporting-paper-2-analysis.md
├── supporting-paper-3-analysis.md
└── literature-review.md
```

The detailed paper analyses contain:

* Paper objectives
* Dataset details
* Methodology
* Algorithms
* Preprocessing
* Results
* Limitations
* Research gaps
* Viva questions
* Relationship to the proposed project

---

## 📖 Key Literature Contributions

### Base Paper

The base paper provides the primary technical foundation for handling **imbalanced CTG data**, particularly through:

* SMOTE
* Cross-validation
* Balanced Accuracy
* Comparison of multiple ML models
* DNN evaluation
* LightGBM-based fetal health classification

Its results demonstrate why ordinary accuracy alone may not be sufficient for an imbalanced fetal-health dataset.

---

### Supporting Paper 1

Supporting Paper 1 contributes additional research context and methodology relevant to the development of the proposed fetal-health prediction framework.

Detailed analysis is available in:

`docs/supporting-paper-1-analysis.md`

---

### Supporting Paper 2

Supporting Paper 2 provides broader context regarding the use of AI in women's health and clinical diagnostic applications.

It highlights important considerations including:

* Clinical decision support
* Explainability
* Bias and fairness
* Privacy
* Regulatory considerations
* Human-AI collaboration
* Real-world clinical integration

Detailed analysis is available in:

`docs/supporting-paper-2-analysis.md`

---

### Supporting Paper 3

Supporting Paper 3 investigates extensive preprocessing, feature selection, hyperparameter optimization, and ensemble learning for CTG-based fetal health classification.

The paper reports a Stacking Classifier combining:

```text
SVM + Extra Trees + LightGBM
```

with reported performance of:

* Accuracy: **98.9%**
* Precision: **99.0%**
* Recall: **98.6%**
* F1-score: **99.3%**
* ROC-AUC: **99.8%**

This paper provides strong methodological motivation for the **optimized ensemble-learning component** of the proposed project.

Detailed analysis is available in:

`docs/supporting-paper-3-analysis.md`

---

## 🔎 Research Gap

The reviewed literature demonstrates strong progress in AI-based fetal health classification. However, several areas remain important for further investigation:

### 1. Class imbalance

Fetal health datasets can contain substantially more Normal cases than Suspect and Pathological cases.

### 2. Model optimization

Different models and preprocessing strategies can produce significantly different results.

### 3. Ensemble learning

Combining complementary models can provide an alternative to relying on a single classifier.

### 4. Explainability

High predictive performance does not automatically explain why a prediction was produced.

### 5. Clinical interpretability

Healthcare-oriented AI systems should provide understandable information that can assist clinical users.

### 6. Generalization

Models developed on a single public dataset require further validation on additional datasets before real-world deployment.

---

## 🚀 Proposed Contribution

The proposed project aims to bring these aspects together into a single framework:

```text
                 ┌─────────────────────┐
                 │    CTG Dataset      │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Preprocessing     │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │  Class Balancing    │
                 │      (SMOTE)        │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Feature Optimization│
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Multiple ML Models  │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Hyperparameter      │
                 │ Optimization        │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Ensemble Learning   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Optimized Ensemble  │
                 └──────────┬──────────┘
                            │
                 ┌──────────┴──────────┐
                 ▼                     ▼
        ┌─────────────────┐   ┌─────────────────┐
        │ Fetal Health    │   │ Explainable AI  │
        │ Prediction      │   │                 │
        └─────────────────┘   └─────────────────┘
```

---

## 🛠️ Technology Stack

### Programming Language

* Python

### Data Processing

* Pandas
* NumPy

### Machine Learning

* Scikit-learn
* Imbalanced-learn

### Candidate ML Algorithms

* Random Forest
* Extra Trees
* Support Vector Machine
* K-Nearest Neighbors
* LightGBM
* Gradient Boosting
* Decision Tree

### Explainable AI

* SHAP
* LIME
* Feature importance techniques

### Visualization

* Matplotlib
* Seaborn

### Development Environment

* Jupyter Notebook
* Python development environment

### Version Control

* Git
* GitHub

> The exact libraries and algorithms used in the final implementation may be updated as experimentation progresses.

---

## 📁 Repository Structure

```text
major-project/
│
├── README.md
│
├── docs/
│   ├── base-paper-analysis.md
│   ├── supporting-paper-1-analysis.md
│   ├── supporting-paper-2-analysis.md
│   ├── supporting-paper-3-analysis.md
│   └── literature-review.md
│
├── data/
│   └── README.md
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_feature_selection.ipynb
│   ├── 04_model_training.ipynb
│   ├── 05_ensemble_learning.ipynb
│   └── 06_explainability.ipynb
│
├── src/
│   ├── preprocessing/
│   ├── feature_selection/
│   ├── models/
│   ├── ensemble/
│   ├── optimization/
│   ├── explainability/
│   └── evaluation/
│
├── results/
│   ├── figures/
│   ├── metrics/
│   └── reports/
│
├── requirements.txt
│
└── LICENSE
```

---

## 📌 Project Status

**Status:** 🚧 In Development

Current development stages include:

* [x] Literature review
* [x] Base paper analysis
* [x] Supporting paper analysis
* [x] Dataset identification
* [x] Problem formulation
* [ ] Data preprocessing implementation
* [ ] Exploratory data analysis
* [ ] Feature optimization
* [ ] Baseline model development
* [ ] Ensemble model development
* [ ] Hyperparameter optimization
* [ ] Explainable AI implementation
* [ ] Model comparison
* [ ] Final evaluation
* [ ] Prototype / user interface
* [ ] Final documentation

---

## ⚠️ Important Clinical Disclaimer

This project is an **academic research and decision-support prototype**.

It is not intended to:

* replace obstetricians or other healthcare professionals,
* provide autonomous medical diagnosis,
* determine treatment without clinical supervision,
* be used as a certified medical device.

Any real-world clinical deployment would require appropriate:

* clinical validation,
* external testing,
* safety assessment,
* regulatory approval,
* privacy and security measures,
* integration with clinical workflows.

---

## 🔮 Future Scope

Potential future improvements include:

* External validation using additional CTG datasets
* Real-time CTG data processing
* Integration with CTG monitoring systems
* More advanced ensemble architectures
* Automated hyperparameter optimization
* Advanced Explainable AI
* Patient-specific/local explanations
* Model calibration
* Bias and subgroup analysis
* Clinical workflow integration
* Prospective clinical validation
* Scalable deployment

---

## 👥 Project Team

**Major Project**

**Project Title:**

> *An Optimized Explainable Ensemble Learning Framework for AI-Assisted Early Fetal Health Risk Assessment Using Cardiotocography Data*

---

## 📚 References

The major research papers used to establish the technical and clinical foundation of this project are documented in:

```text
docs/base-paper-analysis.md
docs/supporting-paper-1-analysis.md
docs/supporting-paper-2-analysis.md
docs/supporting-paper-3-analysis.md
docs/literature-review.md
```

The original publications should be cited directly when reproducing or extending their methods or reported results.

---

## ⭐ Project Vision

The long-term goal of this project is to develop an AI-assisted framework that combines:

**Accurate Prediction**

*

**Optimized Ensemble Learning**

*

**Explainable AI**

*

**CTG-Based Fetal Health Assessment**

to support healthcare professionals with more informative and interpretable fetal health risk assessment.

> **AI should assist clinical decision-making, not replace clinical expertise.**

````

### One change I strongly recommend

For your **current GitHub repository**, I would keep the README above as the **main documentation**, but don't put every paper's detailed results into it. Your structure should remain:

```text
Major-Project/
│
├── README.md                         ← Main project overview
│
├── docs/
│   ├── base-paper-analysis.md       ← Deep base-paper study
│   ├── supporting-paper-1-analysis.md
│   ├── supporting-paper-2-analysis.md
│   ├── supporting-paper-3-analysis.md
│   └── literature-review.md
│
├── data/
├── notebooks/
├── src/
├── results/
├── requirements.txt
└── LICENSE
````

