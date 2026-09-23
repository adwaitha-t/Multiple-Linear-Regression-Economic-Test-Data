# Multiple-Linear-Regression-Economic-Test-Data
Multiple Linear Regression on Economic Test data using train-test split, OLS regression, and MSE/RMSE evaluation.
📌 Project Overview

This project implements Multiple Linear Regression on an economic dataset to understand the relationship between multiple independent variables and a dependent variable.

The project follows a complete machine learning workflow, including data preprocessing, train-test splitting, model training using Ordinary Least Squares (OLS) Linear Regression, prediction, and model evaluation using Mean Squared Error (MSE) and Root Mean Squared Error (RMSE).

🎯 Objectives
Understand the relationship between multiple economic variables.
Build a Multiple Linear Regression model.
Split the dataset into training and testing sets.
Train the model using Ordinary Least Squares (OLS).
Generate predictions on unseen test data.
Evaluate model performance using MSE and RMSE.
🛠️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
Statsmodels
Matplotlib / Seaborn
📂 Dataset

The project uses an Economic Test CSV dataset containing multiple economic variables.

The dataset is used to:

Identify independent and dependent variables
Train the regression model
Test predictions on unseen data
🔄 Project Workflow
Load Dataset
     ↓
Data Exploration
     ↓
Data Preprocessing
     ↓
Define X and y
     ↓
Train-Test Split
     ↓
Multiple Linear Regression
     ↓
OLS Regression
     ↓
Generate Predictions
     ↓
Evaluate Model
     ↓
MSE & RMSE
📊 Multiple Linear Regression

Multiple Linear Regression models the relationship between a dependent variable and multiple independent variables.

The general form is:

Y = β₀ + β₁X₁ + β₂X₂ + ... + βₙXₙ + ε

where:

Y = dependent variable
X₁, X₂, ..., Xₙ = independent variables
β₀ = intercept
β₁, β₂, ..., βₙ = regression coefficients
ε = error term
📈 Train-Test Split

The dataset was divided into training and testing subsets.

The training set was used to fit the regression model, while the test set was used to evaluate how well the model performs on unseen data.

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
🤖 Model Used
Ordinary Least Squares (OLS)

OLS estimates the regression coefficients by minimizing the sum of squared differences between the actual and predicted values.

The project uses:

from sklearn.linear_model import LinearRegression

regression = LinearRegression()
regression.fit(X_train, y_train)

y_pred = regression.predict(X_test)

An OLS statistical summary can also be generated using Statsmodels:

import statsmodels.api as sm

X_train_ols = sm.add_constant(X_train)

model = sm.OLS(y_train, X_train_ols).fit()

print(model.summary())
📏 Model Evaluation

Two evaluation metrics were used.

Mean Squared Error (MSE)

MSE measures the average squared difference between actual and predicted values.

MSE = average((Actual - Predicted)²)

A lower MSE generally indicates smaller prediction errors.

Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and expresses the error in the same units as the target variable.

RMSE = √MSE

Python implementation:

from sklearn.metrics import mean_squared_error

mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)

print("MSE:", mse)
print("RMSE:", rmse)
📌 Key Steps Performed
Loaded the economic dataset using Pandas.
Explored the dataset and its variables.
Selected independent and dependent variables.
Divided the dataset into training and testing sets.
Built a Multiple Linear Regression model.
Trained the model using OLS.
Generated predictions for the test set.
Evaluated the model using MSE and RMSE.
Examined regression results and model performance.
📁 Project Structure
Economic-Multiple-Linear-Regression/
│
├── Economic_Test.csv
├── Multiple_Linear_Regression.ipynb
├── README.md
└── requirements.txt
🚀 How to Run
1. Clone the repository
git clone <your-github-repository-link>
2. Install the required libraries
pip install pandas numpy scikit-learn statsmodels matplotlib seaborn
3. Open the Jupyter Notebook
jupyter notebook

Open:

Multiple_Linear_Regression.ipynb

and run the cells sequentially.

📌 Results

The model performance is evaluated using:

MSE: Mean Squared Error
RMSE: Root Mean Squared Error

The results provide an indication of how accurately the Multiple Linear Regression model predicts the target variable on unseen economic data.

🔮 Future Improvements
Compare Linear Regression with Ridge and Lasso Regression.
Perform feature selection.
Analyze multicollinearity using VIF.
Check regression assumptions using residual analysis.
Compare different train-test split ratios.
Perform cross-validation.
Tune the model and compare performance.
👩‍💻 Author

Adwaitha T

This project was developed as part of my learning and practice in Machine Learning, Regression Analysis, and Python-based Data Analytics.
