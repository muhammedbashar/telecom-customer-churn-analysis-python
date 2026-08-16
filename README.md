

# Customer Churn Analysis using Python

_An end-to-end Exploratory Data Analysis (EDA) project to identify the key drivers of customer churn, uncover high-risk customer segments, and provide data-driven business recommendations to improve customer retention using Python._


---
##   Table of Contents

- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#project-objectives">Project Objectives</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-assessment--cleaning">Data Assessment & Cleaning</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#key-insights">Key Insights</a>
- <a href="#business-recommendations">Business Recommendations</a>
- <a href="#project-outputs">Project Outputs</a>
- <a href="#results--conclusion">Results & Conclusion</a>
- <a href="#future-work">Future Work</a>
- <a href="#author--contact">Author & Contact</a>


---
<h2><a class="anchor" id="overview"></a>Overview</h2>

Customer retention is one of the most important challenges faced by subscription-based businesses. Acquiring new customers is significantly more expensive than retaining existing ones, making customer churn analysis a critical business activity.

This project performs an end-to-end Exploratory Data Analysis (EDA) on the IBM Telco Customer Churn dataset to identify the major factors influencing customer churn. The analysis focuses on discovering customer characteristics associated with higher churn risk and translating analytical findings into actionable business recommendations.


---
<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Customer churn directly impacts revenue, customer lifetime value, and business growth. Understanding why customers leave is essential for designing effective retention strategies.

This project aims to answer the following business questions:

- Why are customers leaving the company?
- Which customer groups are most likely to churn?
- What customer characteristics contribute most to churn?
- What actions can the business take to improve customer retention?


---
<h2><a class="anchor" id="project-objectives"></a>Project Objectives</h2>

- Assess the quality and structure of the dataset.
- Clean and prepare the data for analysis.
- Perform univariate analysis to understand individual feature distributions with respect to churn.
- Perform numerical analysis to study customer behavior across numerical variables with respect to churn.
- Conduct bivariate analysis to identify relationships between customer characteristics combinations and churn.
- Discover the most influential drivers of customer churn.
- Provide data-driven recommendations to reduce churn and improve customer retention.


---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

**Dataset:** IBM Telco Customer Churn Dataset

Dataset Summary:

- Original Records: **7,043 customers**
- Records after Data Cleaning: **7,032 customers**
- Features: **21 columns**
- Target Variable: **Churn**

The dataset contains customer demographic information, subscription details, internet services, contract types, billing information, payment methods, tenure, monthly charges, total charges, and churn status.


---
<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- **Programming Language:** Python
- **Environment:** Google Colab
- **Libraries:**
  - Pandas
  - NumPy
  - Matplotlib
  - Seaborn
- **Version Control:** Git & GitHub

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>


```
customer-churn-analysis-python/
│
├── README.md
│
├── data/
│   └── dataset.csv
│
├── docs/
│   ├── customer_churn_analysis.pdf
│   ├── customer_churn_analysis_full.pdf
│   └── customer_churn_analysis_project_report.pdf
│
├── notebooks/
│   ├── full-analysis/
│   │   └── customer_churn_analysis_full.ipynb
│   │
│   └── portfolio/
│       └── customer_churn_analysis.ipynb
│
├── outputs/
│   ├── univariate/
│   │   ├── churn_distribution.png
│   │   ├── contract_vs_churn.png
│   │   ├── internet_service_vs_churn.png
│   │   └── payment_method_vs_churn.png
│   │
│   ├── bivariate/
│   │   ├── contract_vs_tenure.png
│   │   ├── device_protection_vs_contract.png
│   │   ├── senior_citizen_vs_internet_service.png
│   │   ├── tech_support_vs_payment_method.png
│   │   └── tenure_vs_payment_method.png
│   │
│   └── numarical/
│       ├── correlation_heatmap.png
│       ├── monthly_charges_distribution.png
│       ├── monthly_charges_tenure_vs_total_charges.png
│       ├── tenure_distribution.png
│       └── total_charges_distribution.png
│
└── scripts/
    └── telco_churn_analysis_eda.py

```

---
<h2><a class="anchor" id="data-assessment--cleaning"></a>Data Assessment & Cleaning</h2>

The following preprocessing steps were performed before the analysis:

