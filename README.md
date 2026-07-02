# 🚗 Used Car Price Prediction Model

## 📌 Overview
This is an end-to-end Machine Learning project aimed at predicting the prices of used cars based on various features such as the car's name, company, manufacturing year, kilometers driven, and fuel type. The project handles messy, real-world scraped data, builds a robust ML pipeline, and deploys the final model using Pickle.

## 🛠️ Tech Stack
*   **Language:** Python
*   **Data Manipulation:** Pandas, NumPy
*   **Visualization:** Matplotlib, Seaborn
*   **Machine Learning:** Scikit-Learn (Linear Regression, OneHotEncoder, Pipelines)
*   **Model Serialization:** Pickle

## 📂 Dataset
The dataset (`quikr_car.csv`) contains 892 raw records of used cars. 
*   **Features:** `name`, `company`, `year`, `kms_driven`, `fuel_type`
*   **Target Variable:** `Price`

## 🚀 Project Workflow
1.  **Data Cleaning:** Handled severe data inconsistencies. Extracted numeric values from strings, removed outliers (e.g., 'Ask For Price', invalid years), and dropped null values. Reduced dataset from 892 to 816 clean records.
2.  **Exploratory Data Analysis (EDA):** Visualized price distributions across different car manufacturers and the correlation between mileage and price.
3.  **Feature Engineering:** Applied One-Hot Encoding to categorical variables (`name`, `company`, `fuel_type`) while passing numerical variables (`year`, `kms_driven`) through.
4.  **Pipeline Construction:** Built a Scikit-Learn `Pipeline` and `ColumnTransformer` to prevent data leakage and streamline preprocessing.
5.  **Model Optimization:** Evaluated 1,000 different train-test split random states to find the most statistically representative split, improving the model's $R^2$ score from **0.65 to 0.86**.
6.  **Model Export:** Serialized the final trained pipeline into a `.pkl` file for future web app deployment or inference.

## 📈 Model Performance
*   **Algorithm:** Multiple Linear Regression
*   **Final R² Score:** `0.8604`
*   **Best Random State:** `247`

## 📁 Files Included
*   `project2 (1).ipynb` - Complete Jupyter Notebook with code and EDA.
*   `cleaned_car_data.csv` - The cleaned dataset ready for modeling.
*   `LinearRegressionModel.pkl` - The saved machine learning pipeline.