# Ex03-Univariate-Analysis

AIM:

To perform Univariate EDA on the given data set

Explanation:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis

ALGORITHM:

STEP 1:

Import the built libraries required to perform EDA and outlier removal.

STEP 2:

Read the given csv file

STEP 3:

Convert the file into a dataframe and get information of the data.

STEP 4:

Return the objects containing counts of unique values using (value_counts()).

STEP 5:

Plot the counts in the form of Histogram or Bar Graph.

STEP 6:

Use seaborn the bar graph comparison of data can be viewed.

STEP 7:

Save the final data set into the file

PROGRAM:
```
Name:Adhithya Perumal.D
Reg.No:212222230007

import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)
```

OUTPUT:

EDA - SuperStore.csv:

![super](https://user-images.githubusercontent.com/118707079/228013269-4b046fff-c146-4342-975c-e7b5521c2ce3.png)

Displaying information about Dataset:

![info](https://user-images.githubusercontent.com/118707079/228013369-408a5bb0-62f9-4b4b-ad13-f4fa704fca09.png)

![infoo](https://user-images.githubusercontent.com/118707079/228014697-9b65de90-28e2-4000-89ca-8a811b04e74f.png)

Finding null values and cleaning it:

![postal](https://user-images.githubusercontent.com/118707079/228014880-efa23284-d40b-4619-acea-ef54f04a1204.png)

Value counts of "Postal Code":

![value](https://user-images.githubusercontent.com/118707079/228015110-d7d2b5d2-711a-40b4-90b8-e3ec84008529.png)

Distribution of Data:

![data](https://user-images.githubusercontent.com/118707079/228015236-4d703949-202d-494a-a36f-c62cc49af261.png)

Univariate Analysis:

![uni](https://user-images.githubusercontent.com/118707079/228015499-e56295ba-b07b-4781-8043-024020d446fb.png)

![univariate](https://user-images.githubusercontent.com/118707079/228015859-2604b4c1-94b1-4794-b719-77dc9ff16e2a.png)

![output1](https://user-images.githubusercontent.com/118707079/228016023-09edf85f-acdb-4e01-93cd-840c960ca027.png)

![output2](https://user-images.githubusercontent.com/118707079/228016212-b3cb2c32-aa4e-43d8-92bc-7c4de814d885.png)

![output3](https://user-images.githubusercontent.com/118707079/228016330-3c8f7b9f-75b5-4097-8290-6e6c42c3b684.png)

RESULT:

Thus the program to perform EDA on the given data set is successfully executed















