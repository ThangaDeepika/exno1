# Exno:1
# 1) Data Cleaning Process

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

# Code
# For Data_set
```
 import pandas as pd
 df=pd.read_csv("/content/Data_set .csv")
 df
 df.head(10)
 df.info()
 df.isnull()
 df.isnull().sum()
 df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
 df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
 df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
 df.head()
 df['rating']=df['rating'].fillna(df['rating'].mean())
 df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean
 df.head()
 df['watchers']=df['watchers'].fillna(df['watchers'].median())
 df.head()
 df.info()
 df.isnull().sum()
```
# For loan_set
```
 import pandas as pd
 df=pd.read_csv("/content/Loan_Data.csv")
 print(df)
 df.head(5)
 df.info()
 df.isnull()
 df.isnull().sum()
 df['Loan_ID']=df['Loan_ID'].fillna(df['Education'].mode()[0])
 df['Education']=df['Education'].fillna(df['Education'].mode()[0])
 df['Married']=df['Married'].fillna(df['Education'].mode()[0])
```
```
 df.head()
 df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
 df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
 df.head()
 df.head()
 df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
 df.head()
 df.info()
 df.isnull().sum()
```
 # OUTPUT
 # For Data_Set
 ![image](https://github.com/ThangaDeepika/exno1/assets/125663099/b581b6e4-b8b3-481f-a93c-3ff7421c1a0c)
 ![image](https://github.com/ThangaDeepika/exno1/assets/125663099/cb40ed94-b364-4e1f-8d5b-293f5c1d39cf)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/850fbe7a-a9a6-4fac-ac8a-83b7a619c0ba)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/d9317b7b-5f04-4682-a175-4fe61f361f0a)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/a4928c49-2918-49b6-9e77-8d17ed8da2dd)
# NON NULL BEFORE
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/02b1b7f7-d360-4217-8bad-71ed011fde5f)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/c73f02d8-64e5-47ca-ba0a-0de5c4e63747)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/3fb85203-8458-445a-9e13-3b9f42c0c82c)
# MODE
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/2edc3c80-074e-4b73-aa25-fef19d23f799)
# MEAN
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/d2e49792-c9a3-4b2b-87c2-6031e07fe18b)
# MEDIAN
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/6fab031c-16da-41e8-b152-f3900b258460)
# NON NULL AFTER
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/590becd6-d7bb-4f05-9eed-6a1ebc296379)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/81626ddf-2bf6-45f4-8869-8621be32a9f8)
# For loan_data
# DATA
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/534dfbea-fdc4-4d6e-9e3d-0a50127e7ec4)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/73d7eb81-81c0-4356-90c6-65d09316391c)
# NON NULL BEFORE
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/3620d2af-e3de-4575-aa07-d40db3a68d8e)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/18bb20ca-653c-48f5-8747-2c4830ce0e26)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/a0b7d529-d249-454e-9124-1fe9688a9384)
# MODE
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/0f292fcc-4a18-4a7b-a5e2-a26dd71a53ea)
# MEAN
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/3ca75707-984a-46f9-93a0-86ed7eb9cd8d)
# MEDIAN
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/ecc2bfd7-2b85-4299-9f6e-540627fe4744)
# NON NULL AFTER
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/c2891cdd-b5d1-435a-8a2a-14416a08795d)
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/23d5914e-a325-4392-a35e-22ae78e2b016)

# 2)Outlier Detection and Removal

# AIM:
To read a given dataset and remove outliers and save a new dataframe.

# ALGORITHM:
(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them

# PROGRAM
```
import pandas as pd
import numpy as np
import seaborn as sns
import pandas as pd
from scipy import stats
df = pd.read_csv("/content/heights.csv")
sns.boxplot(data=df)
sns.scatterplot(data=df)
max =df['height'].quantile(0.90)
min =df['height'].quantile(0.15)
max
min
dq = df[((df['height']>=min)&(df['height']<=max))]
dq
low = min-1.5*iqr
high = max+1.5*iqr
dq = df[((df['height']>=min)&(df['height']<=max))]
dq
```
# ZSCORE:
```
import pandas as pd
import numpy as np
import seaborn as sns
import pandas as pd
from scipy import stats
data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}
df = pd.DataFrame(data)
df
sns.boxplot(data=df)
z = np.abs(stats.zscore(df))
print(df[z['weight']>3])
val =[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]
out=[]
def d_o(val):
ts=3
m=np.mean(val)
sd=np.std(val)
for i in val:
z=(i-m)/sd
if np.abs(z)>ts:
out.append(i)
return out
op = d_o(val)
op
```
# OUTPUT
![image](https://github.com/ThangaDeepika/exno1/assets/125663099/2f1a046f-49e9-440a-ba5f-8c16dae0e97d)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/9180b739-53e6-4d08-9761-eb41d79089ea)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/14bde4dd-e564-4fee-91f3-52de5ac7c59f)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/06e0caf4-dde0-4e11-8aee-2379a2ab7234)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/95daf9ae-454f-4924-ba58-b828b333e3b1)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/d889c5ca-07e3-4224-bc95-8a3e9faa1064)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/55f97582-795b-4864-aacf-f8df9fc3bea9)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/5d50f766-e253-4177-a6b0-bcfba5e14a17)

![image](https://github.com/ThangaDeepika/exno1/assets/125663099/969fcb81-d2fc-4e82-85d7-799bd09e1192)

# Result
Thus, the given data is read, cleansed and the cleaned data is saved into the file and the given data is read,remove outliers and save a new dataframe was created and executed successfully.

