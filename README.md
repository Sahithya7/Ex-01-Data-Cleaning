# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
```
# OUPUT
## DATA
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/c590c7d0-e4b8-477a-b4c8-e42165bdc3b2)
## NON NULL BEFORE
## df.info
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/0dc18b25-9fa4-4ceb-925f-78e50584c49d)
## Mode
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/e0b60aeb-e0bc-43c5-a624-d40b29f34d11)
## Mean
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/710a6c9f-36bc-4844-b6e9-c19eb3361a04)
## Median
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/7cf7a437-e86b-425d-956f-5e95480db464)
## NON NULL AFTER
## df.info()
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/638debbc-9388-4554-a054-3b5f1267cbf4)
## df.isnull().sum()
### ![image](https://github.com/Sahithya7/Ex-01-Data-Cleaning/assets/133002193/6a9b8154-23cb-4109-a2fe-553269efdb74)
# Result
Thus,the given data is read,cleansed and the cleaned data is saved into the file.



