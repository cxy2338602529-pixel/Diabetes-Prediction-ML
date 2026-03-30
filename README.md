# Diabetes-Prediction-pipeline

Diabetes Risk Prediction: Modeling and Interpretability

This project builds a machine learning pipeline to predict diabetes risk based on clinical features such as Glucose, BMI, and Age.
The focus is on data preprocessing, model comparison, and improving interpretability using SHAP.

⸻

Methodology

1. Exploratory Data Analysis (EDA)
	•	Examined feature distributions (mean, median, range) to understand the dataset
	•	Identified unrealistic zero values (e.g., BMI, Blood Pressure) and replaced them with missing values
	•	Applied median imputation to preserve clinical plausibility
	•	Explored feature relationships using correlation heatmaps and boxplots
	•	Checked class balance in the target variable

⸻

2. Model Building
	•	Built a Scikit-learn pipeline for preprocessing and training
	•	Compared four models:
	•	Logistic Regression
	•	Random Forest
	•	Support Vector Machine
	•	K-Nearest Neighbors
	•	Evaluated performance using Accuracy, Precision, Recall, and F1-score

⸻

3. Model Optimization and Validation
![CV Results](cv_histogram.png)
*Figure 4: 5-Fold Cross-Validation scores showing the consistency and reliability of the model.*
    •	Performed hyperparameter tuning using GridSearchCV
	•	Compared baseline and tuned model performance
	•	The Random Forest model performed best after tuning
	•	Used 5-fold cross-validation to assess model stability
	•	Visualized performance using ROC and Precision-Recall curves
![CV Results](roc_curve.png,pr_curve.png)
*Figure 5: Precision-Recall (PR) curve highlighting the balance between precision and sensitivity.
⸻

4. Model Interpretation
![Feature Importance](feature_importance.png)
*Figure 3: Global feature importance derived from the Random Forest classifier.*
	•	Examined feature importance from the Random Forest model
    •	Used SHAP to understand how each feature influences predictions
	•	Provided both global and individual-level explanations
![CV Results](shap_summary.png)
*Figure 6: SHAP summary plot providing clinical insights into how each feature (e.g., Glucose, BMI) contributes to the prediction.
⸻

Key Results
	•	Glucose is the most important feature in predicting diabetes
	•	The tuned Random Forest model achieved strong precision and overall performance
	•	SHAP analysis helps make model predictions more interpretable

⸻

Repository Structure
	•	Diabetes-Prediction-ML.ipynb: full workflow (EDA, modeling, evaluation)
	•	best_model.pkl: trained Random Forest model
	•	requirements.txt: dependencies
