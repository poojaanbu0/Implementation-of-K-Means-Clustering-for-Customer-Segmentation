# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print head, info of the dataset

2.check for null values

3.Import kmeans and fit it to the dataset

4.Plot the graph using elbow method

5.Print the predicted array

6.Plot the customer segments

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Pooja A
RegisterNumber: 212222240072
##program##

import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans

wcss=[]

for i in range(1,11):

kmeans=KMeans(n_clusters=i,init="k-means++")

kmeans.fit(data.iloc[:,3:])

wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)

plt.xlabel("No.of.clusters")

plt.ylabel("wcss")

plt.title("Elbow Method")

km=KMeans(n_clusters=5)

km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])

y_pred

data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()

plt.title("customer segments")

*/
```

## Output:
# Data Head
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/d1464b78-a213-4899-a6a6-961efcfe69c4)

# Data Info
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/7d205035-e45b-413c-8b44-f27bba77d7d8)

# Total rows
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/1d43c7b3-9a09-4bb2-8c6c-4046b5d9e4e6)

# Clusters using Elbow method
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/489a603d-fce5-4434-8d99-e4fb302730e1)

# k-means clustering
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/8f76f12f-b6b1-4d48-8fad-115b42a385a1)

# y_pred data
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/e6c389a8-1152-47cf-89d5-f3126b2e0e16)

# Customer Segments graph
![image](https://github.com/poojaanbu0/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119390329/0405c1ef-6c0a-4cd7-9f43-7114f26b0cc7)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
