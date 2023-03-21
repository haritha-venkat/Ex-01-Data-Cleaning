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
Name : thirisha.s
Register Number : 212222230160
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
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
![Screenshot 2023-03-21 101907](https://user-images.githubusercontent.com/120380280/226522301-bb501ac4-e744-4dc8-81ce-226b448a6dc8.png)

### NON NULL BEFORE

# df.info:
![Screenshot 2023-03-21 102456](https://user-images.githubusercontent.com/120380280/226522116-930a13a9-704e-4aa9-bc41-b73d3ae77a82.png)

## MODE
![Screenshot 2023-03-21 102601](https://user-images.githubusercontent.com/120380280/226522253-c84da8a0-e753-4354-b6b4-6758261023a0.png)

## MEAN
![Screenshot 2023-03-21 102737](https://user-images.githubusercontent.com/120380280/226522454-d13e2269-fd07-4ec8-b4ed-86d55bb076b2.png)

## MEDIAN
![Screenshot 2023-03-21 102846](https://user-images.githubusercontent.com/120380280/226522568-fa641799-490b-4f7e-8b28-511c85806840.png)

### NON NULL AFTER

# df.info:
![Screenshot 2023-03-21 102945](https://user-images.githubusercontent.com/120380280/226522672-1cd124c5-69a3-4245-9e60-e164b5601996.png)

# df.isnull().sum():
![Screenshot 2023-03-21 103124](https://user-images.githubusercontent.com/120380280/226522831-212a4c37-b746-4c8f-9af4-8b8ea9d0f0c3.png)


# RESULT:

Thus,the given data is read,cleansed and the cleaned data is saved into the file.
