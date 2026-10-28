# Providence Vendor Payment Analysis

### Exploratory Data Analysis of Public Expenditure Data

A Python-based data analytics project exploring municipal expenditure records published by the City of Providence. This project examines payment distributions, payment methods, spending trends, vendor concentration, expenditure programmes, and unusual transaction patterns to derive meaningful insights from public financial data.

## Project Overview

Public expenditure datasets contain large volumes of transactions across vendors, departments, programmes, funding sources, and payment methods. Analysing these records can help reveal how payments are distributed, identify major expenditure areas, and highlight patterns that may require further investigation.

This project applies data cleaning, exploratory data analysis (EDA), descriptive statistics, and data visualisation to the City of Providence Expenditures dataset.

The analysis focuses on understanding recorded payment activity and identifying unusual patterns without assuming that outliers or anomalies indicate errors or wrongdoing.

## Project Objectives

- Inspect the structure, data types, and quality of the expenditure dataset.
- Clean the data by handling duplicates, missing descriptions, and date fields.
- Analyse payment amount distributions using descriptive statistics.
- Compare transaction counts and payment values across payment methods.
- Examine annual and monthly payment trends.
- Identify leading vendors, departments, expense accounts, funding sources, and programmes by payment value.
- Investigate negative payments, extreme values, and unusual transaction patterns.
- Communicate findings through clear, evidence-based visualisations.

## Dataset

**Dataset:** City of Providence Expenditures

**Source:** City of Providence via Data.gov

**Source link:** https://catalog.data.gov/dataset/city-of-providence-expenditures

The dataset contains public expenditure transaction records, including fields related to payment dates, payment amounts, vendors, departments, programmes, expense accounts, funding sources, entry types, payment methods, and payment status.

### Dataset Summary

| Metric | Value |
|---|---:|
| Original records | 370,959 |
| Records after deduplication | 370,944 |
| Original columns | 17 |
| Columns in the cleaned dataset | 20 |
| Exact duplicate records removed | 15 |
| Exact duplicates remaining after cleaning | 0 |

The cleaned dataset includes additional date-related fields used for time-based analysis.

## Tools and Technologies

- **Python** — Data analysis and transformation
- **Pandas** — Data cleaning, manipulation, and aggregation
- **NumPy** — Numerical computations
- **Matplotlib** — Data visualisation
- **Seaborn** — Statistical visualisation
- **Plotly** — Interactive visualisation, where applicable
- **Google Colab** — Notebook development and execution

## Methodology

### 1. Data Loading and Inspection

Loaded the expenditure dataset into a Pandas DataFrame and examined its structure, column names, data types, record count, descriptive statistics, and missing values.

### 2. Data Cleaning

- Identified and removed 15 exact duplicate records.
- Converted relevant date fields into appropriate date formats.
- Prepared payment amount fields for numerical analysis.
- Added date-related features to support monthly and annual analysis.
- Used `"Unknown"` as a transparent label for missing invoice descriptions rather than inferring unavailable information.
- Retained negative payment amounts and extreme values for further analysis.

### 3. Exploratory Data Analysis

Analysed payment distributions, summary statistics, payment methods, entry types, monthly and annual trends, vendor concentration, and expenditure categories.

### 4. Outlier and Anomaly Investigation

Used the Interquartile Range (IQR) method to identify statistically unusual payment amounts. Examined unusual transaction patterns and date concentrations to identify areas requiring additional validation.

Outliers were retained because statistical extremity alone does not establish that a transaction is incorrect.

### 5. Data Visualisation

Used charts to communicate distributions, comparisons, trends, concentration patterns, and unusual observations in a clear and interpretable format.

## Key Findings

### 1. Payment Amount Distribution

- Mean payment amount: approximately **$6,725.57**.
- Median payment amount: approximately **$364.65**.
- Skewness: approximately **36.14**.

The mean is substantially higher than the median, and the distribution is strongly right-skewed. This indicates that a relatively small number of large recorded payments strongly influence the average.

### 2. Payment Method Analysis

System checks account for:

- **88.52%** of recorded transactions.
- **95.99%** of net recorded payment value.

E-payables account for the remaining 11.48% of transactions and 4.01% of net recorded payment value. System checks therefore dominate both transaction volume and recorded value.

### 3. Annual Payment Trends

Recorded payment totals generally increased between 2017 and 2025, although the trend was not continuous.

- Recorded payments decreased by **10.46% in 2020** compared with 2019.
- Recorded payments decreased by **1.51% in 2024** compared with 2023.

These changes identify periods for further analysis but do not, by themselves, explain the reasons behind the declines.

### 4. Vendor Concentration

The top 10 vendors account for approximately **36.75% of net recorded payment value**.

