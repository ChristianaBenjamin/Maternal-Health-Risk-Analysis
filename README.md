# 🤰 Maternal-Health-Risk-Analysis

### Exploratory analysis of demographic and clinical factors associated with maternal risk classification

![Maternal Health in Bangladesh](https://github.com/ChristianaBenjamin/Maternal-Health-Risk-Analysis/blob/main/images/maternal-health-banner.png)

## 📌 Project Overview
Maternal health risk can be influenced by a combination of demographic and
clinical characteristics. This project explores patterns in maternal health
measurements across low-, mid-, and high-risk classifications using Python.

The analysis focuses on maternal age, systolic and diastolic blood pressure,
blood sugar, body temperature, and heart rate. Rather than developing a
clinical prediction model, the objective is to identify meaningful patterns
within the dataset and assess what the available data can and cannot support.

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](...)
[![Pandas](https://img.shields.io/badge/Pandas-EDA-150458?logo=pandas)](...)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c)](...)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](...)

## 🎯 Research Question

**What demographic and clinical factors are associated with increased maternal health risk?**

## ❓ Analytical Questions

The analysis investigates the following questions:

- How are low-, mid-, and high-risk maternal records distributed?
- How does maternal age vary across risk classifications?
- How do systolic and diastolic blood pressure vary across risk levels?
- Is blood sugar higher among records classified as higher risk?
- Do body temperature and heart rate show meaningful differences across
  risk groups?
- Which available clinical measurements show the clearest differences across
  maternal risk classifications?
- What relationships exist among the available clinical measurements?
- What patterns could help prioritise clinical monitoring?
- What conclusions can this dataset support, and what can it not establish?

---

## 📊 Dataset

The dataset contains maternal health measurements collected from rural areas
of Bangladesh.

### Data Source
Ahmed, M. (2020). Maternal Health Risk [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5DP5D.

### Variables
| Variable | Description |
|---|---|
| `Age` | Maternal age |
| `SystolicBP` | Systolic blood pressure |
| `DiastolicBP` | Diastolic blood pressure |
| `BS` | Blood sugar measurement |
| `HeartRate` | Maternal heart rate |
| `Temp` | Body temperature |
| `RiskLevel` | Maternal risk classification |

The dataset contains three risk classifications:

- Low risk
- Mid risk
- High risk

## 🧹 Data Quality Assessment

Before analysis, the dataset was assessed for data types, missing values,
duplicate records, categorical consistency, and the plausibility of clinical
measurements.

The dataset does not contain a unique patient identifier. As a result,
duplicate rows were assessed based on the complete set of available
variables.

A substantial number of repeated rows were identified. However, without a
unique identifier, it is not possible to determine whether identical rows
represent duplicate data entries or separate observations with identical
measurements.

Therefore, repeated records were treated cautiously rather than assuming
that every repeated row represented an error.

## 🔍 Exploratory Analysis

### 1. Distribution of Maternal Risk Classification

![Risk Distribution](https://github.com/ChristianaBenjamin/Maternal-Health-Risk-Analysis/blob/main/images/age_risk_distribution.png)

The dataset contains observations classified as low, mid, and high risk.
Understanding the distribution of these categories provides context for
interpreting the subsequent comparisons.

---

### 2. Maternal Age and Risk Classification

![Age and Risk Distribution](https://github.com/ChristianaBenjamin/Maternal-Health-Risk-Analysis/blob/main/images/risk_distribution_across_groups.png)

Risk classification varied across maternal age groups. Older age groups,
particularly the 40+ group, contained a greater proportion of high-risk
records.

However, this represents an association within the dataset and does not
establish that age independently causes increased maternal risk.

---

### 3. Blood Sugar and Maternal Risk

![Blood Sugar by Risk Level](https://github.com/ChristianaBenjamin/Maternal-Health-Risk-Analysis/blob/main/images/blood_sugar_boxplot.png)


Blood sugar showed one of the clearest differences across risk
classifications.

High-risk records had substantially higher blood sugar measurements than
low- and mid-risk records, suggesting that blood sugar is an important
variable to examine when comparing the risk groups in this dataset.

---

### 4. Blood Pressure and Maternal Risk
Both systolic and diastolic blood pressure showed higher central values among
high-risk records.

The distributions also showed overlap between risk groups, indicating that
blood pressure alone does not perfectly distinguish the classifications.

---

## 🔗 Relationships Between Clinical Measurements
![Correlation_heatmap](https://github.com/ChristianaBenjamin/Maternal-Health-Risk-Analysis/blob/main/images/clinical_correlation.png)

Correlation analysis was used to examine relationships among the numerical
clinical variables.

The strongest relationship observed was between systolic and diastolic
blood pressure. This is expected because both measurements describe
different components of the same physiological system.

Blood sugar also showed a positive association with systolic blood pressure,
although the relationship was not strong enough to suggest that one variable
alone explains the other.

Correlation was therefore used as an exploratory tool rather than evidence
of causation.

---

## 💡 Key Findings

### Blood sugar showed a clear difference across risk groups

High-risk records had considerably higher average blood sugar measurements
than low- and mid-risk records.

### Blood pressure was higher among high-risk records

High-risk records showed higher systolic and diastolic blood pressure
distributions compared with the lower-risk groups.

### Age was associated with risk classification

Older maternal age groups were more represented among high-risk records,
particularly the 40+ group.

### Temperature and heart rate showed smaller differences

Compared with blood sugar and blood pressure, body temperature and heart rate
showed relatively modest differences across the risk classifications.

---

## 🏥 Patterns That Could Help Prioritise Clinical Monitoring

The analysis suggests that records exhibiting multiple characteristics
associated with higher-risk classifications—particularly elevated blood
pressure and blood sugar—may warrant closer attention when reviewing the
dataset.

These findings should be interpreted as **patterns for analytical
investigation rather than clinical decision rules**.

The analysis does not establish thresholds for intervention or determine
which variables independently predict maternal risk.

---

## ⚠️ Limitations

- The dataset does not contain a unique patient identifier.
- Repeated rows were identified, but identical records cannot be definitively
  classified as data-entry duplicates without an identifier.
- The analysis is observational and descriptive.
- Associations identified in the analysis do not establish causation.
- The dataset does not allow independent assessment of the clinical criteria
  used to assign `RiskLevel`.
- The findings should not be interpreted as clinical diagnostic or treatment
  recommendations.
- Results describe patterns within this dataset and should not automatically
  be generalised to other populations or healthcare settings.

---

## 🛠️ Tools & Skills

**Python**

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

**Skills demonstrated**

- Data cleaning and quality assessment
- Exploratory data analysis
- Grouping and aggregation
- Cross-tabulation
- Categorical analysis
- Distribution analysis
- Correlation analysis
- Data visualization
- Healthcare data interpretation
- Analytical storytelling
- Communicating data limitations

---

## 📁 Project Structure

```text
maternal-health-risk-analysis/
│
├── data/
│   └── maternal_health_risk.csv
│
├── images/
│   ├── maternal-health-banner.jpg
│   ├── risk_distribution_across_groups.png
│   ├── age-risk-distribution.png
│   ├── blood_sugar_boxplot.png
│   └── clinical_correlation.png
│
├── notebooks/
│   └── maternal_health_risk_analysis.ipynb
│
├── README.md

📓 Full Analysis

The complete exploratory analysis, including data preparation,
visualizations, statistical summaries, and interpretation, is available in
the Jupyter Notebook.

👤 Author

Benjamin Christiana Ifelola

Data Analyst |Aspiring Data Scientist | Healthcare Professional

GitHub: https://github.com/ChristianaBenjamin
LinkedIn: https://www.linkedin.com/in/christiana-benjamin-a54495163/
