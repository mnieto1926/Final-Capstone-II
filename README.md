Multiple Myeloma Progression Prediction using Machine Learning
Overview:
This project applies machine learning techniques to predict progression from MGUS/SMM to Multiple Myeloma. 
The project focuses on identifying high-risk patients while balancing sensitivity and specificity.

Objectives
Predict disease progression using clinical biomarkers
Compare multiple machine learning algorithms
Optimize models using GridSearcCV
Evaluate threshols tunning for clinical sensitivity
Analyze ROC curves and confusion matrices

Dataset
Clinical Features Included
Example variables:
Age
Sex
M spike
K/L ratio
Cytogenetic risk
TP53 deletion status
B2M
Race
Disease status

Target variable
0 Disease progression/high risk
1 No progression/lower risk

Machine Learning  Models
The following models were evaluated:

Logistic Regression
K-Nearest Neighbors (KNN)
Support Vector Machine (SVM)
Decision Tree
Random Forest
XGBoost

Preprocessing

Data preprocessing included:

Missing value imputation
Feature scaling
One-hot encoding of categorical variables
Train/test split
Pipeline construction using scikit-learn

Hyperparameter Optimization

GridSearchCV was used to optimized:
SVM kernels and gamma values
Random Forest depth and estimators
XGBoost learning rate and tree depth
KNN neighbors and distance metrics.

Evaluation scoring:

python
scoring= 'roc-auc'

Performance Metrics
Models were evaluated using:
Accuracy
ROC-AUC
Precision
Recall
F1-score
Confusion Matrix
ROC Curves

Results Summary

Model     	Accuracy	ROC-AUC	Recall
SVM	          0.89	  0.90	   0.83
Random Forest	0.86	  0.92	   0.78
XGBoost	      0.79	  0.91	   0.78

The SVM demonstrated the highest overall accuracy, while Random Forest and XGBoost achieved excellent discrimination performance.

Threshold Tuning

Threshold optimization was performed to improve recall for high-risk patient detection. 

Example findings: 
Lower thresholds increased recall
Higher thresholds improved precision
Thresholds around 0.25-0.35 produced balanced F1-scores.

Visualizations:

The project includes:
ROC curves
Confusion matrices
Correlation heatmaps
Feature importance plots
Precision-Recall threshold analysis.

Technologies Used

Python
pandas
numpy
scikit-learn
XGBoost
matplotlib
seaborn

Clinical Relevance

This project demonstrates how machine learning may support:
early disease progression detection
risk stratification
precision medicine
clinical decision support systems

Future Improvements

Potential future work:

External validation dataset
Deep learning approaches
Survival analysis
SHAP explainability analysis
Integration with clinical workflows

Maria J Nieto. MD. MSc.




