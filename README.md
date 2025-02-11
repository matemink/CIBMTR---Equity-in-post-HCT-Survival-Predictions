# CIBMTR - Equity in Post-HCT Survival Predictions (Kaggle Competition)

## :rocket: Overview
This competition focuses on improving the prediction of transplant survival rates for **allogeneic Hematopoietic Cell Transplantation (HCT)**, ensuring fairness across diverse patient backgrounds.

## :memo: Description
Current models for HCT survival often fail to address disparities based on **race**, **socioeconomic status**, and **geography**. The challenge is to develop predictive models that improve both **accuracy** and **fairness**, using **synthetic data** to maintain privacy.

## :bar_chart: Evaluation Criteria

### Stratified Concordance Index (C-index)
The **Stratified C-index** evaluates the model's **accuracy** and **fairness** by adjusting for racial disparities, considering each racial group independently.

### Concordance Index (C-index)
Measures the model's ability to rank **survival times** based on **risk scores**.

### Stratified C-index
Adjusts the standard **C-index** to account for **racial stratification**.

## :information_source: Background Information

### What is Allogeneic HCT?
**Allogeneic Hematopoietic Cell Transplantation (HCT)** replaces defective stem cells with healthy ones from a donor, restoring the immune system and helping treat conditions like **leukemia** or **lymphoma**.

---

# :computer: Survival Analysis with CatBoost

This repository contains a **survival analysis** project using machine learning techniques, specifically the `CatBoostRegressor` model. It also includes classical survival models like **Kaplan-Meier** and **Nelson-Aalen** estimators.

## :gear: Features

- **Implementation** of `CatBoostRegressor` for survival analysis.
- **Calculation** and visualization of **Kaplan-Meier survival curves**.
- **Application** of the **Nelson-Aalen estimator** for cumulative hazard function.
- **Custom preprocessing pipeline** for handling missing values and feature selection.
- **Hyperparameter tuning** for improved model performance.
- **Clear data visualization** using **Matplotlib** and **Seaborn**.

## :floppy_disk: Dependencies

- **Python 3.x**
- **CatBoost**
- **Scikit-learn**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**

## :chart_with_upwards_trend: Results

- Survival curves are generated using the **Kaplan-Meier estimator**.
- Model predictions are evaluated with suitable metrics.
- Visualizations of **survival probabilities** and **hazard functions**.
