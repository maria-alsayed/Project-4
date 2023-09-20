# Project-4

Human Resources Data Analytics and Model
<img width="1266" alt="Screenshot 2023-09-18 at 11 31 43 PM" src="https://github.com/maria-alsayed/Project-4/assets/130250635/dd9a9b16-ed2a-4d38-9ce0-dde2afc5d9be">

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

## Model Creation

We initially decided to procedd with a Random Forest Model (HR_model.ipynb). We chose this model because it is suitable for both numerical and categorical data, high accuracy and generalization, can handle large datasets with many features. Initally, upon the creation of this model we were getting an accuracy of 1.00. This seemed suspicious so we created two other models, decision tree and logisctic regression, to test the accuracy and look for variation. After testing, these models also produced 1.00 accuracy. This lead us to do some more investigating and notice that the columns 'Supervisor', 'TerminationType', 'EmployeeStatus' needed to be dropped. 'Supervisor' because the data was different for every individual and was there for just adding cluter to the model and the other two were causing data leakage. Both were giving the model the answer to if an employee was terminated or not. After removing this we noticed that the accuracy dropped. We also used X = pd.get_dummies(X) to perform one-hot encoding on categorical variables in the DataFrame to ensure that the information contained in the categorical variable was preserved and try to lead to improved model performance by helping the model make distinctions between different categories.

"Turnover" column is a binary target variable that helps categorize employees as either having experienced turnover (1) or not (0) based on the condition that their "ExitDate" is on or before '2023-08-06'.

Random Forest
Accuracy: 0.52
              precision    recall  f1-score   support

           0       0.49      0.52      0.51       287
           1       0.54      0.51      0.52       313

    accuracy                           0.52       600
   macro avg       0.52      0.52      0.51       600
weighted avg       0.52      0.52      0.52       600

Confusion Matrix:
[[149 138]
 [153 160]]

Decision Tree
Accuracy: 0.50
              precision    recall  f1-score   support

           0       0.48      0.52      0.50       289
           1       0.52      0.48      0.50       311

    accuracy                           0.50       600
   macro avg       0.50      0.50      0.50       600
weighted avg       0.50      0.50      0.50       600

Confusion Matrix:
[[151 138]
 [163 148]]

 Logistic Regression 
Accuracy: 0.44
              precision    recall  f1-score   support

           0       0.42      0.49      0.46       285
           1       0.46      0.39      0.42       315

    accuracy                           0.44       600
   macro avg       0.44      0.44      0.44       600
weighted avg       0.44      0.44      0.44       600

Confusion Matrix:
[[141 144]
 [193 122]]
 

## Data Visualizations

To help visualize our data and tell our data’s story more effectively and visually appealing to leaders of an organization, we used Tableau. 

Age, Gender and Termination Type Analysis to compare attrition rate of both gender in each decade. 
![Alt text](./Viz 2 Images/Age and Termination Type.png)
Attrition ratio between men and women varies drastically from employees in their 30's and + 

A dashboard that includes an analysis of department with the highest turnover; as well as evaluate the percentage of attrition that is negatively impacting the company. 
![Alt text](./Viz 2 Images/Dashboard.png)

Attrition is much higher in production roles.  

The loss of talent is too high therefore mitigating employee attrition, especially high performer’s which accounted for 23%, will be a major win for the company. 



Data Source: https://www.kaggle.com/datasets/ravindrasinghrana/employeedataset
