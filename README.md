Asteroid Classification Project

Overview

This project uses machine learning to classify asteroids as hazardous or non-hazardous based on their physical and orbital parameters. The dataset is sourced from NASA's asteroid dataset and is processed to train and evaluate three classifiers: Logistic Regression, Support Vector Machine (SVM), and XGBoost. The results include confusion matrices, ROC curves, and a correlation plot.

Dataset

File: nasa.csv

Path: C:\Users\somar\Downloads\asteroid\nasa.csv

Features Used:

Absolute Magnitude

Estimated Diameter in KM (min and max)

Relative Velocity (km per sec)

Miss Distance (kilometers)

Target Variable: Hazardous

Binary classification: 1 (Hazardous), 0 (Non-Hazardous)

Prerequisites

Python Libraries

Ensure the following libraries are installed:

pandas

numpy

matplotlib

seaborn

scikit-learn

xgboost

Install them using:

pip install pandas numpy matplotlib seaborn scikit-learn xgboost

Project Steps

Data Loading and Preprocessing

The dataset is loaded from the specified path.

Selected features are used to predict the Hazardous target variable.

Data is split into training and testing sets (80% training, 20% testing).

Model Training

Logistic Regression, SVM (with probability=True), and XGBoost classifiers are trained on the training data.

Evaluation Metrics

Confusion Matrices: Visualize true positives, true negatives, false positives, and false negatives for each classifier.

ROC Curves: Show the trade-off between the true positive rate and false positive rate for each classifier.

Correlation Plot: Displays correlations between the numerical features in the dataset.

Visualization

Confusion matrices and ROC curves are plotted for each classifier.

A correlation heatmap is generated to highlight relationships between features.

How to Run

Place the nasa.csv dataset in the specified path: C:\Users\somar\Downloads\asteroid\nasa.csv.

Copy the Python script into a file, e.g., asteroid_classification.py.

Run the script:

python asteroid_classification.py

The script will generate the following visualizations:

Confusion Matrices for Logistic Regression, SVM, and XGBoost.

ROC Curves for all three classifiers.

Correlation heatmap for numerical features.

Outputs

Confusion Matrices

Displays classification performance for each model.

ROC Curves

Provides AUC (Area Under Curve) values for each classifier.

Correlation Plot

Highlights the relationships between the numerical features in the dataset.

Customization

To modify the dataset path, change the read_csv path in the script:

df = pd.read_csv(r"C:\Users\somar\Downloads\asteroid\nasa.csv")

Add or remove features from the X variable as needed.

Results

The outputs provide insights into the performance of each model. XGBoost is expected to have the highest accuracy and ROC AUC among the three classifiers due to its robust ensemble nature.

References

Dataset: NASA Asteroid Dataset

Machine Learning Concepts: Scikit-learn Documentation

XGBoost: XGBoost Documentation
