# Sales_prediction_model

Sales Prediction Model
This repository contains a sales prediction model to predict future sales based on historical data. Accurate sales predictions are essential for inventory management, marketing strategy, and budgeting decisions. The model utilizes regression techniques, including Linear Regression and Random Forest Regressor, to forecast sales.

Table of Contents
Introduction
Dataset
Features
Requirements
Installation
Usage
Model Training
Evaluation
Results
Contributing
License
Introduction
The Sales Prediction Model uses historical sales data from retail outlets to predict future sales. By forecasting future sales, businesses can make better decisions for resource allocation, inventory planning, and financial forecasting.

The model follows a machine learning pipeline consisting of data preprocessing, feature encoding, model training, and evaluation. Two models are trained: Linear Regression and Random Forest Regressor, to identify the best-performing algorithm for sales prediction.

Dataset
The dataset used for this project is the BigMart Sales Data, which contains sales information from different outlets. The dataset includes the following columns:

Item_Identifier: Unique product ID
Item_Weight: Weight of the product
Item_Fat_Content: Level of fat content in the product
Item_Visibility: Percentage of product visibility
Item_Type: Category to which the product belongs
Item_MRP: Maximum retail price of the product
Outlet_Identifier: Unique store ID
Outlet_Establishment_Year: Year of establishment of the outlet
Outlet_Size: Size of the outlet (small, medium, large)
Outlet_Location_Type: Type of city in which the outlet is located
Outlet_Type: Type of outlet (e.g., grocery store, supermarket)
Item_Outlet_Sales: Sales of the product (target variable)
Features
The model takes the following steps:

Handling Missing Values: Missing values in Item_Weight and Outlet_Size columns are imputed with the mean and most frequent value, respectively.
Categorical Encoding:
Label encoding for Item_Identifier, Outlet_Identifier, and Item_Fat_Content.
One-hot encoding for Item_Type, Outlet_Size, Outlet_Location_Type, and Outlet_Type.
Feature Scaling: Scaling is done where needed to standardize data.
Model Training: Linear Regression and Random Forest Regressor models are trained using scikit-learn.
Evaluation: Mean Squared Error (MSE) and R² score are used to evaluate the model's performance.
Requirements
Python 3.7+
Pandas
NumPy
Scikit-learn
Installation
Clone the repository:

sh
Copy code
git clone https://github.com/yourusername/sales-prediction-model.git
cd sales-prediction-model
Install the required dependencies:

sh
Copy code
pip install -r requirements.txt
Usage
To use the sales prediction model, follow these steps:

Place the dataset (CSV file) in the root directory.

Update the file_path variable in the script to the dataset location.

Run the script:

sh
Copy code
python Sales_Prediction_Model.py
The script will preprocess the data, train the models, and output evaluation metrics.

Model Training
The model is trained using two algorithms:

Linear Regression: This is a basic approach to find the linear relationship between features and the target variable.
Random Forest Regressor: This is an ensemble learning technique that helps reduce variance and improve the model's prediction accuracy.
The dataset is split into an 80-20 train-test ratio for model training and evaluation.

Evaluation
The following evaluation metrics are used:

Mean Squared Error (MSE): Measures the average squared difference between the predicted and actual values.
R² Score: Measures the proportion of variance in the dependent variable that is predictable from the independent variables.
Results
After training and evaluating the models:

Linear Regression:

Mean Squared Error: MSE_LINEAR
R² Score: R2_LINEAR
Random Forest Regressor:

Mean Squared Error: MSE_RF
R² Score: R2_RF
The Random Forest model generally performs better in terms of prediction accuracy, given the complexity and non-linearity of sales data.

Contributing
Contributions are welcome! Please follow these steps:

Fork this repository.
Create a new branch (git checkout -b feature-branch).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Create a new Pull Request.
