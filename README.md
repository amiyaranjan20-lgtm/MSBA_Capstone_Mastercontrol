[MSBA Capstone – MasterControl Lead Progression Analytics](https://github.com/amiyaranjan20-lgtm/MSBA_Capstone_Mastercontrol)

# Introduction

Why does MasterControl’s **Mx product line convert leads at a lower rate than its Qx product**, and how can data help improve this performance?

This repository contains my analysis and modeling work for the **MSBA Capstone project with MasterControl**. The project focuses on analyzing qualified account leads and developing predictive models to identify which companies are most likely to progress through the sales pipeline for the **Mx manufacturing software product**.

Using exploratory data analysis and machine learning models, the goal of this project is to identify patterns in industries, company types, and buyer personas that influence lead progression and to provide **data-driven recommendations for improving outbound sales targeting.**

---

# 1. Business Context and Objective

MasterControl provides enterprise software solutions for **life sciences companies** through two primary product families:

- **Qx** – Quality management solutions  
- **Mx** – Manufacturing operations solutions  

While **Qx has strong market adoption (~19.7% progression)**, the **Mx product currently progresses at only ~12.7%**, creating a significant performance gap.

This gap suggests that current sales and marketing strategies for Mx may not be effectively targeting the right organizations or buyer personas.

MasterControl currently lacks clarity on:

- Which **industries and manufacturing models** are most likely to adopt Mx  
- Which **company sizes and locations** convert most frequently  
- Which **job titles or decision-makers** drive purchasing decisions for manufacturing software  

The guiding business question is:

> Which types of companies and buyer personas are most likely to progress in the sales pipeline for the Mx product?

The core objective of this project is to:

- Identify **high-propensity customer segments** for the Mx product  
- Develop **predictive models** to estimate lead progression likelihood  
- Provide **data-driven targeting recommendations** to improve conversion rates and SDR productivity  

---

# 2. Analytics Workflow Overview

My analysis follows a structured, reproducible workflow.

---

## 2.1 Data Understanding and Initial Cleaning

The first phase involved understanding the structure and quality of the lead dataset.

Key steps included:

- Reviewing dataset structure, variables, and data types  
- Standardizing variable names and formats  
- Identifying missing values and inconsistent entries  
- Cleaning categorical variables such as industry, job title, and company type  
- Preparing the dataset for exploratory and predictive analysis  

This phase ensured the dataset was clean, interpretable, and ready for deeper analysis.

---

## 2.2 Exploratory Data Analysis (EDA)

Before model building, I performed a detailed exploratory analysis to understand the structure, quality, and behavior of the variables in the dataset.

This included:

- Analyzing distribution of leads across **Qx and Mx products**
- Comparing **conversion rates between product lines**
- Examining patterns across **industries, company sizes, and site functions**
- Investigating patterns across **job titles and seniority levels**
- Identifying variables that show early signals of lead progression

The EDA phase provided the foundation for informed preprocessing decisions and helped guide the modeling strategy.




---

## 2.3 Data Preparation and Feature Engineering

To prepare the dataset for modeling, several preprocessing steps were applied:

- Handling missing values in account and contact attributes  
- Encoding categorical variables such as industry and job title  
- Creating derived features related to company characteristics and buyer roles  
- Preparing clean inputs for machine learning models  

These steps ensured consistent, structured data for model training.

---

## 2.4 Train / Validation Split

To evaluate model performance fairly:

- The dataset was split into **training and validation sets**
- Models were trained on the training set
- Performance was evaluated on unseen validation data

This process helps ensure that the models **generalize well and are not overfitting**.

---

## 2.5 Model Development

Several supervised machine learning models were trained to predict whether a lead would **progress to the next stage in the sales pipeline**.

Models evaluated include:

1. **Logistic Regression**
2. **Elastic Net Logistic Regression**
3. **Decision Tree (CART)**
4. **Random Forest**
5. **Gradient Boosting (XGBoost)**

Each model was trained using consistent preprocessing and evaluation methods to ensure fair comparison.

The complete modeling workflow can be found in:

`Modeling_Mastercontrol_Group_5_Final.html`

---

## 2.6 Model Performance

Several models were evaluated to determine which approach best predicts lead progression while also supporting business interpretation.

The models compared included:

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting (XGBoost)

Tree-based ensemble models demonstrated the ability to capture **non-linear relationships and complex interactions between company characteristics and buyer roles**. However, the goal of this project was not only predictive performance but also **clear business interpretability**.

For this reason, **Logistic Regression was selected as the primary model for analysis.**

Logistic regression provides several advantages that align directly with the business objective:

- **Statistical significance testing (p-values)** allows us to identify which variables meaningfully influence lead progression.
- **Odds ratios** provide an interpretable measure of how specific factors increase or decrease the probability of progression.
- The model structure makes it easier to translate analytical findings into **actionable sales and marketing recommendations**.

In practical analytics work, the most complex model is not always the most useful.  
Sometimes **a simpler, interpretable model can provide clearer insights and stronger business value than a more complex algorithm.**

By using logistic regression, we were able to directly answer key business questions such as:

- Which industries have higher progression likelihood?
- Which company characteristics are associated with successful leads?
- Which buyer roles are most likely to advance in the sales pipeline?

This approach allowed the analysis to remain both **statistically rigorous and highly interpretable for business stakeholders.**

---


# 3. My Contributions

This repository documents the work I contributed to the **MasterControl Capstone project**, including:

- Data exploration and feature understanding  
- Exploratory data analysis to identify key patterns  
- Data preparation and preprocessing  
- Development and evaluation of predictive models  
- Interpretation of results from a business perspective  
- Documentation of insights and project findings  

---

# 4. Business Value of the Analysis

This project provides MasterControl with a framework to:

- Identify **high-probability target accounts**
- Improve **Mx lead conversion rates**
- Optimize **sales and marketing targeting strategies**
- Increase **SDR productivity by focusing on high-propensity segments**

By prioritizing accounts with the highest likelihood of progression, the company can improve **sales efficiency and product adoption.**

---

# 5. Challenges Encountered

Several challenges influenced the analysis:

1. **High variability in job titles and roles**
2. **Complex categorical variables such as industry classifications**
3. **Incomplete or inconsistent account information**
4. **Differences in buyer personas between Qx and Mx**

Addressing these challenges required careful preprocessing, feature engineering, and model comparison.

---

# 6. What I Learned

This project strengthened several practical analytics skills:

- Translating business questions into analytical frameworks  
- Conducting structured exploratory data analysis  
- Preparing real-world business datasets for machine learning  
- Building and evaluating predictive models  
- Communicating technical insights in business language  

The experience reflects a **complete end-to-end analytics workflow similar to industry consulting projects.**

---

# 7. Interpretation of Results and Key Takeaways

The analysis revealed several key insights about lead progression for the Mx product.

### Key Findings

**1. Product positioning affects conversion**

Mx currently converts leads at a lower rate than Qx, suggesting that **targeting strategies may not yet be optimized.**

**2. Industry and manufacturing model matter**

Certain manufacturing-focused industries show stronger alignment with the Mx solution.

**3. Buyer personas differ between products**

Decision-makers for manufacturing software may differ from those responsible for quality management systems.

**4. Predictive analytics improves targeting**

Machine learning models help identify patterns in company attributes and buyer roles associated with higher progression rates.

These insights support the development of a **data-driven targeting strategy for MasterControl’s sales and marketing teams.**

---

# 8. Repository Contents

- `Business Problem Statement(Group 5).pdf`  
  Overview of the business problem, project objectives, and success metrics.

- `EDA-MasterControl-Amiya_updated-03-19`  
  Exploratory data analysis examining distributions, patterns, and early signals in the data.

- `Modeling_Mastercontrol_Group_5_Final`  
  Full predictive modeling workflow including feature preparation, model training, and evaluation.
  
  `Group 5 Presentation.pdf`
- Project documentation and analysis files used throughout the MSBA Capstone project.
