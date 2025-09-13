Overview
This project aims to build and evaluate a machine learning model to predict the onset of diabetes based on diagnostic measurements. The model uses a Support Vector Machine (SVM) classifier, and the entire process, from data cleaning to model deployment, is documented in the Jupyter notebook project2_diabetes.ipynb.

Dataset
The project uses the diabetes.csv dataset, which contains diagnostic information for several hundred female patients of Pima Indian heritage. The features include:

Pregnancies: Number of times pregnant

Glucose: Plasma glucose concentration

BloodPressure: Diastolic blood pressure (mm Hg)

SkinThickness: Triceps skin fold thickness (mm)

Insulin: 2-Hour serum insulin (mu U/ml)

BMI: Body mass index (weight in kg/(height in m)^2)

DiabetesPedigreeFunction: A function that scores the likelihood of diabetes based on family history

Age: Age in years

Outcome: Class variable (0 for non-diabetic, 1 for diabetic)

Notebook Structure
The Jupyter notebook is structured into the following key sections:

Importing Libraries: All necessary Python libraries for data manipulation, visualization, and machine learning are imported.

Data Loading and Exploration: The dataset is loaded, and initial data exploration is performed to understand its structure, identify missing values, and analyze descriptive statistics.

Data Preprocessing: This section handles the critical steps of data cleaning:

Replacing impossible zero values in key columns with NaN (missing values).

Imputing the missing values with the mean of their respective columns to avoid data loss.

Splitting the dataset into features (X) and the target variable (y).

Data Splitting and Scaling: The data is split into training and testing sets. StandardScaler is used to scale the features, which is essential for the optimal performance of the SVM model.

Model Training with Hyperparameter Tuning:

An SVM model with an 'rbf' kernel is chosen for classification.

GridSearchCV is employed to find the best hyperparameters (C and gamma) for the SVM model, ensuring it performs optimally.

Model Evaluation: The performance of the trained model is thoroughly evaluated using various metrics on the test set:

Confusion Matrix: Provides a detailed breakdown of correct and incorrect predictions.

Classification Report: Presents precision, recall, and F1-score for each class.

ROC Curve and AUC: Visualizes the model's ability to distinguish between classes and provides a single score for its overall performance.

Prediction on New Data: The final section demonstrates how to use the trained model to predict the diabetes status of a new, unseen patient. A reusable function is created to streamline this process.
