---
title: "TikTok Data Exploration"
categories:
  - Python
  - Pandas
  - NumPy
tags:
  - Python
  - Pandas
---
TikTok’s data team is in the earliest stages of the claims classification project. The following tasks are needed before the team can begin the data analysis process:
- Build a dataframe for the TikTok dataset
- Examine data type of each column
- Gather descriptive statistics

## Project Overview
[The code for the project can be found here](https://github.com/SimpleStepper/GADA_Project_1-TikTok_Data_Exploration/blob/main/Course%202%20-%20TikTok%20Python%20Project.ipynb)

Several task were performed such as: 
- Loading necessary packages (NumPy, Pandas)
- Importing TikTok dataset and converting into a Pandas dataframe
- Identifying relevant data structures and summarizing data
- Combining or modifying data structures to create meaningful variables
  
## Data Insights
- Dataset Overview:
  - Contains **19,382 records** with TikTok Metrics such as video views, likes, shares, downloads.
  - Key attributes investigated include **claim_status** and **author_ban_status**.
  - Missing several values within columns displayed as NaN.
      
- Key Observations:
  - The Percentage of data is split between "claims" and "opinion" is 51% for claims (9,608 users) and 49% (9476 users) for opinions.
  - Videos from **"Banned"** or **"Under-review"** users have a higher "claim" classification which have **significantly higher count of likes, shares and comments** in the "claim" category. In the "Opinion" classifcation the opposite is true, Active users have more engagement overall than the "Banned" or "Under-review" users.

## Technical Skills
1. **Data Exploration:**
     - Computing summary statistics (mean, median, min, max) in relevant categories.
     - Utilizing Pandas to filter, group, and transform data for actionable insights.
     - Understanding data distributions and trends in the dataset.
2. **Programming and Libraries:**
     - Proficency in **Python** and utilizing **Jupyter Notebooks**.
     - Utilized key Python libraries such as **Pandas** and **NumPy**.
3. **Problem Solving:**
     - programming and debugging Python code to perform analytical tasks.
     - Understanding questions proposed in project statement and emails.
     - Interpreting raw data and designing workflows to achieve actionable insights for projects going forward.
