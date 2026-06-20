# Liver Disease Prediction 🫀

One of my first ML projects. Built during my internship where 
I learned how to take real patient data and train a model to 
predict whether someone has liver disease or not.

## What it does
Takes patient information like age, gender, bilirubin levels, 
and liver enzyme levels and predicts if the patient has 
liver disease.

## What I actually understood
The most interesting part was learning why we only applied 
IQR outlier removal to the enzyme columns (alkaline phosphatase, 
alamine aminotransferase, aspartate aminotransferase) and not 
all columns. Liver enzymes shoot up dramatically in sick patients 
so those columns specifically have extreme outliers that mess 
up the model.

## Tech used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

## Pipeline
1. Load and explore dataset
2. Handle missing values
3. Encode gender column (Male/Female → 0/1)
4. IQR outlier removal on enzyme columns
5. Correlation heatmap
6. SMOTE for class balancing
7. Train Logistic Regression model
8. Evaluate with accuracy, confusion matrix, classification report

## How I built this
Built with guidance during my first ML internship at 
DeltaQ Solutions (June 2026). Understood the full pipeline 
and the reasoning behind each step.

Dataset: Indian Liver Patient Dataset — publicly available on Kaggle.
