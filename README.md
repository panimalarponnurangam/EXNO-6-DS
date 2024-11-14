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
NAME : PANIMALAR P
REG NO : 212222110031
```
```
import seaborn as sns
import matplotlib.pyplot as plt
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
```
![327918503-1c8ab253-15f0-4b45-8caa-13ab87b620d0](https://github.com/user-attachments/assets/8708e8c4-9514-4d82-87af-1c4cf57739a2)
```
df=sns.load_dataset("tips")
df
```
![327918507-95a2ed6d-ef61-4344-be6d-175b073b5192](https://github.com/user-attachments/assets/955ff972-fbfd-438d-b317-adace48ef352)
```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![327918510-99b1f75a-f56a-48fe-91c7-4b6d4cca4c62](https://github.com/user-attachments/assets/00388cd9-4ffd-4c58-9785-fbb4b303bccd)
```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-line Plot")
plt.xlabel('X Label')
plt.ylabel('Y Label')
```
![379625514-cc0ebebf-7ecd-4ef9-9360-885302505997](https://github.com/user-attachments/assets/c7f54086-35c4-4d8c-8f88-c7bbc03624bc)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![327918517-fd7c2a3a-b168-44b2-8892-0ac6d388adf9](https://github.com/user-attachments/assets/70e80fac-78d1-4cc6-96b1-1010a4103f57)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip = tips.groupby('time')['tip'].mean()
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)

plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```

![327918524-5c9a4aca-7887-4bab-9bf7-a441a31ed425](https://github.com/user-attachments/assets/db918b77-4b6d-4cc1-ac80-473b0c7b7c64)

```
years=range (2000, 2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![327918526-6fdee4e0-c832-43c3-9917-afff4e1375f8](https://github.com/user-attachments/assets/fa6b6b00-d388-4273-9dee-d5888424de47)
```
import seaborn as sns
dt= sns.load_dataset('tips')
# Bar plot with hue parameter
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![327918530-e9a48fc4-a932-4043-87ed-c46d30d52d7c](https://github.com/user-attachments/assets/a3bd63ff-be2a-433d-b0c5-8ce517ba20ed)
```
import seaborn as sns
# Load the tips dataset
tips = sns.load_dataset('tips')
# Scatter plot of total bill vs. tip amount
sns.scatterplot(x= 'total_bill', y='tip', hue='sex',data=tips)
# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![327918533-3694fb1b-176a-4696-aa5d-c3b1fc7b4260](https://github.com/user-attachments/assets/596712ca-58b4-4d9b-9a7e-92bbf4dfb17a)
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
marks
```
![327918537-eee0727e-d897-4540-ae5a-83cb6f59b847](https://github.com/user-attachments/assets/c19c8712-27c8-4942-88b8-a8e550277145)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,
palette="Set3", inner="quartile")
# Add labels and title
plt.xlabel("Day of the week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![327918540-98fb5506-36c4-4824-bfdd-7b260a2a2752](https://github.com/user-attachments/assets/87bdf59e-bff5-4c11-9acc-d78b3faa090f)
```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![327918546-29596560-6a54-4051-9c55-0903af5c0665](https://github.com/user-attachments/assets/f4a4acb1-6830-4ef5-846e-cdab3f89d1cd)
```

import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
````
![327918551-7323ef13-38b2-472b-9146-e68f7f5049df](https://github.com/user-attachments/assets/47db8136-13b5-4ce8-9ceb-d5a1a673047f)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![327918553-322e04f2-b84b-4477-be92-23e22385feac](https://github.com/user-attachments/assets/da717e65-1e45-486d-905d-15d7b9a7a676)
```
sns.histplot(data=marks, bins=10, kde=True, stat='count', cumulative=False, multiple='stack', element='bars', palette='Set1', shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of students Marks')
```
![327918565-b95a290d-8aa5-421b-910f-a8d05f0db533](https://github.com/user-attachments/assets/4a75a0a4-7ff6-489b-97a6-72673ca08647)

![327918569-15ad7faa-d749-4ae6-8540-e56e79949db3](https://github.com/user-attachments/assets/c75c4fbb-39df-4e58-b557-5f46a4187a28)


# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
