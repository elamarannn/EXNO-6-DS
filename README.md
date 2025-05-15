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
## Developed by : Elamaran S E
## Register no.: 212222230036
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x=[1,2,3,4,5]
y=[3,5,2,7,1]
sns.lineplot(x=x,y=y,color = 'green')
```
![download](https://github.com/user-attachments/assets/1cbefd55-f79f-4973-98d3-121baf672c07)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/ad628a15-962e-4388-8ce4-f927a878be98)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto",)
```
![download](https://github.com/user-attachments/assets/489024b4-4cdc-425e-a1a2-53a872cde893)
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
![download](https://github.com/user-attachments/assets/4c086553-594f-4930-9c81-475152c6a6b6)
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
![download](https://github.com/user-attachments/assets/44ef617c-fda7-40f9-a1b6-f975043a0d40)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![download](https://github.com/user-attachments/assets/acf49072-8360-404b-8049-310a90cd2379)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![download](https://github.com/user-attachments/assets/874b8645-475e-4c1f-af01-d7d060284710)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![download](https://github.com/user-attachments/assets/8600be97-21d3-40b6-b2bd-57806178f843)
```
tit=pd.read_csv("/content/titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/16a421b1-e1c7-4266-be6f-ed8354426152)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rocket') 
plt.title("Fare of Passenger by Embarked Town")
```
![download](https://github.com/user-attachments/assets/98062f4f-a698-439b-b4a0-612686ea1483)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='viridis', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![download](https://github.com/user-attachments/assets/df114a5f-f53c-4a85-9fba-8b20e8d720d9)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![download](https://github.com/user-attachments/assets/fc06170e-c9b9-4131-98ca-aa8468b0fb4e)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/d7aaa38e-89f9-4a6c-b130-dca296e0bec1)
```
sns.histplot(data = num_var, kde = True,color = 'red')
```
![download](https://github.com/user-attachments/assets/fcd2a925-a13d-4d2f-ad7a-18d342db57db)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True, palette = "Set1")
```
![download](https://github.com/user-attachments/assets/60be6fc9-4ac9-4c55-aa34-5b289dff279d)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'], palette = "Set2")
```
![download](https://github.com/user-attachments/assets/59730bad-03b0-4a96-afe1-5f13afe10862)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "violet", "edgecolor": "pink"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![download](https://github.com/user-attachments/assets/c5befef9-12c7-47eb-a560-d683d179f57d)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Paired", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![download](https://github.com/user-attachments/assets/1101d2ea-f1d8-4a3e-b30c-0745f84d17e8)
```
mart=pd.read_csv("/content/titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/86ddc0c1-41d3-4e6a-ad56-7f8140c0452f)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/user-attachments/assets/5def1026-8176-42f6-9598-2cd38fdc9e62)
```
sns.kdeplot(data=mart,x='PassengerId',color = 'red')
```
![download](https://github.com/user-attachments/assets/5f58cc3f-9d39-4eb9-ba45-fe2b8e209aee)
```
sns.kdeplot(data=mart,x='Age',color = 'green')
```
![download](https://github.com/user-attachments/assets/c24ef8b7-4b18-47c3-a0f2-f9e2b7f79b06)
```
sns.kdeplot(data=mart)
```
![download](https://github.com/user-attachments/assets/e84a0589-0c01-4c3a-a164-56d1b12f22da)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack',palette='Set2')
```
![download](https://github.com/user-attachments/assets/d6cfec9f-1e84-4362-be39-98312651149f)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![download](https://github.com/user-attachments/assets/358872dc-a608-40f5-aee2-ee895bed2dc1)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![download](https://github.com/user-attachments/assets/f72397a7-f542-475b-9aa5-e386b3c76351)
```
hm=sns.heatmap(data=data)
```
![download](https://github.com/user-attachments/assets/0e76965d-561c-4366-9ef3-428d5fd82e28)

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully

