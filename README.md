# Student Academic Performance Prediction

This repository contains the practical part of my MSc Computer Science dissertation at GISMA University of Applied Sciences.

My dissertation focuses on predicting students final mathematics grades using machine learning. The main idea of the project is to compare different regression models and see how well they can predict the final grade (G3) from student-related information.

For the main experiment, I removed G1 and G2 because these variables contain the students' previous grades. I wanted to see whether the final grade could still be predicted from other information such as study habits, family background, school-related factors, absences and educational support.

## Dataset

I used the Student Performance Mathematics dataset (student-mat.csv). It contains data about secondary-school students and includes demographic, family, behavioural, school and academic information.

The target variable in this project is G3, which represents the final mathematics grade.

## Models

I compared six regression models:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree
- Random Forest
- XGBoost

## Evaluation

I used an 80/20 train-test split. The models were evaluated using:

- MAE
- RMSE
- R²
- 5-fold cross-validation

Hyperparameter tuning was also carried out for the models that required it.

## Main Results

For the main experiment without G1 and G2, XGBoost achieved the lowest cross-validation RMSE of 3.9469.

On the final test set, Random Forest produced the best test results with:

- MAE: 3.2102
- RMSE: 3.9928
- R²: 0.2225

I also carried out another experiment where G1 and G2 were included. The results improved considerably, with an R² of 0.8079 and RMSE of 1.9845.

This showed that previous grades contain much stronger information for predicting the final grade.

## Notebook

The file student_performance_prediction.ipynb contains the Python implementation of the project, including data exploration, preprocessing, model training, cross-validation, model evaluation and comparison of the results.

## Tools

The project was developed in Python using Jupyter Notebook and machine-learning libraries such as pandas, NumPy, scikit-learn and XGBoost.

A fixed random state of 42 was used where applicable to make the experiment reproducible.

## Author
Eid Mohammad Qasimi  
MSc Computer Science  
GISMA University of Applied Sciences

