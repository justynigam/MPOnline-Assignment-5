# Employee Attrition Prediction

Name: Nigam Prasad Lenka


Reg No: 23BCE11432


Application no: IN26011682


Batch Number: 1(A)


Email: nigam.23bce11432@vitbhopal.ac.in

## Objective
The objective of this assignment is to develop and compare machine learning models (Decision Tree and Random Forest) to predict employee attrition based on demographic, professional, and work-related attributes.

## Dataset Link
Dataset used: [IBM HR Analytics Employee Attrition & Performance Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) *(Hosted on Kaggle)*.

## Libraries Used
* `pandas` - Data manipulation and analysis
* `numpy` - Numerical operations
* `matplotlib` & `seaborn` - Data visualization
* `scikit-learn` - Machine learning model building, preprocessing, and evaluation

## Methodology
1. **Data Understanding**: Loaded the dataset, identified feature types, and reviewed summary statistics.
2. **Data Preprocessing**: Verified no missing values, dropped zero-variance/ID columns (`EmployeeCount`, `StandardHours`, etc.), applied One-Hot Encoding to categorical features, and split the data (80% train, 20% test).
3. **Model Development**: Trained a standard Decision Tree Classifier and a Random Forest Classifier (100 estimators).
4. **Evaluation**: Compared models using Accuracy, Precision, Recall, F1-Score, and Confusion Matrices. Extracted feature importances from the Random Forest.

## Results
* **Decision Tree:** Displayed lower generalization accuracy and was prone to overfitting the training data.
* **Random Forest:** Achieved higher overall accuracy and a better F1-score. The top features driving attrition were identified as Monthly Income, Age, and OverTime.
* *(Bonus)* Tuning the `max_depth` parameter on the Decision Tree improved its performance by restricting it from memorizing the noise in the training set.

## Model Comparison
Random Forest outperformed the Decision Tree in almost all evaluation metrics. While the Decision Tree struggled with the natural class imbalance (leading to higher false negatives/positives), the Random Forest mitigated this by averaging the predictions of 100 individual trees, resulting in a much more robust and reliable model.

## Conclusion
Random Forest is the superior model for this dataset due to its ensemble nature, which reduces variance and prevents overfitting. However, its "black box" nature makes it slightly harder to interpret for HR stakeholders compared to a simple, highly visual Decision Tree.
