# Iris Flower Classification 🌸

## Project Overview

This project uses supervised machine learning to classify Iris flowers into three species based on their physical measurements.

The project demonstrates a complete machine learning workflow, including data exploration, visualization, preprocessing, model training, prediction, and evaluation.

## Objective

The objective of this project is to build a machine learning classification model that can predict the species of an Iris flower from its measurements.

The three species are:

- Iris Setosa
- Iris Versicolor
- Iris Virginica

## Dataset

The dataset contains measurements of Iris flowers.

### Features

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

### Target

- Species

The dataset contains 150 samples, with 50 samples belonging to each species.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning Workflow

The project follows these steps:

1. Load the dataset
2. Understand the dataset structure
3. Check for missing values and duplicate records
4. Perform exploratory data analysis
5. Visualize feature distributions and relationships
6. Separate features and target
7. Split the data into training and testing sets
8. Train a Decision Tree Classifier
9. Generate predictions
10. Evaluate the model using classification metrics
11. Analyze the confusion matrix
12. Interpret the model results

## Model Used

### Decision Tree Classifier

A Decision Tree Classifier was selected because it is suitable for tabular classification data and provides an interpretable way to understand how predictions are made.

The model learns decision rules from the flower measurements and uses those rules to classify new observations into one of the three Iris species.

## Train-Test Split

The dataset was divided into:

- **80% training data**
- **20% testing data**

The training data was used to build the model, while the testing data was used to evaluate its performance on unseen samples.

## Model Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

### Result

The Decision Tree Classifier achieved:

**Test Accuracy: 100%**

This means that the model correctly classified all samples in the test set used for this project.

## Project Structure

```text
CodeAlpha_Iris_Flower_Classification/
│
├── data/
│   └── iris.csv
│
├── notebooks/
│   └── iris_classification.ipynb
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

### 2. Navigate to the project directory

```bash
cd CodeAlpha_Iris_Flower_Classification
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

Open:

```text
notebooks/iris_classification.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model training.

## Conclusion

This project demonstrates the fundamental workflow of a supervised machine learning classification problem. The Iris dataset was explored and prepared, a Decision Tree Classifier was trained, and its predictions were evaluated using multiple classification metrics.

The model achieved **100% accuracy on the test set** used in this project.

## Internship

This project was completed as part of the **CodeAlpha Internship Program**.

**Task 1:** Iris Flower Classification