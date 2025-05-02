# Diabetes Prediction using K - Nearest Neighbors (KNN)

## Problem Statement
The goal of this project is to predict whether a patient is likely to be diagnosed with diabetes based on various health metrics such as glucose level, BMI, age, pregnancies, etc., using machine learning models. The data used comes from female patients of Pima Indian heritage aged 21 and above.

## Proposed System / Solution

This system uses the K-Nearest Neighbors (KNN) algorithm to classify patients into two categories:
- 1 → Diabetic
- 0 → Non-Diabetic
The model is trained using medical data and aims to give accurate predictions by finding patterns among patient characteristics.

## System Development Approach

1. Imported Required Libraries
You imported Python libraries like pandas, numpy, seaborn, matplotlib, and sklearn to handle data, visualize patterns, and apply machine learning models.
2. Loaded the Dataset
You used a dataset named diabetes.csv which contains 768 records with 8 input features and 1 target column (Outcome).
3. Exploratory Data Analysis (EDA)
You explored the data using:
- .describe() → to get statistical details.
- .info() → to see column types.
- .isna() and .duplicated() → to check missing values and duplicates.
- countplot, boxplot, pairplot, histplot, heatmap → to understand distribution, relationships, and detect outliers.
4. Feature Scaling
You used StandardScaler to normalize the input values. This helps improve model performance by making all features have the same scale.
5. Splitting the Dataset
You split the data into training (70%) and testing (30%) using train_test_split.
This helps test the model on unseen data.
6. Model Selection: KNN
You implemented the K-Nearest Neighbors algorithm:
-	You tested the model with values of k from 1 to 14.
- Stored accuracy for both train and test sets.
- Found best k = 13 for test accuracy (~77.9%).
- Plotted train vs test accuracy using line plots.
7. Evaluation of Final Model
You chose k=13 (best test score) and:
- Evaluated accuracy on test data.
- Generated a confusion matrix.
- Printed a classification report to check precision, recall, f1-score.

## Algorithm & Deployment
## Algorithm Used:
## K-Nearest Neighbors (KNN)
- It stores all data points.
- To predict, it finds the 'k' closest data points and chooses the majority class.
- Here, k = 13 gave the best results.
## Deployment:
This code is designed for offline or academic use. For real-world deployment, it can be wrapped in a web app or REST API using Flask or Streamlit.

## Result 

#### Confusion Matrix Output:
![result 1](https://github.com/user-attachments/assets/ca26b621-3182-438d-ae15-0fe59fd8ac25)

#### This means:
- 141 people were correctly predicted as Non-Diabetic.
- 39 people were correctly predicted as Diabetic.
- 35 diabetic people were wrongly classified as non-diabetic (False Negatives).
- 16 non-diabetic were wrongly predicted as diabetic (False Positives).
#### Classification Report:
- Accuracy: ~78%
- Precision for diabetic (1): 0.71
- Recall for diabetic (1): 0.53
- F1 Score for diabetic (1): 0.60
This shows your model is good, but could be improved further (especially for predicting diabetics).

## Conclusion
You successfully created a diabetes prediction system using the KNN algorithm. You:
- Preprocessed and visualized the data.
- Normalized features using StandardScaler.
- Found the best value of k using accuracy testing.
- Evaluated your final model using metrics and plots.
Your model achieved ~78% accuracy on test data using k=13.

## Future Scope
- Improve predictions using advanced models like Random Forest, XGBoost, or Neural Networks.
- Use hyperparameter tuning techniques like Grid Search.
- Address the imbalanced dataset using oversampling (e.g., SMOTE).
- Build a web interface for user-friendly access to predictions.
- Include more real-world data (males, other age groups, ethnicities).

## References
1.	Dataset: Pima Indian Diabetes Dataset
2.	Scikit-learn Documentation: https://scikit-learn.org/
3.	Seaborn Visualization: https://seaborn.pydata.org/
4.	StandardScaler Info: https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html
5.	K-Nearest Neighbors: https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html

