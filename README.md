Inflation and Monetary Policy

Advanced Python Project – VT25

Project Overview
-----------------

Monetary policy is often analyzed using the Taylor rule, which describes how policy rates respond to inflation. 
However, rather than estimating a full Taylor rule, this project explores whether a simpler regression-based approach 
can capture the relationship between inflation and the policy rate when accounting for time lags.

The objective is to investigate whether lagged policy rates are associated with current inflation, and how this 
relationship varies across different lag lengths.

Research Question
-----------------

Is there a statistically observable relationship between inflation and lagged policy rates, 
and how does this relationship depend on time lags?

Data
-----------------

The analysis uses publicly available Swedish macroeconomic data:

- Inflation (annual CPI-based measure)

- Policy rate (styrränta) from Sveriges Riksbank

The data is retrieved via API and aligned at a monthly frequency. Missing values occur naturally 
due to differences in data availability over time and are handled through filtering.

Process
-----------------
1. Exploratory Data Analysis (EDA)

Time series visualization of inflation and the policy rate

Summary statistics and initial correlation analysis

Visual inspection of structural changes over time

2. Feature Engineering

Construction of lagged policy rate variables (e.g. 3, 12, 24 months)

Correlation analysis to identify potentially relevant lags

3. Model

A linear regression model is used with inflation as the dependent variable and lagged policy 
rates as explanatory variables.

This approach is intentionally simple and exploratory. The goal is not causal inference, but to 
quantify associations consistent with the delayed transmission of monetary policy.

4. Evaluation

Model performance is assessed using:

R² (coefficient of determination)

(Mean Squared Error (MSE))

Low explanatory power is expected given the multifactor nature of inflation.

Dashboard
--------------

An interactive dashboard built with Plotly presents:

- Time series of inflation and the policy rate

- Scatter plots illustrating lagged relationships

- Regression results summarized in tables

Short interpretative text to guide analysis

The dashboard is exported as a standalone HTML file.

Key Findings
---------------

- The relationship between policy rates and inflation is weak but generally negative.
- Stronger associations appear at longer lags, consistent with monetary policy transmission delays. 
- Inflation is influenced by many factors beyond the policy rate, limiting explanatory power

Limitations and Extensions
- The model does not account for other macroeconomic variables (e.g. output gap, unemployment)
- No causal interpretation is claimed


Files Included
---------------

Jupyter notebook containing data retrieval, analysis, and modeling

Interactive dashboard (.html)


Author:

Sara Stigmar
Advanced Python Workshops – Lund University Finance Society
