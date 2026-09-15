# Child Mortality Determinants Analysis

## Integrating DHS, WHO, WASH, Nutrition, Immunization, Maternal Health and Climate Data

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Data Science](https://img.shields.io/badge/Field-Data%20Science-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Analysis-green)
![DHS](https://img.shields.io/badge/Data-DHS-red)
![WHO](https://img.shields.io/badge/Data-WHO-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)


---
## 📌 Project Overview

Child mortality remains one of the most important indicators of population health and development. Although global child mortality has declined over the past decades, substantial inequalities continue to exist across countries and populations.

This project investigates the **determinants of child mortality** by integrating data from multiple sources, including:

- **Demographic and Health Surveys (DHS)**
- **World Health Organization (WHO)**
- **UNICEF**
- **World Bank**
- **CHIRTS-ERA5 climate datasets**
- Other relevant environmental, demographic and socioeconomic sources

The project combines **health, demographic, socioeconomic, environmental and climate information** to identify factors associated with mortality among children, particularly children under five years of age.

The ultimate goal is to develop a reproducible data science pipeline that can be used to:

1. Understand patterns and trends in child mortality.
2. Identify major risk factors and determinants.
3. Examine the relationship between child mortality and environmental/climate conditions.
4. Integrate datasets from multiple sources.
5. Develop statistical and machine learning models for mortality risk analysis and prediction.
6. Generate evidence-based insights that can support public health research and decision-making.

---

# 🎯 Research Objectives

## General Objective

To investigate and model the demographic, health, socioeconomic, environmental and climatic determinants of child mortality using integrated multi-source datasets.

## Specific Objectives

### 1. Data Collection

Collect relevant child mortality and determinant indicators from reliable international and national data sources.

### 2. Data Integration

Integrate datasets from:

- DHS
- WHO
- UNICEF
- World Bank
- CHIRTS
- ERA5
- Other relevant sources

using common geographic, temporal and demographic dimensions.

### 3. Data Quality Assessment

Assess the quality of the collected datasets by identifying:

- Missing values
- Duplicate records
- Outliers
- Inconsistent formats
- Invalid observations
- Temporal inconsistencies
- Geographic inconsistencies

### 4. Exploratory Data Analysis

Explore:

- Child mortality trends
- Geographic variations
- Temporal patterns
- Health disparities
- WASH conditions
- Nutritional status
- Immunization coverage
- Maternal health
- Climate conditions
- Socioeconomic factors

### 5. Determinant Analysis

Investigate the relationships between child mortality and potential explanatory variables such as:

- Water and sanitation
- Malnutrition
- Immunization
- Maternal health
- Healthcare access
- Poverty and socioeconomic conditions
- Disease burden
- Temperature
- Rainfall
- Other climatic and environmental factors

### 6. Predictive Modeling

Develop statistical and machine learning models to estimate or predict child mortality risk.

Potential algorithms include:

- Linear Regression
- Logistic Regression
- Random Forest
- XGBoost
- Gradient Boosting
- Support Vector Machines
- Neural Networks

### 7. Model Interpretation

Use explainable AI and feature importance techniques to identify the variables that contribute most strongly to mortality predictions.

---

# 📊 Key Outcome Variable

The primary outcome variable for the project is:

### Under-Five Mortality Rate

**Definition:**

> Probability of dying before reaching age five, expressed per 1,000 live births.

This will serve as the primary indicator for measuring child mortality.

Other mortality indicators may be used for supplementary analysis, including:

- Neonatal mortality rate
- Infant mortality rate
- Stillbirth rate
- Number of under-five deaths

---

# 📈 Key Explanatory Variables

The project considers multiple categories of determinants.

## 1. Water, Sanitation and Hygiene (WASH)

Key indicators include:

- Basic drinking-water services
- Safely managed drinking-water services
- Basic sanitation services
- Safely managed sanitation services
- Basic handwashing facilities
- Open defecation
- Safely treated domestic wastewater

---

## 2. Child Nutrition

Key indicators include:

- Stunting prevalence
- Wasting prevalence
- Severe wasting prevalence
- Underweight prevalence
- Overweight prevalence

These indicators will help assess the relationship between nutritional conditions and child mortality.

---

## 3. Immunization

Key vaccination indicators include:

- DTP3 coverage
- MCV1 coverage
- MCV2 coverage
- PCV3 coverage
- Polio vaccination coverage
- BCG coverage
- Hepatitis B vaccination coverage
- Rotavirus vaccination coverage

---

## 4. Maternal Health

Variables include:

- Births attended by skilled health personnel
- Maternal mortality ratio
- Antenatal and reproductive health indicators where available

---

## 5. Reproductive Health

Potential indicators include:

- Adolescent birth rate
- Family planning needs satisfied with modern methods

---

## 6. Disease Burden

Potential indicators include:

- Malaria incidence
- HIV incidence
- Tuberculosis incidence
- Other relevant infectious diseases

---

## 7. Healthcare Access

Potential indicators include:

- UHC Service Coverage Index
- Medical doctors per 10,000 population
- Nursing and midwifery personnel per 10,000 population
- Essential medicines availability

---

## 8. Environmental and Climate Variables

Climate and environmental variables will be derived from datasets such as:

- CHIRTS
- ERA5

Potential variables include:

- Maximum temperature
- Minimum temperature
- Mean temperature
- Temperature anomalies
- Rainfall/precipitation
- Extreme temperature events
- Climate variability

Environmental variables will be analyzed to determine whether climatic conditions are associated with changes in child mortality.

---

# 🌍 Geographic Scope

The initial analysis focuses on countries and populations for which compatible DHS, WHO and climate data are available.

The geographic scope may be expanded depending on:

- Data availability
- Temporal coverage
- Geographic resolution
- Compatibility between datasets

Where possible, analysis will be conducted at multiple geographic levels, including:

- Country
- Region
- DHS survey cluster
- Other compatible administrative/geographic units

---

# 🗂️ Data Sources

## Demographic and Health Surveys (DHS)

DHS datasets provide detailed demographic, household, maternal and child health information.

Main areas of interest include:

- Child health
- Mortality
- Maternal health
- Household characteristics
- Water and sanitation
- Nutrition
- Immunization
- Socioeconomic characteristics

---

## World Health Organization (WHO)

WHO Global Health Observatory indicators provide internationally comparable health statistics.

Key indicator groups include:

- Child mortality
- Maternal mortality
- Immunization
- Nutrition
- WASH
- Disease burden
- Healthcare coverage
- Environmental health

---

## CHIRTS-ERA5

Climate data will be used to investigate the relationship between climate conditions and child mortality.

Relevant climate variables include:

- Daily maximum temperature
- Daily minimum temperature
- Temperature variability
- Precipitation
- Extreme climate conditions

---

# 🏗️ Project Architecture

The project follows an end-to-end data science workflow:

```text
                    ┌─────────────────────┐
                    │     Data Sources    │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
            DHS              WHO          CHIRTS/ERA5
              │                │                │
              └────────────────┼────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Data Collection   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Data Cleaning     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Data Validation   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Data Transformation │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  Data Integration   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │        EDA          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Feature Engineering │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Statistical Analysis│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Machine Learning    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Model Interpretation│
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Insights & Reporting│
                    └─────────────────────┘
