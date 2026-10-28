# Providence Vendor Payment Analysis

### Python-Powered Financial Data Analytics

A comprehensive Python-based data analytics project analysing public expenditure records to understand payment distributions, vendor concentration, spending trends, and unusual transaction patterns through data preparation, statistical analysis, and visualisation.

**Author:** Christy Rose

**Tools & Technologies:** Python · Pandas · NumPy · Matplotlib · Seaborn · Plotly · Google Colab

---

## 📌 Project Overview

Public expenditure datasets contain large volumes of transactions across vendors, departments, expenditure programmes, funding sources, and payment methods. Analysing these records can help identify spending patterns, understand payment distributions, and highlight areas that may require further investigation.

This project analyses the **City of Providence Expenditures** dataset using Python, data cleaning, exploratory data analysis (EDA), descriptive statistics, and visualisation.

The project focuses on understanding recorded payment behaviour and identifying unusual patterns while distinguishing statistical observations from conclusions that require further evidence.

## 🎯 Project Objectives

- Inspect the structure and quality of public expenditure data.
- Clean selected fields and prepare payment amounts and dates for analysis.
- Identify and remove confirmed exact duplicate records.
- Analyse payment amount distributions and statistical outliers.
- Compare payment methods using transaction counts and recorded payment values.
- Examine annual and monthly expenditure patterns.
- Identify leading vendors and expenditure programmes.
- Investigate negative payments, large transactions, and unusual date concentrations.
- Communicate findings through visualisations and evidence-based recommendations.

## 📂 Dataset

**Dataset:** City of Providence Expenditures

**Source:** City of Providence, published through Data.gov.

