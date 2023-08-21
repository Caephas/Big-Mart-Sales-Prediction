# Big Mart Sales Prediction

This project focuses on predicting the sales of different products in various outlets of Big Mart. We will use different features related to each product and its respective store, and apply the XGBoost Regressor machine learning model to predict sales.

## Libraries Used

- `numpy`: For numerical computations.
- `pandas`: For data manipulation and analysis.
- `matplotlib`: For creating static, interactive, and animated visualizations.
- `seaborn`: For data visualization.
- `sklearn`: For data preprocessing and model evaluation.
- `xgboost`: For using the XGBoost Regressor.

### Steps followed

1. **Importing the dependencies**: Necessary modules and libraries are imported.

2. **Data Collection and Analysis**:
    - The dataset 'Train.csv' is loaded into a pandas DataFrame.
    - Preliminary analysis like shape, info, and null values are checked.

3. **Handling missing values**:
    - The 'Item_Weight' column missing values are filled with the mean.
    - For the 'Outlet_Size' column, missing values are replaced using a pivot table that considers the mode of the 'Outlet_Size' based on the 'Outlet_Type'.

4. **Data Analysis**:
    - Basic statistics of data are checked.
    - Data distribution for various columns such as 'Item_Weight', 'Item_Visibility', 'Item_MRP', and 'Item_Outlet_Sales' are visualized.
    - Categorical data like 'Outlet_Establishment_Year', 'Item_Type', and 'Outlet_Size' distributions are plotted.
    - Variations in 'Item_Fat_Content' values are standardized.

5. **Label Encoding**:
    - Categorical variables like 'Item_Identifier', 'Item_Fat_Content', 'Item_Type', 'Outlet_Identifier', 'Outlet_Size', 'Outlet_Location_Type', and 'Outlet_Type' are encoded to numerical values.

6. **Splitting features and targets**:
    - Features (X) and target (Y) are separated. The target here is 'Item_Outlet_Sales'.

7. **Data Splitting**:
    - The data is split into training and test sets.

8. **Training the machine learning model**:
    - An XGBoost Regressor model is trained on the training data.

9. **Model Evaluation**:
    - Predictions are made on both training and test data.
    - R squared value is computed to evaluate the performance of the model on both training and test datasets.

### Note

Ensure that you have all the mentioned libraries installed and make sure 'Train.csv' is available in the project directory when running the code.

### How to run

Open your Jupyter notebook or any preferred IDE that supports IPython notebooks. Load the provided notebook, ensure the 'Train.csv' is in the correct path, and then execute the cells sequentially
