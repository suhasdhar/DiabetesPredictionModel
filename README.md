# Diabetes Prediction Model

A step-by-step machine learning project that predicts diabetes from health exam and lab data. The project covers the full workflow: feature identification, building the feature table, EDA, feature engineering, a base model, model fitting, metrics, recalibration and optimization, and final evaluation.

## Data source

**National Health and Nutrition Examination Survey (NHANES), 2017–2018 cycle**, run by the CDC's National Center for Health Statistics (NCHS).

- Cycle page: https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2017
- NHANES combines home interviews with physical exams and lab tests done in mobile exam centers, on a nationally representative sample of the U.S. population.
- License: NCHS data are in the public domain. Under the NCHS data use agreement, the data may be used only for statistical analysis, and no one may try to identify the people in it.

### Files in `Data/`

These are the original NHANES files with readable column names. Every table shares a `person_id` column (NHANES `SEQN`), which is used to join them.

| File | Original NHANES file | Rows | What it contains |
|---|---|---|---|
| `demographics.csv` | `DEMO_J` | 9,254 | Age, sex, race/ethnicity, education, income, survey weights |
| `body_measures.csv` | `BMX_J` | 8,704 | Height, weight, BMI, waist circumference |
| `blood_pressure.csv` | `BPX_J` | 8,704 | Systolic and diastolic blood pressure readings, pulse |
| `diabetes_questionnaire.csv` | `DIQ_J` | 8,897 | Doctor-diagnosed diabetes, insulin and medication use, related history |
| `bp_cholesterol_questionnaire.csv` | `BPQ_J` | 6,161 | Diagnosed high blood pressure and cholesterol, and whether taking medicine for each |
| `hba1c.csv` | `GHB_J` | 6,401 | Glycohemoglobin (HbA1c, %) |
| `fasting_glucose.csv` | `GLU_J` | 3,036 | Fasting plasma glucose (fasting subsample) |
| `insulin.csv` | `INS_J` | 3,036 | Fasting insulin (fasting subsample) |
| `total_cholesterol.csv` | `TCHOL_J` | 7,435 | Total cholesterol |
| `hdl_cholesterol.csv` | `HDL_J` | 7,435 | HDL cholesterol |
| `triglycerides_ldl.csv` | `TRIGLY_J` | 3,036 | Triglycerides and LDL cholesterol (fasting subsample) |
| `data_dictionary.csv` | — | 180 | Maps every readable column name to its original NHANES code and description |

Some tables cover only part of the sample. For example, fasting glucose, insulin and triglycerides were measured only in the fasting subsample of about 3,000 people.

## Citation

> Centers for Disease Control and Prevention (CDC), National Center for Health Statistics (NCHS). National Health and Nutrition Examination Survey Data, 2017–2018. Hyattsville, MD: U.S. Department of Health and Human Services, Centers for Disease Control and Prevention.
