# Diabetes-Missing-Data# Diabetes Missing Data Handling

## Description
This project demonstrates how to identify and handle missing values in a diabetes dataset using Python and Google Colab.

## Dataset
The dataset contains diabetes-related health information such as:
- Pregnant
- Glucose
- Diastolic_BP
- Skin_Fold
- Serum_Insulin
- BMI
- Diabetes_Pedigree
- Age
- Class

## Technologies Used
- Python
- Pandas
- Scikit-learn
- Google Colab

## Steps
1. Load the dataset.
2. Check for missing values.
3. Handle missing values using Mean Imputation.
4. Verify that missing values are removed.
5. Save the cleaned dataset.

## Code
```python
import pandas as pd
from sklearn.impute import SimpleImputer

df = pd.read_csv('Diabetes Missing Data.csv')

imputer = SimpleImputer(strategy='mean')
df[df.columns] = imputer.fit_transform(df)

df.to_csv('Diabetes_Cleaned.csv', index=False)
#Author Rajneet kaur
