# STA314-ML-Project

Alzheimer’s Disease Prediction Project

## Overview

This project aims to develop a machine learning model to predict the likelihood of Alzheimer’s disease based on demographic, lifestyle, and medical data. The goal is to support early diagnosis and intervention, improving patient outcomes and reducing healthcare costs.

### Dataset
	•	Source: Classification of Alzheimer’s Disease Dataset
	•	Features: Includes patient demographic information, lifestyle factors, and medical records.
	•	Class Imbalance: 35.37% of samples are diagnosed with Alzheimer’s.

### Team
	•	William Wu: Data analysis, feature engineering, and modeling.
	•	Megan Wang: Data preprocessing and model evaluation.

### Final Results
	•	Kaggle Ranking: 64th
	•	Prediction Score: 0.94894

### Key Features
	•	Tree-Based Models: Random Forest, CatBoost, and XGBoost.
	•	Performance Metrics: Accuracy, ROC-AUC, Precision, Recall, and F1-Score.
	•	Techniques:
	•	Exploratory Data Analysis (EDA)
	•	Feature Engineering (e.g., threshold effects for key features)
	•	Hyperparameter Tuning (Grid Search)
	•	Ensemble Methods (Weighted Average, Stacking, Voting)

## Methodology

### Preprocessing
	•	Removed irrelevant features (e.g., PatientID).
	•	Handled categorical features by setting them as category data type.
	•	Addressed class imbalance using class weights in tree-based models.
	•	Assessed and mitigated multicollinearity and non-linear relationships.

### Models
	1.	Random Forest: Used as a baseline model.
	2.	CatBoost: Best individual model, with features selected via recursive elimination.
	3.	XGBoost: Optimized for efficiency in experimentation.
	4.	Ensemble Models: Combined strengths of Random Forest and CatBoost.

### Evaluation
	•	Cross-Validation: 5-fold cross-validation used to ensure generalizability.
	•	Primary Metric: ROC-AUC to account for class imbalance.
	•	Threshold Features: Incorporated threshold effects for critical features such as MMSE and FunctionalAssessment.

## Results
	•	Best Individual Model: CatBoost (Accuracy: 0.978, ROC-AUC: 0.946).
	•	Best Ensemble Model: Weighted average of CatBoost (70%) and Random Forest (30%) achieved an ROC-AUC of 0.958.

## Limitations & Future Directions
	1.	Focus on Tree-Based Models: May not fully capture complex feature interactions.
	2.	Interaction Effects: Future work could include interaction terms for better modeling.
	3.	Dataset Size: External validation needed to confirm generalizability.

## References
	•	Buda, M., Maki, A., & Mazurowski, M. A. (2018). A systematic study of the class imbalance problem in convolutional neural networks.
	•	CatBoost Documentation. https://catboost.ai/docs/en/concepts/parameter-tuning
	•	Dormann, C. F., et al. (2013). Collinearity: A review of methods to deal with it and a simulation study evaluating their performance.
