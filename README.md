# Liver Disease Prediction 🫀

One of my first ML projects built during my internship. 
Takes real patient data and predicts whether someone has 
liver disease or not — implemented using two different 
algorithms to compare performance.

## Two approaches, one dataset
| | Logistic Regression | Random Forest🌲 |
|---|---|---|
| Type | Linear classifier | Ensemble of decision trees |
| Training Accuracy | 0.6842105263157895| 1.0 |
| Testing Accuracy |0.6709677419354839 |0.7354838709677419|
| Best for | Simple, interpretable | Complex patterns |


## What it does
Takes patient information — age, gender, bilirubin levels, 
and liver enzyme levels — and predicts if the patient 
has liver disease.

## What I actually understood
The most interesting part was learning why we only applied 
IQR outlier removal to the enzyme columns specifically 
(alkaline phosphatase, alamine aminotransferase, aspartate 
aminotransferase) and not all columns.

Liver enzymes shoot up dramatically when the liver is damaged 
so those columns have extreme outliers that confuse the model. 
The other columns like age and bilirubin stay in relatively 
normal ranges so they didn't need the same treatment.

This was my first time understanding that data cleaning 
decisions aren't just mathematical — they require understanding 
what the data actually represents.

## Something I noticed and learnt eventually 🤔
Random Forest gave a training accuracy of 1.0 (100%) which 
looks perfect but is actually a red flag called overfitting.

The model memorized the training data completely instead of 
learning generalizable patterns. This is why testing accuracy 
is lower than training accuracy.

You can fix this by adding max_depth parameter to limit how 
deep the trees grow — but I kept it as is because seeing this 
happen and understanding WHY it happens felt more valuable 
than just fixing it blindly.

Overfitting is one of the most common real world ML problems 
and now I actually understand what it looks like.

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
7. Train model (Logistic Regression / Random Forest)
8. Evaluate with accuracy, confusion matrix, classification report
9. Predict for new patient sample

## Files
- `liver(2).ipynb` — Logistic Regression implementation
- `liver_randomforest.ipynb` — Random Forest implementation

## How I built this
Built with guidance during my first ML internship at 
DeltaQ Solutions (June 2026). Understood the full pipeline 
and the reasoning behind each decision — not just the code.

Dataset: Indian Liver Patient Dataset — publicly available on Kaggle.
