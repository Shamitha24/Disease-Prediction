# Disease Prediction from Symptoms

## Problem Statement

Early and accurate diagnosis of diseases is critical for effective treatment and improved patient outcomes. However, in many healthcare settings, particularly in resource-constrained environments — access to specialized medical professionals and diagnostic tools is limited. Patients often present with a set of symptoms, and identifying the most likely disease(s) from these symptoms remains a challenging pattern recognition task.

This project aims to develop a **machine learning-based system** capable of predicting probable diseases given a patient’s reported symptoms. The goal is to assist healthcare providers, medical students, and patients in generating informed preliminary disease hypotheses, thereby supporting faster triage and decision-making.

## Project Overview

This repository implements a **multi-class classification model** to predict diseases based on binary symptom features (present/absent). Multiple algorithms are compared, with emphasis on interpretability, accuracy, and generalization.

### Key Objectives
- Build a reliable symptom-to-disease prediction model
- Compare performance of common classification algorithms
- Achieve high predictive accuracy on real-world-like symptom data
- Provide a reproducible notebook with preprocessing, modeling, and evaluation

## Dataset

- **Source**: Commonly used symptom-disease dataset (Kaggle / UCI-style format)
- **Training samples**: ≈ 4920 records
- **Features**: 132 binary symptoms (1 = present, 0 = absent)
- **Target classes**: 41 distinct diseases / prognosis labels
- **Train / Test split**: 80:20 (stratified)

## Model Performance

| Model                | Accuracy   | Precision (macro) | Recall (macro) | F1-Score (macro) | Notes                          |
|----------------------|------------|-------------------|----------------|------------------|--------------------------------|
| Random Forest        | **97.8%**  | 0.978             | 0.977          | 0.977            | Best overall performance       |
| Decision Tree        | 94.1%      | 0.942             | 0.940          | 0.941            | Good interpretability          |
| Gradient Boosting    | 96.5%      | 0.966             | 0.965          | 0.965            | Strong, slightly slower        |
| Support Vector Machine | 92.8%    | 0.930             | 0.928          | 0.929            | Kernel = RBF                   |
| Naive Bayes          | 85.4%      | 0.862             | 0.854          | 0.857            | Fast baseline                  |

**Best model**: Random Forest Classifier  
**Test set accuracy**: **97.8%**  
**Cross-validation accuracy** (5-fold): ~96.9–97.6%

## Technologies & Libraries

- Python 3.8+
- pandas, numpy
- scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

