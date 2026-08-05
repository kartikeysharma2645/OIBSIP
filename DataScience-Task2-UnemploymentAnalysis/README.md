# Unemployment Analysis with Python

## Oasis Infobyte Data Science Internship — Task 2

This project analyzes unemployment trends across different regions of India using Python. The analysis focuses on regional and temporal unemployment patterns, with particular attention to the changes observed during the early COVID-19 period.

## Objective

The objective of this project is to perform exploratory data analysis (EDA) on unemployment data in India, visualize unemployment trends across regions and time periods, and examine the impact of the COVID-19 pandemic on unemployment.

## Dataset

The dataset contains unemployment-related observations for different regions of India from May 2019 to June 2020.

### Key Features

- Region
- Date
- Frequency
- Estimated Unemployment Rate (%)
- Estimated Employed
- Estimated Labour Participation Rate (%)
- Area

After data cleaning, the dataset contains **740 valid records**.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Project Workflow

1. Data Loading
2. Dataset Inspection
3. Data Cleaning and Preprocessing
4. Feature Preparation
5. Exploratory Data Analysis
6. Region-wise Unemployment Analysis
7. Month-wise Unemployment Trend Analysis
8. Time-Series Analysis of Selected Regions
9. Top 10 Regions by Average Unemployment Rate
10. Correlation Analysis
11. COVID-19 Impact Analysis
12. Final Findings and Conclusion

## Key Findings

- **Tripura** recorded the highest average unemployment rate at approximately **28.35%**, followed by **Haryana** at approximately **26.28%**.
- Unemployment remained relatively stable around **9–10%** during most of 2019 and early 2020.
- The average unemployment rate increased sharply during **April and May 2020**, reaching approximately **23.64%** and **24.88%**, respectively.
- The analysis of Maharashtra, Delhi, and Karnataka showed considerable regional differences in unemployment trends during the COVID-19 period.
- No strong linear correlations were observed among the selected employment indicators.
- The average unemployment rate increased from approximately **9.51% during the Pre-COVID period to 17.77% during the defined COVID period**.
- This represents an increase of approximately **86.91%** compared with the Pre-COVID average.
- By June 2020, unemployment had declined considerably from its peak, indicating signs of an early recovery.

## Project Structure

```text
OIBSIP_Task2_Unemployment_Analysis/
│
├── data/
│   └── Unemployment in India.csv
│
├── UnemploymentAnalysis.ipynb
├── README.md
└── requirements.txt