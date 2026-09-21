# SWYNEX Data Preparation – Healthcare Stroke Dataset

## Project Overview

This project focuses on data preparation and cleaning of a healthcare stroke prediction dataset.

The dataset contains information about patients, including age, hypertension, heart disease, work type, average glucose level, BMI, smoking status, and stroke information.

## Dataset Information

- Records: 5,110
- Columns: 12
- Domain: Healthcare
- Task: Data Preparation and Cleaning

## Data Cleaning Performed

### 1. Missing Values

The `bmi` column contained missing values.

Missing BMI values were replaced using the median BMI:

```python
df['bmi'] = df['bmi'].fillna(df['bmi'].median())