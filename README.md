# Ex-01_DS_Data_Cleansing
# AIM:
To read the given data and perform data cleaning and save the cleaned data to a file.

# EXPLANATION:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM:
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE:
## Loan_data.csv
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

# OUTPUT:

## Loan_data.csv

## DATA
![d1](https://user-images.githubusercontent.com/118707332/226185889-c6b8a63f-4b9d-41ca-b676-1408e6cc9733.png)

# NON NULL BEFORE

## df.info
![d2](https://user-images.githubusercontent.com/118707332/226186003-6a845a7b-6638-4c30-ae46-5c5d21cb542e.png)

# Mode
![d3](https://user-images.githubusercontent.com/118707332/226186126-603daa80-35c9-473b-a88c-e1410aa2311a.png)

# Mean
![d4](https://user-images.githubusercontent.com/118707332/226186191-2c1195de-b113-4693-9313-938ed955a602.png)

# Median
![d5](https://user-images.githubusercontent.com/118707332/226186373-43bcfbd9-9956-4c25-b0ac-88054f76bd70.png)

# NON NULL AFTER

## df.info()
![d6](https://user-images.githubusercontent.com/118707332/226186585-f1b542f2-747e-43ee-a454-3e11af01aed1.png)

## df.isnull().sum()
![d8](https://user-images.githubusercontent.com/118707332/226186642-96862123-c945-4210-8836-58ac28824a03.png)

# RESULT:
Thus,the given data is read,cleansed and the cleaned data is saved into the file.



