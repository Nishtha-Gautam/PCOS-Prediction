# PCOS-Prediction-ML  
Machine learning models for predicting Polycystic Ovary Syndrome (PCOS) using a Kaggle dataset.<br><br>

## Project Overview  
This project develops predictive models for **Polycystic Ovary Syndrome (PCOS)** using a Kaggle dataset.<br>
The workflow includes imputation, feature selection, preprocessing, and evaluation of multiple ML algorithms.<br>
The goal is to identify key predictors of PCOS and evaluate model effectiveness in early diagnosis.<br><br>
This was a **group project under my B.Tech degree**, so parts of the code may appear **redundant** due to multiple contributors.<br><br>

## Methodology  
**Data Preprocessing:** MAR-based MICE imputation → ANOVA feature selection → Standardization<br>
**Model Training & Evaluation:** Train-test split → Logistic Regression (LR) → Support Vector Machine (SVM) → Multi-Layer Perceptron (MLP) → XGBoost (with hyperparameter tuning)<br><br>

## Results  
**Support Vector Machine (SVM):**<br>
Train → Accuracy: 0.9144, ROC-AUC: 0.9652<br>
Test → Accuracy: 0.9174, ROC-AUC: 0.9589<br><br>

**Logistic Regression (LR):**<br>
Train → Accuracy: 0.8912, ROC-AUC: 0.9627<br>
Test → Accuracy: 0.8716, ROC-AUC: 0.9444<br><br>

**XGBoost:**<br>
Best Params → {'colsample_bytree': 1.0, 'learning_rate': 0.1, 'max_depth': 3, 'n_estimators': 200, 'reg_alpha': 5, 'reg_lambda': 10, 'scale_pos_weight': 2.06, 'subsample': 0.7}<br>
Train → Accuracy: 0.9676, ROC-AUC: 0.9922<br>
Test → Accuracy: 0.8991, ROC-AUC: 0.9444<br><br>

**Multi-Layer Perceptron (MLP):**<br>
Best Params → {'activation': 'tanh', 'alpha': 0.0001, 'hidden_layer_sizes': (100,), 'learning_rate': 'adaptive', 'solver': 'sgd'}<br>
Train → Accuracy: 0.9259, ROC-AUC: 0.9672<br>
Test → Accuracy: 0.9083, ROC-AUC: 0.9585<br><br>

### ROC-AUC Curve Comparison
<p align="center">
  <img src="roc_auc.png" alt="ROC-AUC Curve Comparison" width="600"/>
</p>

## Observations  
- SVM and MLP provided consistently strong performance on both training and testing datasets.<br>
- Logistic Regression showed slightly lower accuracy but maintained a high ROC-AUC.<br>
- XGBoost achieved the best training performance but slightly lower testing accuracy, suggesting mild overfitting.<br>
- Feature analysis highlighted important clinical predictors relevant to PCOS.<br><br>

## Limitations  
- Based on a Kaggle dataset; real-world validation is needed on larger, diverse clinical datasets.<br>
- Some code redundancy is present due to collaborative group work.<br><br>

## License  
Open-source for academic and research purposes. Please cite this repository if used.<br>
