# Rwanda Maize Yield Dataset Preparation

## 1. Project Overview

This project focuses on preparing a Rwandan maize yield dataset for future machine learning applications. The work involves acquiring, inspecting, cleaning, transforming and organizing agricultural data.

**Assignment:** Machine Learning Dataset Preparation  
**Dataset:** maize_yield_rwanda_rw.csv  
**Original records:** 1,426  
**Original variables:** 20  
**Target variable:** `yield_t_ha`

## 2. Project Objectives

- Inspect and understand the original dataset.
- Identify missing values, duplicates and unusual observations.
- Clean and preprocess the dataset.
- Create at least five meaningful new features.
- Check data quality and prevent target leakage.
- Divide the dataset into training, validation and testing sets.
- Save the processed datasets for future use.

## 3. Project Structure

```text
GROUP1_MAIZE/
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
├── notebooks/
│   └── 01_acquire_maize_data.ipynb
├── docs/
├── README.md
└── environment.yml
```

## 4. Dataset Information

The original dataset contains 1,426 records and 20 variables. The target variable is `yield_t_ha`, which represents maize yield in tonnes per hectare.

## 5. Data Quality Findings

The initial audit identified:
- 39 missing values across three columns.
- 0 duplicate records.
- Numerical and categorical variables requiring inspection.
- Potential outliers investigated using the Interquartile Range (IQR) method.

Missing numerical values were handled using median imputation. The medians were calculated using the training data only and then applied to the validation and testing data.

## 6. Feature Engineering

Six new features were created:

1. `chemical_fertilizer_kg_ha`
2. `manure_kg_ha`
3. `total_fertilizer_input_kg_ha`
4. `plant_density_per_1000`
5. `soil_ph_category`
6. `altitude_zone`

These features provide additional information about fertilizer application, plant density, soil conditions and farm altitude.

## 7. Dataset Splitting

The dataset was divided using a fixed random seed:

- Training: 70%
- Validation: 15%
- Testing: 15%

The target variable was retained in each processed file. The original dataset was preserved without modification.

## 8. Output Files

The processed datasets are stored in `data/processed/`:

- `maize_train.csv`
- `maize_validation.csv`
- `maize_test.csv`

## 9. Tools and Technologies

- Python
- Anaconda
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn

## 10. Important Note

This project covers dataset preparation only. No machine learning model has been trained as part of this assignment.