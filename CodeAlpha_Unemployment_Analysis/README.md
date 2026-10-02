# CodeAlpha - Unemployment Analysis with Python

## Overview

This project analyzes unemployment data from India using Python. The analysis focuses on unemployment trends over time, differences across regions and areas, labour participation, and the changes observed during the COVID-19-affected period.

The project demonstrates how Python can be used for data cleaning, exploratory data analysis, visualization, and extracting meaningful insights from real-world unemployment data.

## Objective

The main objectives of this project are to:

- Analyze unemployment rate data from India.
- Clean and prepare the dataset for analysis.
- Explore unemployment trends over time.
- Compare unemployment rates across different regions.
- Compare urban and rural unemployment.
- Examine the relationship between labour participation and unemployment.
- Investigate changes in unemployment during the COVID-19-affected period.
- Identify patterns and observations from the available data.

## Dataset

The dataset used in this project is **Unemployment in India.csv**.

### Dataset Features

| Feature | Description |
|---|---|
| Region | Name of the Indian region/state |
| Date | Date of the observation |
| Frequency | Frequency of the data |
| Estimated Unemployment Rate (%) | Estimated percentage of unemployed people |
| Estimated Employed | Estimated number of employed people |
| Estimated Labour Participation Rate (%) | Percentage of the working-age population participating in the labour force |
| Area | Urban or Rural |

### Dataset Period

The dataset covers **May 2019 to June 2020** and contains **740 valid records** after cleaning.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Google Colab / Jupyter Notebook

## Data Cleaning

The following preprocessing steps were performed:

- Removed unnecessary whitespace from column names.
- Converted the `Date` column to the appropriate datetime format.
- Identified and removed completely empty rows.
- Reset the DataFrame index after removing empty rows.
- Standardized values in the `Frequency` column.
- Checked the dataset for missing values after cleaning.

## Analysis Performed

### 1. Overall Unemployment Trend

The monthly average unemployment rate was calculated to understand how unemployment changed over time.

The unemployment rate remained around **9–10% during most of the pre-COVID period**, before increasing sharply in April and May 2020.

### 2. Regional Analysis

The average unemployment rate was calculated for each region.

The analysis showed considerable variation between regions. **Tripura and Haryana** recorded the highest average unemployment rates in this dataset, while **Meghalaya** recorded one of the lowest.

### 3. Urban vs Rural Analysis

The average unemployment rate was compared between urban and rural areas.

- Rural: **10.32%**
- Urban: **13.17%**

The urban average was approximately **2.84 percentage points higher** than the rural average during the dataset period.

### 4. Labour Participation Analysis

The average values across the dataset were:

- Average unemployment rate: **11.79%**
- Average estimated employed: approximately **7.20 million**
- Average labour participation rate: **42.63%**

A scatter plot was also used to examine the relationship between labour participation and unemployment. The observations were widely scattered, with no obvious strong relationship visible from the plot.

### 5. COVID-19 Impact

The data was divided into two periods:

- **Pre-COVID:** May 2019 – February 2020
- **COVID-affected period:** March 2020 – June 2020

| Period | Average Unemployment Rate |
|---|---:|
| Pre-COVID | 9.51% |
| COVID Period | 17.77% |

The average unemployment rate increased by approximately **8.26 percentage points** during the COVID-affected period.

The sharpest increase occurred in **April and May 2020**, followed by a considerable decline in June 2020.

### 6. Monthly Pattern

Monthly unemployment patterns were also examined.

Unemployment remained relatively stable across most of the available period, while a sharp increase appeared during April and May 2020. Since the dataset covers only about 14 months, it is not sufficient to establish a recurring seasonal pattern.

## Visualizations

The project includes the following visualizations:

1. Average Unemployment Rate Over Time
2. Average Unemployment Rate by Region
3. Average Unemployment Rate: Urban vs Rural
4. Average Unemployment Rate: Pre-COVID vs COVID Period
5. Labour Participation Rate vs Unemployment Rate

## Key Findings

- Unemployment remained around 9–10% during most of the pre-COVID period.
- A sharp increase in unemployment was observed during the COVID-19-affected period.
- The average unemployment rate increased from **9.51% before March 2020 to 17.77% during March–June 2020**.
- April and May 2020 showed the most significant increase in unemployment.
- There was substantial variation in unemployment rates across different regions.
- Urban areas recorded a higher average unemployment rate than rural areas during the dataset period.
- The average labour participation rate was approximately **42.63%**.
- No obvious strong relationship between labour participation rate and unemployment rate was visible in the scatter plot.
- The available data shows a major employment disruption during the COVID-19 period, but the limited time range does not provide enough evidence to establish a recurring seasonal trend.

## Conclusion

This project analyzed unemployment trends across different regions and areas in India using Python. The analysis identified substantial regional variation and a clear increase in unemployment during the COVID-19-affected period.

The average unemployment rate increased from approximately **9.51% before March 2020 to 17.77% during March–June 2020**, with the sharpest increase occurring in April and May 2020. Urban areas also recorded a higher average unemployment rate than rural areas during the dataset period.

Overall, the project demonstrates how data cleaning, exploratory analysis, grouping, and visualization can be used to identify meaningful patterns in real-world employment data. The findings highlight periods and regions that can be examined further when studying employment conditions.

Because the dataset covers only **May 2019 to June 2020**, longer-term trends and recurring seasonal patterns cannot be established from this dataset alone.

## Project Structure

```text
CodeAlpha_Unemployment_Analysis/
│
├── data/
│   └── Unemployment in India.csv
│
├── notebooks/
│   └── unemployment_analysis.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd CodeAlpha_Unemployment_Analysis
```

### 2. Install the required libraries

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/unemployment_analysis.ipynb
```

Run the notebook cells to reproduce the analysis and visualizations.

## Internship

This project was completed as part of the **CodeAlpha Data Science / Machine Learning Internship**.