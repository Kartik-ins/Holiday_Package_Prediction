# Holiday Package Prediction - README

## Overview
This project focuses on predicting whether a customer will purchase a holiday package based on their demographic and behavioral characteristics. The solution uses machine learning techniques to analyze customer data and predict purchase likelihood.

## Project Structure
```
holiday-package-prediction/
├── Travel.csv            # Raw dataset
├── requirements.txt      # Python dependencies
├── Holiday_Package_Prediction.ipynb  # Jupyter notebook with full analysis
└── README.md            # This file
```

## Key Steps

### 1. Data Cleaning
- Handled missing values by imputing with median/mode
- Corrected inconsistent categories (e.g., "Fe Male" → "Female")
- Combined related features ("TotalVisiting" = NumberOfPersonVisiting + NumberOfChildrenVisiting)

### 2. Feature Engineering
- Identified numerical and categorical features
- Created discrete and continuous feature categories
- Applied appropriate transformations

### 3. Model Training
Tested multiple algorithms:
- Logistic Regression
- Decision Tree
- Random Forest (best performer)
- Gradient Boosting

### 4. Hyperparameter Tuning
Optimized Random Forest parameters using RandomizedSearchCV:
- n_estimators: 1000
- min_samples_split: 2
- max_features: 7
- max_depth: None

## Results
The tuned Random Forest model achieved:
- Test Accuracy: 93.35%
- Precision: 97.01%
- Recall: 68.06%
- ROC AUC: 0.838

## Requirements
To run this project, install the required packages:
```
pip install -r requirements.txt
```

## Usage
1. Clone the repository
2. Install dependencies
3. Run the Jupyter notebook `Holiday_Package_Prediction.ipynb`

## Future Improvements
- Experiment with additional ensemble methods
- Implement feature importance analysis
- Develop a web interface for predictions
- Handle class imbalance more effectively

## Acknowledgments
Dataset provided by [source name if available]. Special thanks to [any contributors].
