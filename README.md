# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
##  Data Cleaning
   ```
import pandas as pd
df=pd.read_csv('Loan_data.csv')
df
```
![image](https://github.com/user-attachments/assets/cb677b6c-086a-46ec-87d9-2a3a736d1cca)
```
df.info()
```
![image](https://github.com/user-attachments/assets/6342c7a3-96b1-49f9-9dc1-3d642acfa0c7)
```df.describe()```
![Screenshot 2025-03-12 205741](https://github.com/user-attachments/assets/2e5196ce-2086-43c2-88ea-c850ca86f18f)
```df.isnull()```
![Screenshot 2025-03-12 205944](https://github.com/user-attachments/assets/40256420-d6b8-4682-a1b7-a4d853048bd5)
```df.isnull().sum()```
![Screenshot 2025-03-12 210142](https://github.com/user-attachments/assets/8d18b6ae-a27e-4860-b9f1-9cc19826da56)
```
df_dropped=df.dropna()
df_dropped
```
![Screenshot 2025-03-12 210251](https://github.com/user-attachments/assets/830b54d2-51a2-4ecf-ae9b-34202e51121d)
```
df_fill_0=df.fillna(0)
df_fill_0
```
![Screenshot 2025-03-12 210541](https://github.com/user-attachments/assets/8159e4c6-d3be-4ea8-bd0a-5aae132bf868)

```
df_ffill=df.ffill()
df_ffill
```
![Screenshot 2025-03-12 210650](https://github.com/user-attachments/assets/a5136bd3-67d9-4cbc-a2a8-572a5949f949)

```
df_bfill=df.bfill()
df_bfill
```
![Screenshot 2025-03-12 210748](https://github.com/user-attachments/assets/5b0a9387-2f22-4755-aa0c-bd46cc2d3037)

```
df_new=df
df_new['LoanAmount']=df['LoanAmount'].fillna((df['LoanAmount']).mean)
df_new['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna((df['Loan_Amount_Term']).mean)
df_new
```
![Screenshot 2025-03-12 211027](https://github.com/user-attachments/assets/fc4297da-3843-431c-b0db-aac6afae1c30)

```df_new.dropna(axis=0)```
![Screenshot 2025-03-12 211147](https://github.com/user-attachments/assets/b5c0f382-9e83-4fda-995d-439169d6f452)


# Result
          <<include your Result here>>
