# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[2,3,7,1,5]
sns.lineplot(x=x,y=y)
````
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle="solid",legend="auto")
```
![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/9d553688-ca50-4686-9b48-45a7c443f20a)

import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by day')
plt.legend()


![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/66c722a8-d103-46ec-acf5-8e9f0cb8a83c)


sns.barplot(x='day',y='total_bill',hue='sex',data=df,palette='Set2')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by day and gender')

![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/1a3d0679-9329-4198-b980-e7ff8a9f2a4e)


import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter plot of total bill vd Tip amount')

![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/057a33c5-d9d2-47f2-8ad7-0f4b622ee10d)

import seaborn as sns
import numpy as np
import pandas as pd
num_var=pd.read_csv("/content/titanic_dataset.csv")
num_var
sns.histplot(data=num_var,x="Pclass",hue="Survived",kde=True)

![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/ea611395-0600-470b-af54-0e141c708915)

np.random.seed(1)
num=np.random.randn(100)
num=pd.Series(num,name="Numerical Variable")
num
sns.histplot(data=num,kde=True)


![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/f7564649-4ca5-4510-9d3e-ad00d04bc1fe)

import matplotlib.pyplot as plt
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
marks
sns.histplot(data=marks,bins=10,kde=True,stat="count",cumulative=False,multiple="stack",element="bars",palette="Set1",color="black",shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students marks')


![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/3a0cd191-e44a-49cc-9186-b042c5361206)


import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])


![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/a3f04cff-ce79-44cf-b362-7a1e2ef6903d)

sns.boxplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, boxprops={'facecolor':'lightblue','edgecolor':'black'},whiskerprops={'color':'blue','linestyle':'--','linewidth':1.5},capprops={'color':'red','linestyle':'--','linewidth':1.5})


![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/64693251-1b2f-4ebf-9834-a1b6829f1163)

import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
sns.violinplot(x='day',y='total_bill',hue='smoker',data=tips, linewidth=2,width=0.6, palette='Set1',color='blue',inner="quartile")
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Violin plot of Total bill by day and smoker status')


![image](https://github.com/Preetha-Senthamilan/EXNO-6-DS/assets/119390282/f2c618f0-bbc7-4c5e-96df-15365eb8c50d)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
