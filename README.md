![280221177-f50bd4c8-8840-4d61-afa9-f090d98716d2](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/6b24eb96-4a2c-434c-92a9-246c57e1bf37)# Ex-08-Data-Visualization-
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
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/4a5b9a47-e60e-4faf-92ed-3d3cc513818">
<img src="https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/8c02f032-c237-4743-83ef-75a9203c9e47"height=300 width=350>
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
<img src="![280221836-16ece634-b224-42df-82be-c4a731f908af](https://github.com/Adhithyaram29D/ODD2023-Datascience-Ex-08/assets/119393540/69b310d0-7686-465b-8033-7ea17a0833d8)
" height=500 width=350>
<img src="" height=300 width=350>

- <B>_POINTPLOT_</B>
```python
sns.pointplot(x=df["Quantity"],y=df["Discount"])
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/cc5c01fb-bc88-4f6e-8f53-08e45f679e08" height=300 width=350>

- <B>_COUNT PLOT_</B>
```python
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/b6e8298d-0a6c-4a58-85b6-6a0e5c53508f" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/a9e07021-4889-490c-8451-69864bf6f778" height=300 width=350>

- <B>_HISTOGRAM_</B>
```python
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
``` 
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/6e5a4fab-1cfd-4415-9a76-6e398571742b" height=300 width=350>

- <B>_KDE PLOT_</B>
```python
sns.kdeplot(x="Profit", data = df,hue='Category')
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/2129a043-381c-4b04-a0da-5b6745ba0adf" height=300 width=350>

### DATA VISUALIZATION USING MATPLOTLIB :
- <B>_PLOT_</B>
```python
plt.plot(df['Category'], df['Sales'])
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/5f621aad-c520-4e01-96cf-1701acefa1e7" height=300 width=350>


- <B>_HEATMAP:_</B>
```python
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/d133809e-1704-4f91-8332-0041d7ca3e33" height=300 width=350>

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
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/09b81541-1b03-4017-bd64-e20c6894898b" height=300 width=350>
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/76eb96a0-0bec-4d40-af21-f906b45b9c16" height=300 width=350>

- <B>_HISTOGRAM:_</B>
```python
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/5d549a00-18a3-4126-af87-1652098f826d" height=300 width=350>

- <B>_BARGRAPH:_</B> 
```python
plt.bar(df.index,df['Category'])
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/bee209ed-e0f9-4968-94c7-babc9140edfb" height=300 width=350>

- <B>_SCATTERPLOT:_</B>
```python
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/82653e8a-3f2a-4a58-ae41-0631925cd402" height=300 width=350>

- <B>_BOXPLOT:_</B>
```python
plt.boxplot(x="Sales",data=df)
plt.show()
```
<img src="https://github.com/Janarthanan2/ODD2023-Datascience-Ex-08/assets/119393515/9515bcd2-15ba-453a-a02e-e3e6e3ea875c" height=300 width=350>

# RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
