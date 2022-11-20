 Ex-07-Data-Visualization-

AIM

To Perform Data Visualization on the given dataset and save the data to a file. 

Explanation

Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an 
accessible way to see and understand trends, outliers, and patterns in data.

ALGORITHM

STEP 1

Read the given Data

STEP 2

Clean the Data Set using Data Cleaning Process

STEP 3

Apply Feature generation and selection techniques to all the features of the data set

STEP 4

Apply data visualization techniques to identify the patterns of the data.

CODE:

import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore (1).csv")

df.info()

df.isnull().sum()

![71](https://user-images.githubusercontent.com/95409048/202892315-01047194-837a-4613-a498-d976b83a64e6.png)

![72](https://user-images.githubusercontent.com/95409048/202892330-c3406935-c7de-4d58-a6ea-ff3ff0fb1ba3.png)


import matplotlib.pyplot as plt

import numpy as np

sns.distplot(df['Sales'])

plt.axvline(x=np.mean(df['Sales']), c='red', ls='--', label='mean')

plt.axvline(x=np.percentile(df['Sales'],25),c='green', ls='--', label = '25th percentile:Q1')

plt.axvline(x=np.percentile(df['Sales'],75),c='orange', ls='--',label = '75th percentile:Q3' )

plt.legend()

![73](https://user-images.githubusercontent.com/95409048/202892334-26c6c539-4c22-4b1b-9a50-a82fe29f9f10.png)


sns.boxplot(x=df['Segment'], y=df['Sales'])

![74](https://user-images.githubusercontent.com/95409048/202892344-2d1207ac-b3e3-499f-bf37-06e9f386bf7c.png)


sns.scatterplot(x=df['City'], y=df['Sales'])

![75](https://user-images.githubusercontent.com/95409048/202892351-de952401-14e0-4a70-8385-fa96c48b142e.png)

sns.boxplot(df['Region'], df['Sales'])

![76](https://user-images.githubusercontent.com/95409048/202892356-6f7220cb-c79e-47e1-a7be-eab47ab444f3.png)




