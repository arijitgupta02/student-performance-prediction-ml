# Student Performance Prediction using Machine Learning

## Overview

This project develops and compares machine learning models for predicting student academic performance.

Three regression models are implemented:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor

The project also applies hyperparameter tuning using GridSearchCV and evaluates the models using 5-fold cross-validation.

## Objectives

The main objectives of this project are:

1. Load and preprocess a student performance dataset.
2. Train a Linear Regression model.
3. Train a Decision Tree Regression model.
4. Train a Random Forest Regression model.
5. Perform hyperparameter tuning using GridSearchCV.
6. Perform 5-fold cross-validation.
7. Compare the models using MAE, RMSE, and R².
8. Visualize feature importance.
9. Identify the best-performing model.
10. Generate a final recommendation report.

## Dataset

The project uses the Student Performance dataset.

The target variable is `G3`, which represents the student's final grade.

The dataset contains demographic, social, family, and academic information about students.

The dataset is automatically downloaded by the Google Colab notebook.

## Machine Learning Models

### Linear Regression

Linear Regression is used as a baseline regression model for predicting the final student grade.

### Decision Tree Regressor

Decision Tree Regression is used to model nonlinear relationships between the input features and the final student grade.

GridSearchCV is used to tune the Decision Tree hyperparameters.

### Random Forest Regressor

Random Forest Regression combines multiple decision trees to improve prediction performance and reduce overfitting.

GridSearchCV is used to tune the Random Forest hyperparameters.

## Data Preprocessing

The following preprocessing steps are applied:

* Separation of features and target variable
* Identification of numerical and categorical features
* Standardization of numerical features
* One-hot encoding of categorical features
* Train-test split

## Hyperparameter Tuning

GridSearchCV is used to search for suitable hyperparameter combinations for:

* Decision Tree Regressor
* Random Forest Regressor

Five-fold cross-validation is used during the grid search process.

## Cross-Validation

Five-fold cross-validation is performed to evaluate model performance across multiple subsets of the dataset.

The mean and standard deviation of the evaluation metrics are calculated.

## Evaluation Metrics

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between the actual and predicted values.

A lower MAE indicates better performance.

### Root Mean Squared Error (RMSE)

RMSE measures the square root of the average squared prediction error.

A lower RMSE indicates better performance.

### R² Score

R² measures the proportion of variance in the target variable explained by the model.

A higher R² indicates better performance.

## Project Workflow

```text
Student Performance Dataset
            |
            v
    Data Preprocessing
            |
            v
      Train-Test Split
            |
            v
   +--------+---------+
   |        |         |
   v        v         v
Linear   Decision   Random
Regression  Tree     Forest
   |        |         |
   |        v         v
   |    GridSearchCV  |
   |        |         |
   +--------+---------+
            |
            v
   5-Fold Cross-Validation
            |
            v
     MAE / RMSE / R²
            |
            v
      Model Comparison
            |
            v
    Feature Importance
            |
            v
       Best Model
            |
            v
   Final Recommendation
```

## Project Structure

```text
student-performance-prediction-ml/
|
├── data/
│   └── student-mat.csv
|
├── models/
│   ├── linear_regression_model.joblib
│   ├── decision_tree_model.joblib
│   └── random_forest_model.joblib
|
├── results/
│   ├── evaluation_comparison.csv
│   ├── feature_importance.csv
│   ├── dataset_summary.csv
│   ├── final_recommendation_report.txt
│   |
│   └── plots/
│       ├── feature_importance.png
│       ├── actual_vs_predicted.png
│       └── model_rmse_comparison.png
|
├── Student_Performance_Prediction_Colab.ipynb
├── requirements.txt
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/student-performance-prediction-ml.git
```

Move into the project directory:

```bash
cd student-performance-prediction-ml
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Running the Project

### Google Colab

Open:

```text
Student_Performance_Prediction_Colab.ipynb
```

Upload the notebook to Google Colab and run the cells sequentially.

The notebook downloads the dataset, preprocesses the data, trains the models, performs hyperparameter tuning and cross-validation, evaluates the models, and generates the project outputs.

### Local Environment

The project can also be executed in a Python environment after installing the dependencies listed in `requirements.txt`.

## Outputs

After execution, the project generates the following outputs:

### Trained Models

```text
linear_regression_model.joblib
decision_tree_model.joblib
random_forest_model.joblib
```

### Evaluation Results

```text
evaluation_comparison.csv
```

This file contains the model performance results for MAE, RMSE, R², and 5-fold cross-validation.

### Feature Importance

```text
feature_importance.csv
```

This file contains the calculated feature importance values from the Random Forest model.

### Visualizations

The following plots are generated:

```text
feature_importance.png
actual_vs_predicted.png
model_rmse_comparison.png
```

### Final Recommendation

```text
final_recommendation_report.txt
```

This report summarizes the model comparison and identifies the recommended model based on the evaluation results.

## Results

The actual results are generated when the notebook is executed.

The models are compared using MAE, RMSE, and R².

| Model             |                       MAE |                      RMSE |                        R² |
| ----------------- | ------------------------: | ------------------------: | ------------------------: |
| Linear Regression | Generated after execution | Generated after execution | Generated after execution |
| Decision Tree     | Generated after execution | Generated after execution | Generated after execution |
| Random Forest     | Generated after execution | Generated after execution | Generated after execution |

The final model recommendation is based on the evaluation results.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib
* Google Colab
* GitHub

## Future Scope

Possible future improvements include:

* Testing additional regression algorithms
* Improving feature selection
* Exploring ensemble learning techniques
* Performing more extensive hyperparameter optimization
* Applying explainable AI techniques
* Developing a web-based interface for student performance prediction
* Evaluating the model on additional student performance datasets

## License

This project is intended for educational and research purposes.
