# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
- STEP 1:
 Read the given Data
- STEP 2:
 Clean the Data Set using Data Cleaning Process
- STEP 3:
 Apply Feature generation and selection techniques to all the features of the data set
- STEP 4:
 Apply data visualization techniques to identify the patterns of the data.

### READING THE GIVEN FILES
```python
import pandas as pd
df=pd.read_csv("/content/Superstore.csv",encoding='unicode_escape')
df.head()
```
### DATA VISUALIZATION USING SEABORN :
```
import seaborn as sns
from matplotlib import pyplot as plt
```
- <B>_LINE PLOT:_</B>
```python
plt.figure(figsize=(9,6))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/4aab30cb-a4a8-45d1-8bae-aceeb0eca278" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/8c02f032-c237-4743-83ef-75a9203c9e47" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/2aecf214-5be9-4594-83dd-1df66e763f21)" height=300 width=350>

- <B>_SCATTERPLOT:_</B>
```python
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/f38352d4-504c-4926-b6e7-512734888392" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/2bb1b565-0c26-4730-998a-64c6a81ac3ac" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/4f77f0e1-2fe2-4fb2-900f-6f3940bd6ee9"height=300 width=350>

- <B>_BOXPLOT:_</B>
```python
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/f230a62e-f13f-416a-ae1e-0086c2922bcb" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/e21b3b38-3517-45c6-80ad-f44daf9679f7" height=300 width=350>

- <B>_VIOLIN PLOT:_</B>
```python
sns.violinplot(x="Profit",data=df)
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/bb267ffa-c369-47d1-be47-05fe4137ea85" height=300 width=350>

- <B>_BARPLOT_</B>
```python
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/69b310d0-7686-465b-8033-7ea17a0833d8" height=500 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/9291dcfb-d723-49fd-b33c-58ad22a16809" height=300 width=350>

- <B>_POINTPLOT_</B>
```python
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/b6a6f701-ebda-4fcb-a307-fde1f02045a2" height=300 width=350>

- <B>_COUNT PLOT_</B>
```python
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/7b9191b4-d75e-4dfe-a051-04b6ba045d96" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/e3c70bf2-4703-43b1-b695-eab0559eded0" height=300 width=350>

- <B>_HISTOGRAM_</B>
```python
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/73c5c5c3-606e-4030-9406-801e7775649d" height=300 width=350>

- <B>_KDE PLOT_</B>
```python
sns.kdeplot(x="Profit", data = df,hue='Category')
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/253bae47-e0ad-4ca3-9643-648af77da202" height=300 width=350>

### DATA VISUALIZATION USING MATPLOTLIB :
- <B>_PLOT_</B>
```python
plt.plot(df['Category'], df['Sales'])
plt.show()
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/0549a345-7dc0-4616-9a29-95accc134733" height=300 width=350>


- <B>_HEATMAP:_</B>
```python
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/4a74ae29-1c3c-4745-82ef-dd8167e7feb9" height=300 width=350>

- <B>_PIECHART:_</B>
```python
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/3bdf032f-371c-4225-aeb6-641d22090907" height=300 width=350>
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/d29ea959-ff0d-490d-9867-68f86406188b" height=300 width=350>

- <B>_HISTOGRAM:_</B>
```python
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/d40c0a4d-3fec-46b5-828f-7b95db50ee83" height=300 width=350>

- <B>_BARGRAPH:_</B> 
```python
plt.bar(df.index,df['Category'])
plt.show()
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/a551d5d6-d08b-4331-8c27-80848cc9992f" height=300 width=350>

- <B>_SCATTERPLOT:_</B>
```python
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/b49ce246-8246-4c50-b00e-217ea3ec7c1d" height=300 width=350>

- <B>_BOXPLOT:_</B>
```python
plt.boxplot(x="Sales",data=df)
plt.show()
```
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/e693ef94-1aee-49e7-8851-098c10d32775" height=300 width=350>

# RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
