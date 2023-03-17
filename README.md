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

# CODE for DATA 1

```
/* 
Name : Aakash H
Register Number : 212220040002
**Data Cleaning - Data_set.csv**
import numpy as np
import pandas as pd
import seaborn as sbn
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUPUT for DATA 1
![11](https://user-images.githubusercontent.com/120620842/225975786-c1294853-cfe5-4058-92bc-3c582123a275.png)

# Before Cleaning
![head1](https://user-images.githubusercontent.com/120620842/225976025-f38b42e2-fe41-4de4-8716-e1f2633a89e0.png)
![info data1](https://user-images.githubusercontent.com/120620842/225978903-d7d57049-ddfd-4daf-bfde-8869ee6eb0ad.jpg)


![isnull01](https://user-images.githubusercontent.com/120620842/225976349-ccc38124-41ee-42c4-879e-e9ce1c9d0409.jpg)
![isnull sum01](https://user-images.githubusercontent.com/120620842/225976485-d53c488c-2f69-48eb-82cd-9e4ed88e0b7d.jpg)

# Mode
![mode1](https://user-images.githubusercontent.com/120620842/225976693-63e838b3-2813-43e9-a9e1-2f3689bbd0d5.png)

# Mean
![mean1](https://user-images.githubusercontent.com/120620842/225976895-84bb0106-f0d7-42da-887c-313e30754449.png)

# Median
![median1](https://user-images.githubusercontent.com/120620842/225976981-3c65e108-3076-4e20-8e9f-5d534b5fa045.png)

# After cleaning
![info1](https://user-images.githubusercontent.com/120620842/225977576-76bd3bb4-56ec-4a22-b29a-c068def0890c.png)

![isnull sum1](https://user-images.githubusercontent.com/120620842/225977466-df5f09b8-653c-4233-94cc-e595953f1f56.png)

# Code for DATA 2
```
import pandas as pd
import numpy as np
import seaborn as sns
d = pd.read_csv("/content/Loan_data.csv")
d
d.head()
d.describe()
d.tail()
d.isnull().sum()
d.shape
d.columns
d.duplicated

#Using mode method to fill the data in columns as Object(String)
#mode()[0] - Takes the most reccuring value and fills the empty cells
d['Gender'] = d['Gender'].fillna(d['Gender'].mode()[0])
d['Dependents'] = d['Dependents'].fillna(d['Dependents'].mode()[0])
d['Self_Employed'] = d['Self_Employed'].fillna(d['Self_Employed'].mode()[0])

#Using mean method to fill the data
d['LoanAmount'] = d['LoanAmount'].fillna(d['LoanAmount'].mean())
d['Loan_Amount_Term'] = d['Loan_Amount_Term'].fillna(d['Loan_Amount_Term'].mean())
d['Credit_History'] = d['Credit_History'].fillna(d['Credit_History'].mean())

sns.boxplot(y="LoanAmount",data=d)

#Checking the total no.of null values
again
d.isnull().sum()

#Checking info of the dataset to check all the columns have entries
d.info()
```

# Output for DATA 2
![21](https://user-images.githubusercontent.com/120620842/225985839-fcc1db78-a1fe-4e0a-9b1a-76672ffe7c1c.png)

# Before Cleaning

![22](https://user-images.githubusercontent.com/120620842/225986091-b2841eec-4db6-45ce-9c0b-c0329c579254.png)

![23](https://user-images.githubusercontent.com/120620842/225986249-80797c10-6ef4-4545-86e5-b049d7e32e15.png)
![24](https://user-images.githubusercontent.com/120620842/225986398-1e37fb97-fd72-4cb8-a2df-505e3824b8d6.png)
![25](https://user-images.githubusercontent.com/120620842/225986471-4c0ef827-81d8-4f46-8c65-41ce405f1da4.png)
![27](https://user-images.githubusercontent.com/120620842/225986537-12c311dc-3448-4b83-b360-5fa893ab4df1.png)
![28](https://user-images.githubusercontent.com/120620842/225986616-0643b98c-1906-4714-ac3c-431d9f2b1736.png)

# Mode
![mode2](https://user-images.githubusercontent.com/120620842/225986723-0b3fb589-fb86-498a-aeb0-a2932d402174.png)

# Mean
![mean2](https://user-images.githubusercontent.com/120620842/225986794-38573f63-1ea0-4b38-b24a-f59d64bbae8c.png)

# Median
![median2](https://user-images.githubusercontent.com/120620842/225986932-7623b229-3e0b-4fcf-9667-6ce32d8085f8.png)

# After cleaning
![after cleaning1](https://user-images.githubusercontent.com/120620842/225987124-ba12fa46-54d0-4ab5-86c1-c020417650b8.jpg)

# Result
Thus the given data is read,cleansed and cleaned data is saved into the file.
