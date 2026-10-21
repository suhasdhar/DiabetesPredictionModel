# Diabetes Prediction Model

A machine learning model that predicts whether a person has prediabetes or diabetes (`Diabetes_binary`) from 21 health survey answers, such as BMI, blood pressure, cholesterol, physical activity, general health, age and income.

## Data source

**CDC Diabetes Health Indicators** dataset, from the UCI Machine Learning Repository.

- UCI page: https://archive.ics.uci.edu/dataset/891/cdc+diabetes+health+indicators (dataset id `891`)
- DOI: [10.24432/C53919](https://doi.org/10.24432/C53919)
- Original source: the CDC's [Behavioral Risk Factor Surveillance System (BRFSS) 2014](https://www.cdc.gov/brfss/annual_data/annual_2014.html), an annual telephone health survey of U.S. adults
- Size: 253,680 survey responses, 21 features and 1 binary target
- License: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

The target is imbalanced: only about 14% of respondents have prediabetes or diabetes.

### Getting the data

```python
# pip install ucimlrepo
from ucimlrepo import fetch_ucirepo

cdc = fetch_ucirepo(id=891)
X = cdc.data.features   # 21 feature columns
y = cdc.data.targets    # Diabetes_binary (0 = no diabetes, 1 = prediabetes or diabetes)
```

## Citation

> CDC Diabetes Health Indicators [Dataset]. (2023). UCI Machine Learning Repository. https://doi.org/10.24432/C53919
