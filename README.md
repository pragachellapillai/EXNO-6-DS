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
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

![exp6_1](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/67ad761b-ebc3-4e05-8962-e26b097a6263)


```
df = sns.load_dataset("tips")
df
```

![exp6_2](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/b5fc6822-8621-4a65-baec-020503a9bcbb)


```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```

![exp6_3](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/781429ca-6da1-4c17-9fba-62422fd9cc3e)


```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```

![exp6_4](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/a430a3e4-af71-4991-91d1-39c9bd5dd0e2)


```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```

![exp6_5](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/ec2c0fb2-5d42-4bc1-9d99-edb6be3859dd)


```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

![exp6_6](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/d62befb1-f228-4eb5-87cb-228a0ddbfaff)


```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
```
```
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

![exp6_7](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/2c3a43bc-e5c3-4a44-82cf-90c890326631)


```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

![exp6_8](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/34a280c5-e3e3-4e2c-9263-de0961871fd3)


```
tit=pd.read_csv("titanic_dataset.csv")
tit
```

![exp6_9](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/fab996cf-189a-47f4-a398-1207787c20fb)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```

![exp6_10](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/056050b6-8263-4bd9-832e-e568f8265123)


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

![exp6_11](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/a3052672-c278-4eb5-98ae-285b789a7191)


```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![exp6_12](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/1c5767ec-34fd-44c5-a6f3-6ee3934494ac)


```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

![exp6_13](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/db1f7401-e653-4aac-a109-9d7a813bbd9f)


```
sns.histplot(data = num_var, kde = True)
```

![exp6_14](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/f331ceba-dcb6-49be-a109-74035fa62e20)


```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![exp6_15](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/ad131a00-ca2d-401d-b31e-71babf047d25)


```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

![exp6_16](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/bae1c452-5bd0-4798-ba8f-80d953dca267)


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![exp6_17](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/4b712839-8885-4e21-8ea9-7538f15f3125)


```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![exp6_18](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/b59cc4f4-ce41-496a-ab88-5a36d44724dd)


```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

![exp6_19](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/0bc89365-2fbe-4d3c-bb29-fec896ce2c82)


```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```

![exp6_20](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/32284a15-9667-4aef-8941-fff3136152a2)


```
sns.kdeplot(data=mart,x='PassengerId')
```

![exp6_21](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/db2fe42d-971c-4dda-a63b-8c7956ea50d3)


```
sns.kdeplot(data=mart,x='Age')
```

![exp6_22](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/a2e75a70-aabf-431e-8541-98ae53c1c7ee)


```
sns.kdeplot(data=mart)
```

![exp6_23](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/0993c561-cbf9-47c1-8f61-4c5f075899de)


```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

![exp6_24](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/9a8a99f2-0079-48de-bd6a-cac1e14b620c)


```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![exp6_25](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/7c95581b-79ae-4574-a878-dc1230ddb105)


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![exp6_26](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/7285fba4-89e2-4c8f-8449-34d7bd6e6aa5)


```
hm=sns.heatmap(data=data)
```

![exp6_27](https://github.com/Skanthasishanth/EXNO-6-DS/assets/118298456/c3973279-38aa-44a9-9025-8543d3030e11)



# Result:

Thus, all the data visualization techniques of seaborn has been implemented.
