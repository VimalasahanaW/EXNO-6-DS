# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
## NAME:VIMALA SAHANA W
## REG NO: 212223040241
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
![image](https://github.com/user-attachments/assets/2465d3c8-081f-4236-ba59-63d4ac738d77)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/a605f7c8-e060-4e61-a42c-eea2e20eb0f9)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/user-attachments/assets/50798c5e-d0e5-4a4e-a5ab-3afcbd3b2426)
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
![image](https://github.com/user-attachments/assets/0a2bd0f9-bd6b-4b88-8c05-33e8fba38d6d)
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
![image](https://github.com/user-attachments/assets/0a2cec63-8ea3-4b93-89f5-141ea369ac0e)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/92d714bd-7d84-44ea-bd2b-cf910e4ea490)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/e326d6ca-a820-408d-926f-7f1daa511f15)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/2156e803-3429-44b8-92aa-cc12336726e1)
```
import pandas as pd
tit=pd.read_csv("/content/titanic_dataset (1).csv")
tit
```
![image](https://github.com/user-attachments/assets/fe03d052-d228-4d80-8a91-8fd96a736fab)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/3146c045-4c3c-435e-865f-e375666afaae)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/858256b4-3a6a-43f4-9566-2fec8117bff7)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/2b174ace-acd4-43ff-8388-33f3cd90baa1)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/ace58244-91cb-4f17-9092-b311fe2b0397)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/2268b397-1f81-43ab-9954-ab80906d8751)
```
df=pd.read_csv("/content/titanic_dataset (1).csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/e69ee98a-ef28-4e93-88e5-2a43078e619f)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/69a068e0-4c09-4a88-91de-152eb0b939cc)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/23ea16ee-ffcd-4919-ae9d-ecd49bfcd98c)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/ef72d568-3db0-4c2b-9b69-a2d53227fea1)
```
mart=pd.read_csv("/content/titanic_dataset (1).csv")
mart
```
![image](https://github.com/user-attachments/assets/37200c25-cc8f-445f-90bd-d6bfc7a578ec)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/4a08c881-30d9-48d8-ada3-da050a54d4a3)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/dae79246-7662-4429-bc1d-da6358c83e9c)
```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/7e46335a-7947-445b-afeb-aa786be699b9)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/4c412e2c-eb9e-4f1c-b28c-00227eb1cab4)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/1fd780bd-9c22-4bb9-8eb0-d6a2e8523d25)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/bf327193-9014-4259-9a2f-4482073044cf)
```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/5fed2f96-c722-4d17-8436-9592e3bede50)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/066c2cbc-3df2-4f98-93ff-96f2ba55dd17)





























# Result:
 Include your result here