**Official dataset:** [City of Providence Expenditures — Data.gov](https://catalog.data.gov/dataset/city-of-providence-expenditures)

The source dataset contains 17 original columns, including:

- Payment Date
- Payment Amount
- Vendor/Payee
- Payment Method
- Invoice Description
- Department and Programme Accounts
- Funding Source Account
- Payment Status and Invoice ID

The project report records **370,944 rows and 20 columns** in the cleaned dataset, including derived year and month fields. These figures should be confirmed by running the final notebook from beginning to end.


## 🛠️ Tools and Technologies

| Tool | Purpose |
|---|---|
| Python | Data preparation and analysis |
| Pandas | Data cleaning, grouping, and tabular analysis |
| NumPy | Numerical operations and calculations |
| Matplotlib | Static charts and visualisations |
| Seaborn | Statistical visualisations |
| Plotly | Interactive visualisations, where used |
| Google Colab | Notebook development and execution |

## 🔄 Project Workflow

1. **Data loading and inspection** — examined the dataset's dimensions, column names, data types, descriptive statistics, and missing values.
2. **Data cleaning** — prepared payment amounts, parsed dates, standardised selected categories, and investigated exact duplicates.
3. **Feature engineering** — derived payment year and month fields for time-based analysis.
4. **Exploratory data analysis** — examined payment distributions, payment methods, trends, vendors, programmes, and negative values.
5. **Statistical analysis** — used descriptive statistics and IQR-based outlier detection to identify unusual observations for review.
6. **Visualisation** — used charts to communicate important patterns and comparisons.
7. **Interpretation and recommendations** — documented findings, limitations, and areas requiring further validation.


## 📈 Visualisations and Key findings
### Distribution of Positive Payment Amounts
<img width="939" height="308" alt="image" src="https://github.com/user-attachments/assets/72fb5d2c-9861-4252-8475-e080b39b195a" />
The distribution is strongly right-skewed: most positive payments are relatively small, while a few very large payments create a long right tail.

### Spread of Positive Payment Amounts
<img width="938" height="976" alt="image" src="https://github.com/user-attachments/assets/1cd041d6-482a-454d-9b9c-986aaf7e7f59" />

<img width="938" height="517" alt="image" src="https://github.com/user-attachments/assets/8d431d25-65d1-44a0-be98-c6bcd40821e3" />
<img width="936" height="582" alt="image" src="https://github.com/user-attachments/assets/4d162f40-7cc9-4164-b388-a1a5f10b4e75" />
<img width="939" height="466" alt="image" src="https://github.com/user-attachments/assets/826db086-41ab-44ae-8819-917e07db6b5f" />
<img width="938" height="506" alt="image" src="https://github.com/user-attachments/assets/40194843-dbe3-4460-80ee-157cd591db70" />
<img width="938" height="464" alt="image" src="https://github.com/user-attachments/assets/972e3edc-d90f-4a9a-a5c9-03c7676b896f" />
<img width="939" height="398" alt="image" src="https://github.com/user-attachments/assets/6633aeae-cb11-4d0a-ac3a-d59fa2941183" />
<img width="940" height="444" alt="image" src="https://github.com/user-attachments/assets/af8d8a67-fe92-4995-bd17-082ef778cfb0" />
<img width="938" height="559" alt="image" src="https://github.com/user-attachments/assets/cc195cdd-77fd-4a54-af3d-0f2a285444cb" />
<img width="938" height="509" alt="image" src="https://github.com/user-attachments/assets/87fee766-aca1-40fd-9b6f-5b9d9cf94183" />
<img width="938" height="463" alt="image" src="https://github.com/user-attachments/assets/c09a5605-4001-4d6a-ba25-4061eecfa1d5" />
<img width="938" height="463" alt="image" src="https://github.com/user-attachments/assets/d7d3b14a-9504-40c7-bbe8-34ee6fff00eb" />
<img width="936" height="461" alt="image" src="https://github.com/user-attachments/assets/a1d76ee6-0a61-4681-8079-ca1e13b88c3a" />
<img width="938" height="622" alt="image" src="https://github.com/user-attachments/assets/5789b556-02c0-40cb-8d96-189302877ea6" />
<img width="938" height="422" alt="image" src="https://github.com/user-attachments/assets/4357a36c-b598-4668-8f8c-140b76383294" />
<img width="938" height="622" alt="image" src="https://github.com/user-attachments/assets/19062391-a713-4e04-883c-bdbe66a5b8ea" />
<img width="940" height="566" alt="image" src="https://github.com/user-attachments/assets/6eb84e33-effe-4421-b2c2-95d0be69dd0d" />
<img width="938" height="422" alt="image" src="https://github.com/user-attachments/assets/f3b66381-e1a6-474e-98ed-35a0f3b4cd3a" />










## 💡 Recommendations

- Re-run the complete notebook to verify row counts, duplicate counts, date parsing, and reported statistics.
- Review unusually large positive payments against supporting source records before classifying them as errors.
- Analyse negative payments separately to investigate possible reversals, refunds, or adjustments.
- Distinguish gross positive payment totals from net recorded payment totals where relevant.
- Clearly label incomplete years when comparing annual spending.
- Report missing invoice descriptions transparently; placeholder values such as `Unknown` do not recover the original information.
- Ensure that notebook outputs and any interactive dashboard use consistent definitions and totals.

## ⚠️ Limitations

- The analysis is based on published expenditure records and cannot independently verify the business purpose or validity of each payment.
- Missing invoice descriptions limit the interpretation of some transactions.
- The meaning of negative amounts cannot be confirmed from the sign alone.
- Partial years may distort year-to-year comparisons.
- IQR-based outlier detection identifies statistically unusual values but does not prove fraud or incorrect payment.
- Reported figures must be checked against a fresh, complete execution of the final notebook.


## ▶️ How to Run the Project

1. Open the notebook in the `notebooks/` folder.
2. Download the source dataset from the official [Data.gov dataset page](https://catalog.data.gov/dataset/city-of-providence-expenditures).
3. Upload the CSV to your Google Colab session or configure the notebook to read it from your own storage.
4. Install any required libraries that are not already available.
5. Run the notebook cells in order, from data loading through analysis and visualisation.
6. Compare the final outputs with the figures documented in this README.

## 📚 References

- [City of Providence Expenditures — Data.gov](https://catalog.data.gov/dataset/city-of-providence-expenditures)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Plotly Python Documentation](https://plotly.com/python/)

## 👩‍💻 Author

**Christy Rose**

This project demonstrates a practical application of Python-based data cleaning, exploratory analysis, statistical reasoning, and visual communication using publicly available expenditure data.
