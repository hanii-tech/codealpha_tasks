# Car Price Prediction Using Machine Learning

## Overview

This project predicts the selling price of used cars using machine learning regression models. The project covers data cleaning, exploratory data analysis, preprocessing, model building, evaluation, and visualization.

## Objective

To build machine learning models that can predict a car's selling price based on features such as manufacturing year, present price, driven kilometers, fuel type, selling type, transmission, and ownership.

## Dataset

The dataset contains information about used cars with the following columns:

- `Car_Name` — Name of the car
- `Year` — Year of manufacture
- `Selling_Price` — Target variable
- `Present_Price` — Present price of the car
- `Driven_kms` — Kilometers driven
- `Fuel_Type` — Fuel type
- `Selling_type` — Dealer or individual
- `Transmission` — Manual or automatic
- `Owner` — Number of previous owners

The original dataset contained 301 records. After removing 2 duplicate records, the dataset contains **299 rows and 9 columns**.

`Car_Name` was excluded from model training because the dataset contains 98 unique car names. Including this high-cardinality feature could create many additional encoded columns for this relatively small dataset.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

1. Load and inspect the dataset
2. Check data types and missing values
3. Remove duplicate records
4. Perform exploratory data analysis
5. Analyze numerical and categorical features
6. Calculate feature correlations
7. Select features and target
8. Encode categorical variables
9. Split the data into training and testing sets
10. Train regression models
11. Evaluate model performance
12. Visualize actual vs predicted prices

## Exploratory Data Analysis

The following visualizations were created:

- Distribution of Selling Price
- Present Price vs Selling Price
- Driven Kms vs Selling Price
- Year vs Selling Price
- Selling Price by Fuel Type
- Selling Price by Selling Type
- Selling Price by Transmission
- Correlation Heatmap
- Actual vs Predicted Selling Price

### Key EDA Findings

- `Present_Price` has the strongest linear relationship with `Selling_Price`, with a correlation of approximately **0.88**.
- Newer cars generally tend to have higher selling prices.
- `Driven_kms` shows a weak linear relationship with selling price in this dataset.
- Fuel type, selling type, and transmission show differences in selling-price distributions.

## Data Preprocessing

The categorical features used for preprocessing were:

- `Fuel_Type`
- `Selling_type`
- `Transmission`

These features were encoded using `OneHotEncoder` inside a `ColumnTransformer`.

The encoder was configured with:

- `drop="first"` to remove one reference category
- `handle_unknown="ignore"` to safely handle categories not seen during training

The numerical features were passed through without transformation.

The dataset was divided into training and testing sets using an **80/20 split** with `random_state=42`.

## Machine Learning Models

### Linear Regression

A Linear Regression model was trained using a Scikit-learn Pipeline containing the preprocessing steps and regression model.

### Random Forest Regression

A Random Forest Regressor was trained using:

- `n_estimators=200`
- `random_state=42`

## Model Evaluation

The models were evaluated using:

- **MAE (Mean Absolute Error)** — measures the average absolute difference between actual and predicted prices.
- **RMSE (Root Mean Squared Error)** — measures prediction error while giving greater weight to larger errors.
- **R² Score** — measures how much variation in the target variable is explained by the model.

### Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 1.47 | 2.52 | 0.753 |
| Random Forest | 1.53 | 3.67 | 0.477 |

For the particular train-test split used in this project, Linear Regression produced the stronger test-set metrics.

## Actual vs Predicted Analysis

The actual-versus-predicted plot shows that most Linear Regression predictions are relatively close to the perfect-prediction line. A few observations show small deviations from the line, indicating prediction errors. One high-priced observation has an actual selling price above 30 lakhs.

## Conclusion

This project demonstrates a complete machine learning workflow for used-car price prediction, including data cleaning, exploratory data analysis, feature preprocessing, model training, evaluation, and visualization.

On the test set, the Linear Regression model achieved an R² score of approximately **0.753**, while the Random Forest model achieved an R² score of approximately **0.477**.

These results are specific to the dataset, preprocessing approach, models, and train-test split used in this project.

## Project Structure

```text
CodeAlpha_Car_Price_Prediction/
│
├── data/
│   └── car_data.csv
│
├── notebooks/
│   └── car_price_prediction.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Install the required libraries

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

```bash
jupyter notebook
```

### 4. Run the notebook

Open:

```text
notebooks/car_price_prediction.ipynb
```

and run the cells from beginning to end.

## Internship

This project was completed as part of the **CodeAlpha Data Science Internship — Task 3: Car Price Prediction with Machine Learning**.