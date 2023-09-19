# Project-4
<img width="1266" alt="Screenshot 2023-09-18 at 11 31 43 PM" src="https://github.com/maria-alsayed/Project-4/assets/130250635/c23eaa71-ac06-4790-a88b-c8065e15cb8f">
Human Resources Data Analytics and Model


## Overview

The main goal of this project is to create data visualizations and data model using machine learning that will help predict an issue.

In recent years, job-switching and voluntary resignations have become more common. Employee retention can help companies/organizations save a tremendous amount of time and money. Nonetheless, more and more employees are deciding to leave their current employer, but why? To help provide employers some insight, for this project, we decided to analyze publicly available human resource data to create a data model that will predict attrition based on data/features available. Additionally, we also want to create attractive visualizations that will enable leaders within an organization gain a deeper understanding of the data.

## Built With

In looking for publicly available HR data, we were able to locate a simulated employee dataset in Kaggle.com. This dataset is in CSV format. The specific dataset contains 2,952 records. Data includes the following information:
1.	Employee ID 
2.	First Name 
3.	Last Name 
4.	Start Date
5.	Exit Date 
6.	Title
7.	Supervisor
8.	Email
9.	Business Unit
10.	Employee Status
11.	Employee Type
12.	Pay Zone
13.	Employee Classification Type
14.	Termination Type
15.	Termination Description
16.	Department Type
17.	Division Description
18.	DOB (Date of Birth) 
19.	State
20.	Job Function
21.	Gender
22.	Location
23.	Race (or) Ethnicity
24.	Marital Status
25.	Performance Score
26.	Current Employee Rating

Dataset can be found here: https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset

## Data Cleanup

To begin exploring the dataset we created a Jupyter Notebook where we loaded and queried the CSV file. Using Pandas, we cleaned up the data by looking for duplicates, dropped columns that were not needed (e.g. Email), converted dates to usable formats, and converted date of birth to age. This initial data cleanup, allowed us to prepare our dataset for the data model and data visualizations.

## Data Visualizations

To help visualize our data and tell our data’s story more effectively and visually appealing to leaders of an organization, we used Tableau. [Insert what visualizations were created]

Age, Gender and Termination Type Analysis to compare attrition rate of both gender in each decade. 
![Alt text](./Viz 2 Images/Age and Termination Type.png)
Attrition ratio between men and women varies drastically from employees in their 30's and + 

A dashboard that includes an analysis of department with the highest turnover; as well as evaluate the percentage of attrition that is negatively impacting the company. 
![Alt text](./Viz 2 Images/Dashboard.png)

Attrition is much higher in production roles.  

The loss of talent is too high therefore mitigating employee attrition, especially high performer’s which accounted for 23%, will be a major win for the company. 


## Data Model


Data Source: https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset
