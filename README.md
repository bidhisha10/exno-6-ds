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
<img width="682" height="556" alt="image" src="https://github.com/user-attachments/assets/442a19a8-544b-431c-bcc2-722681b026d8" />


```
df = sns.load_dataset("tips")
df

```
<img width="607" height="532" alt="image" src="https://github.com/user-attachments/assets/3e7a8160-d521-4c10-9783-9aac0b766bcf" />


```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

```
<img width="727" height="562" alt="image" src="https://github.com/user-attachments/assets/b26e360d-9426-4a15-8217-56b444c9d128" />


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

<img width="802" height="592" alt="image" src="https://github.com/user-attachments/assets/7cfc7a76-7ac2-4255-8a45-1caf77ff09d0" />


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
<img width="728" height="602" alt="image" src="https://github.com/user-attachments/assets/5083ce61-c4b7-400d-810f-203a3005b47e" />


```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

```
<img width="728" height="561" alt="image" src="https://github.com/user-attachments/assets/8049b511-3ed0-4abc-8016-528e192fdba5" />


```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)

```
<img width="770" height="587" alt="image" src="https://github.com/user-attachments/assets/e19263fe-fe98-4cfe-9203-d6517de9da07" />


```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')

```
<img width="752" height="587" alt="image" src="https://github.com/user-attachments/assets/47dd9614-b9b1-4fbc-bc42-80f08e6c60e9" />


```
tit=pd.read_csv("/content/titanic_dataset.csv")
tit

```
<img width="1516" height="550" alt="image" src="https://github.com/user-attachments/assets/77bc1912-588c-4d12-b82e-d9bb1de4bd97" />


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")

```
<img width="727" height="535" alt="image" src="https://github.com/user-attachments/assets/22350899-502a-4786-816e-ab4c0f516e65" />


```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")

```

<img width="738" height="543" alt="image" src="https://github.com/user-attachments/assets/e3a13adb-0ed8-44c2-a413-ef1bc11cb495" />


```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')

```

<img width="731" height="610" alt="image" src="https://github.com/user-attachments/assets/718e4b29-121a-48de-bf5d-576158b6e9e2" />


```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var

```
<img width="355" height="575" alt="image" src="https://github.com/user-attachments/assets/72131f83-5139-4cb7-a74f-5f2fdb1fbf4a" />


```
sns.histplot(data = num_var, kde = True)

```
<img width="757" height="580" alt="image" src="https://github.com/user-attachments/assets/94f557a2-f52c-4a67-a806-9fbb727ba02c" />


```
df=pd.read_csv("/content/titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)

```
<img width="753" height="577" alt="image" src="https://github.com/user-attachments/assets/2e84b293-8c80-4d1b-91b9-862bf7517192" />


```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])

```
<img width="753" height="598" alt="image" src="https://github.com/user-attachments/assets/2e881fff-d369-4cc2-812a-e0cb9d44f797" />


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

```
<img width="780" height="576" alt="image" src="https://github.com/user-attachments/assets/4c6b2826-83a7-413a-ad11-1ed26bb84494" />


```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")

```
<img width="743" height="620" alt="image" src="https://github.com/user-attachments/assets/aff93561-4f91-4f34-8738-6761e0a0636e" />


```
mart=pd.read_csv("/content/titanic_dataset.csv")
mart

```
<img width="1062" height="478" alt="image" src="https://github.com/user-attachments/assets/382459f8-3a32-40e5-a60f-5723a939dee7" />


```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)

```
<img width="752" height="562" alt="image" src="https://github.com/user-attachments/assets/e63904c0-1022-4381-ac08-1bd842800f05" />


```
sns.kdeplot(data=mart,x='PassengerId')
```

<img width="782" height="592" alt="image" src="https://github.com/user-attachments/assets/243b9890-b35f-4061-a8c8-b16b45a3dcbf" />


```
sns.kdeplot(data=mart,x='Age')

```
<img width="752" height="577" alt="image" src="https://github.com/user-attachments/assets/adfa24a2-524f-4699-80f8-f7188c3310fb" />


```
sns.kdeplot(data=mart)
```
<img width="802" height="571" alt="image" src="https://github.com/user-attachments/assets/c39d8724-b161-4e06-a6f9-54c03b20e845" />


```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')

```
<img width="752" height="582" alt="image" src="https://github.com/user-attachments/assets/116c6082-063d-4830-b498-e88b5098a945" />


```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')

```


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)

```
<img width="702" height="547" alt="image" src="https://github.com/user-attachments/assets/ca5282b4-a0ed-40e9-af77-265ce0c59034" />


```
hm=sns.heatmap(data=data)

```
<img width="710" height="557" alt="image" src="https://github.com/user-attachments/assets/acaa760c-6e92-4ee1-8d51-cc1a9dc4feac" />








# Result:
Thus, the Data Visualization using seaborn python library for the given datas is performed.
