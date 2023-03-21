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
Name : harithashree.v
Register Number : 212222230046
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

# OUTPUT

# DATA: 
![Screenshot 2023-03-21 102119](https://user-images.githubusercontent.com/121285701/226528626-322e1a21-bb41-43a1-b64f-5d3fd78ed74e.png)


# NON-NULL BEFORE:
# df.info:
![Screenshot 2023-03-21 103124](https://user-images.githubusercontent.com/121285701/226528650-c8bda3c6-1c60-416a-9b7e-bca7de54b2b9.png)

# MODE:
![Screenshot 2023-03-21 102601](https://user-images.githubusercontent.com/121285701/226528873-0788ec6d-cb7c-49a9-8794-f9c0b6b066e4.png)

# MEAN:
![Screenshot 2023-03-21 102737](https://user-images.githubusercontent.com/121285701/226528935-7325770f-da67-486d-bb8b-577dd9c2497e.png)

# MEDIAN:
![Screenshot 2023-03-21 102846](https://user-images.githubusercontent.com/121285701/226528967-4e530748-ee9d-4926-ab13-e1bc6c03519e.png)

# NON-NULL AFTER:
# df.info:
![Screenshot 2023-03-21 103124](https://user-images.githubusercontent.com/121285701/226529038-7a4c92dc-6ce9-4a12-9697-7224679c2191.png)

# df.isnull().sum():
![Screenshot 2023-03-21 113001](https://user-images.githubusercontent.com/121285701/226529239-9266e311-dd7b-440d-a64a-5de85b0101f0.png)


# RESULT:

Thus,the given data is read,cleansed and the cleaned data is saved into the file.