- Assessed dataset structure and data quality.
- Checked for duplicate records.
- Standardised column names using snake_case naming convention.
- Identified and handled missing values.
- Converted numerical columns to appropriate data types.
- Removed 11 records containing missing Total Charges values.
- Validated categorical values for consistency.
- Performed outlier detection using the IQR method.
- Engineered tenure groups by creating tenure bins for lifecycle analysis.
- Removed Customer ID as it has no analytical value.

---
<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

The analysis was divided into three major sections:

**Univariate Analysis:**
- Analysed the distribution of each categorical feature.
- Compared churn rates across customer characteristics.
- Identified individual variables associated with higher churn.

**Numerical Analysis:**
- Studied the distribution of Tenure, Monthly Charges, and Total Charges.
- Compared churned and retained customers using density plots.
- Examined correlations among numerical variables.

**Bivariate Analysis:**
- Compared combinations of customer characteristics.
- Identified high-risk customer segments by calculating churn rates across feature combinations.
- Automated repetitive visualisation using reusable Python functions.

---
<h2><a class="anchor" id="key-insights"></a>Key Insights</h2>

Major findings from gettext import install

import pip

from the analysis include:

- Customers on Month-to-Month contracts showed the highest churn rates.
- Customers within the first 12 months had the greatest likelihood of churning.
- Fiber Optic internet customers experienced significantly higher churn than DSL customers.
- Customers without Online Security, Tech Support, Device Protection, or Online Backup consistently showed higher churn.
- Customers paying through Electronic Check exhibited the highest churn among payment methods.
- Customers with higher Monthly Charges and lower Total Charges were more likely to churn.
- Long-tenure customers demonstrated significantly stronger retention.
- Bivariate analysis revealed that combining multiple high-risk characteristics further increased churn probability.

---
<h2><a class="anchor" id="business-recommendations"></a>Business Recommendations</h2>

Based on the findings, the following business recommendations are suggested:

- Strengthen onboarding programs to improve retention during the first year.
- Encourage customers to migrate from Month-to-Month contracts to longer-term contracts through incentives.
- Promote value-added services such as Tech Support, Online Security, Device Protection, and Online Backup.
- Investigate customer satisfaction among Fibre Optic users to identify underlying causes of churn.
- Encourage customers to adopt automatic payment methods instead of Electronic Check.
- Build targeted retention campaigns for high-risk customer segments identified through bivariate analysis.
- Continue rewarding long-term loyal customers through loyalty programs and personalised offers.

---
<h2><a class="anchor" id="project-outputs"></a>Project Outputs</h2>

The project includes several visualisations illustrating customer churn patterns, including:

- Customer Churn Distribution
- Churn by Contract Type
- Churn by Internet Service
- Churn by Payment Method
- Tenure Distribution by Churn Status
- Monthly Charges Distribution by Churn Status
- Total Charges Distribution by Churn Status
- Key Bivariate Analysis Visualizations

(Project screenshots can be found inside the outputs/ directory.)

---
<h2><a class="anchor" id="results--conclusion"></a>Results & Conclusion</h2>

This project successfully identified the major drivers of customer churn through comprehensive exploratory data analysis.

The findings indicate that customer churn is strongly influenced by contract type, customer tenure, internet service type, payment methods, monthly charges, and the adoption of value-added support services. Customers with multiple high-risk characteristics were found to have substantially higher churn probabilities.

The insights generated through this analysis can support data-driven customer retention strategies, enabling businesses to improve customer satisfaction, reduce churn, and maximise long-term customer lifetime value.

---
<h2><a class="anchor" id="future-work"></a>Future Work</h2>

Potential extensions of this project include:

- Build machine learning models to predict customer churn.
- Perform statistical hypothesis testing on key churn drivers.
- Develop an interactive Power BI dashboard.
- Deploy the analysis using Streamlit.
- Compare multiple classification algorithms for churn prediction.
- Evaluate feature importance using explainable AI techniques.

---
<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Muhammed Bashar Ayyoli**
  
  Data Analyst
- 📧 Email: muhammedbashar2003@gmail.com
- 🔗 [LinkedIn](https://www.linkedin.com/in/muhammed-bashar-b56770328/)
- 🔗 [GitHub](https://github.com/muhammedbashar)
- 🔗 [Portfolio](datascienceportfol.io/muhammedbashar)
