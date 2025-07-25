---
title: "Predicting Employee Attrition with Random Forest Model - Google Advanced Analytics Capstone"
categories:
  - Python
  - Data Visualization
  - Scikit-learn
  - Seaborn
  - Classification Models
  - Matplotlib
tags:
  - Dashboard
  - Tableau
---
This Python project is the final capstone in Google’s Advanced Data Analytics Course. It focused on developing a predictive model to identify employees at risk of leaving (employee churn) Salifort Motors. Using Exploratory Data Analysis (EDA) and a Random Forest classifier, the analysis revealed key factors that influence employee attrition, such as satisfaction, workload, and tenure.

**This project was original created in a GitHub Repository. If you experience any formatting issues, please view the [original GitHub project](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone?tab=readme-ov-file#google-advanced-analytics-capstone).**

# Table of Contents
1. [Define - Overview](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone?tab=readme-ov-file#define---overview)
2. [Method - Dataset](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone?tab=readme-ov-file#method---dataset)
3. [Analyze - Exploratory Data Analysis](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone?tab=readme-ov-file#analyze---exploratory-data-analysis)
4. [Improve - Model Creation](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone?tab=readme-ov-file#improve---model-creation)
5. [Control - Conclusion and Stakeholder Suggestions](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone?tab=readme-ov-file#control---conclusion-and-stakeholder-suggestions)

--- 

## Define - Overview

The objective of this project was to **develop a predictive model** to identify employees at risk of leaving Salifort Motors. Leveraging **exploratory data analysis (EDA)** and a **Random Forest algorithm**, the analysis focused on internal HR and employee survey data to uncover the key drivers of turnover.

The project followed the **DMAIC framework**—Define, Measure, Analyze, Improve, and Control—to ensure a structured and data-driven approach. The final model achieved strong performance, highlighting **employee satisfaction, tenure, and workload** as the top predictors of turnover. These insights offer actionable guidance for Salifort Motors leadership to proactively identify retention risks.

All code used to create this project was written by me and can be found can be found [here](https://github.com/SimpleStepper/Google-Advanced-Analytics-Capstone/blob/main/Google%20Advanced%20Data%20Analytics%20Capstone.ipynb), or in the GitHub repository. The code offers deeper EDA insights and additional graphs. 

---

## Method - Dataset
The dataset provided contains 14,999 rows with employees’ self-reported information. It contains 10 columns featuring data on satisfaction levels, time spent with company, promotions, department, salary and left. The full dataset can be found on [Kaggle](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction).

![image](https://github.com/user-attachments/assets/de342ab0-eeeb-474a-ba44-8c3704a5daa8)

---

## Analyze - Exploratory Data Analysis
EDA was conducted fully within Python. This section will highlight the most important insights gathered during the data exploration phase. 

### 1. Correlation Heatmap

A Correlation Heatmap was made to identify which features should be investigated. By creating the heatmap, we understand that **Last Evaluation, Number of Projects, Average Monthly Hours, and Satisfaction level all potentially correlate with employees leaving the company**. 

![image](https://github.com/user-attachments/assets/fe0c6a87-6640-4924-9b95-12affa2a99a1)

### 2. Monthly Hours compared to Number of Projects Boxplot
- Strong Correlation between high workload (measured by monthly hours and number of projects).
- Burnout risk increases with **high project count (6-7)** and **high working hours** (over **200 hours** per month).
- Employees leave company when assigned **under 2 projects** per month or **over 5 projects** per month.
![image](https://github.com/user-attachments/assets/86ded3ca-3e19-444f-90d4-9445f5bcafd8)


### 3. Monthly Hours Worked Compared to Satisfaction Level
- Employees who worked over under 175 hours per month, and employees who worked more than 230 hours both have very low satisfaction ratings and high churn-rates. 

![image](https://github.com/user-attachments/assets/a080cc4d-7e81-475a-b75f-cccdb699fc3e)

### 4. Satisfaction Level compared to Tenure
- Employees that have worked over 7 years are unlikely to leave.
- Employees that have been with the company from 1 - 4 years are more likely to churn. 
- Employees that have worked 4 and 5 years have the lowest satisfaction score. This could be worth looking into for further analysis. 

![image](https://github.com/user-attachments/assets/fad4f2d4-ad35-49a0-8550-10139c17e13f)

### 5. Latest evaluation compared to Average Monthly Hours
- Employees that work over 260 hours are more likely to churn, depsite high evaluation ratings.
- Evaluation ratings are biased to be higher the longer a employee works each month.
- Employees who work less than 150 hours have a lower evaluation and higher churn rate than employees working in the 150 - 220 hours range.
  
![image](https://github.com/user-attachments/assets/3dd66430-f2de-4bc2-98fe-b06e8d428959)

---


## Improve - Model Creation
A random forest model comprising 100 decision trees was used to determine feature importance in which employees were more likely to churn (leave the company). The plot below shows that satisfaction level, tenure, number of projects, Average monthly hours, and last evaluation were the top 6 most important reasons in determining whether a employee is likely to leave the company.

![image](https://github.com/user-attachments/assets/a960fe1c-36df-40df-9765-74946ca44022)

The created model performed very well with a accuracry score of 97% and a precision score of 98%. The model was verified using a confusion matrix which showed 10 false positives, and 49 false negatives, compared to 2491 accurate positives, and 448 accurate negatives.

![image](https://github.com/user-attachments/assets/47c355f2-3a0a-483c-8224-96661948d08d)

---

## Control - Conclusion and Stakeholder Suggestions
Our model and feature importance results confirms that employees are currently being overworked leading to higher churn rates for the company. To prevent the employees from churning, the companies stakeholders should focus on:
1. Cap number of projects a individual can work on to a maximum of 5 per month.
2. Employees that work over 250 hours per month have a high churn rate. Reward employees who work more projects and hours. Most of the employees in this company worked over 167 hours per month.
3. Consider promoting employees or rewarding employees from years 1 - 4 as they have a higher churn rate. Why are 4 - 5 year employees unproportionately dissatisfied?
4. Employees with high evaluation scores are exclusively reserved for employees who work more than 200 hours currently. Evaluation scores should be based on quality of work, rewarding 250 hours or more. 
5. If expectations regarding high workload and time off have not been clearly communicated, take steps to clarify them.
6. If extended work hours are expected, ensure they are appropriately compensated. If not, avoid making them a requirement.