This indicates a substantial concentration of recorded expenditure among a limited group of vendors. Vendor concentration should be interpreted alongside contract details, services provided, and supporting records.

### 5. Programme Expenditure

Regular Elementary/Secondary Education Programs represents the largest recorded payment total among the programmes examined, followed by Special Education and G&A Services.

This highlights the importance of programme-level analysis when understanding how public expenditure is distributed.

### 6. Unusual Transaction Concentration

An unusual concentration was observed in December 2018:

- Total December 2018 transactions: **14,066**
- Transactions recorded on 21 December 2018: **12,277**
- Share of December transactions recorded on that day: **87.3%**

This concentration warrants validation against the original records, payment dates, and possible batch-processing activity. The pattern alone does not establish its cause.

## Visualisations

The following visualisations summarise the major findings of the analysis.

### 1. Payment Amount Distribution

<img width="939" height="308" alt="image" src="https://github.com/user-attachments/assets/446139ef-bf64-44d4-b75d-75cac3ccfcf7" />


The distribution is strongly right-skewed, with most positive payments concentrated at lower values and a small number of large payments extending the upper tail.

### 2. Payment Method Analysis

<img width="938" height="975" alt="image" src="https://github.com/user-attachments/assets/3eb329fc-d163-4a28-af55-4da0561b0ce3" />


System checks account for the majority of both transaction volume and net recorded payment value, while e-payables represent a smaller share.

### 3. Annual Spending Trends

<img width="939" height="466" alt="image" src="https://github.com/user-attachments/assets/3b0f7a0e-43ba-47c8-b550-f91d5c01ec72" />


Recorded payment totals generally increased from 2017 to 2025, with notable declines in 2020 and 2024.

### 4. Monthly Spending Trends

<img width="938" height="509" alt="image" src="https://github.com/user-attachments/assets/008c0490-b638-4da5-ac2e-37fbece413b4" />


Monthly payment values fluctuate over time, revealing periods of higher and lower recorded expenditure rather than a uniform spending pattern.

### 5. Vendor Concentration

<img width="938" height="506" alt="image" src="https://github.com/user-attachments/assets/6fbe7715-0b51-4285-91f6-b67267fd5c14" />


The top 10 vendors account for approximately 36.75% of net recorded payment value, highlighting the concentration of recorded expenditure among major vendors.

### 6. Programme Expenditure

<img width="936" height="461" alt="image" src="https://github.com/user-attachments/assets/32094814-a7f2-48c4-9523-286c452517f3" />


Regular Elementary/Secondary Education Programs has the highest recorded payment total among the programmes analysed, followed by Special Education and G&A Services.

### 7. Negative Payments and Outliers

<img width="938" height="622" alt="image" src="https://github.com/user-attachments/assets/2c303e33-cd7d-43d5-849f-939747b10fd1" />


Negative payment amounts and statistically extreme values require contextual interpretation. Their presence alone does not establish an error or irregularity.

### 8. December 2018 Transaction Concentration

<img width="1032" height="422" alt="image" src="https://github.com/user-attachments/assets/bff56b32-8856-4098-a758-6fd079f9a02b" />


A single date accounts for approximately 87.3% of recorded December 2018 transactions. This unusual concentration should be investigated and validated against the original source records.

## Limitations

- Missing invoice descriptions cannot be reliably reconstructed from the available fields.
- Extreme values may represent legitimate transactions and were not automatically removed.
- Negative payment amounts cannot be assigned a definitive meaning based on their values alone.
- Unusual transaction concentrations require additional source validation and contextual information.
- The dataset describes recorded expenditure but does not independently establish the reasons for spending patterns or changes over time.
- Findings reflect the dataset and analysis performed; they should be reconfirmed against a fresh execution of the final notebook.

## Conclusion

This project demonstrates how Python-based data analytics can be applied to public expenditure records to understand payment distributions, compare payment methods, analyse spending trends, and identify areas requiring further investigation.

The analysis highlights the influence of large payments on average values, the concentration of recorded expenditure among major vendors, changes in annual payment totals, and an unusual transaction concentration in December 2018.

By combining data cleaning, descriptive statistics, exploratory analysis, and visualisation, the project turns a large transactional dataset into structured findings that can support further investigation and more informed analysis of public financial data.

## Repository Contents

- **Jupyter Notebook:** Data cleaning, exploratory analysis, calculations, and visualisations.
- **README.md:** Project overview, methodology, key findings, and visual summaries.

## Author

**Christy Rose**

Data Analytics | Python | Pandas | NumPy | Data Visualisation

---

**Data Source:** [City of Providence Expenditures — Data.gov](https://catalog.data.gov/dataset/city-of-providence-expenditures)
