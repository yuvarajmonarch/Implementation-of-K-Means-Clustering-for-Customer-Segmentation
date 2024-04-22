# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas and matplotlib.pyplot
2. Read the dataset and transform it
3. Import KMeans and fit the data in the model
4. Plot the Cluster graph

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: YUVARAJ B
RegisterNumber: 212222040186

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1) (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []  #Within-Cluster sum of square. 
for i in range(1,11):
  kmeans=KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")


*/
```

## Output:
#### data.head() function
![Screenshot 2023-06-03 174421](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/4ddf5cc1-60a4-4f52-9101-d0c664fef559)

#### data.info()
![Screenshot 2023-06-03 174451](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/c980ee78-5b2d-4787-a428-599f1c6a1a9a)

#### data.isnull().sum() function
![Screenshot 2023-06-03 174514](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/e32c9584-db05-47f7-8953-c573ab2bd24b)

#### Elbow method Graph
![Screenshot 2023-06-03 174540](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/12f65900-41fe-4ea8-8a3e-23b53f3ddd63)

#### KMeans clusters
![Screenshot 2023-06-03 174604](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/c8cda73d-62dd-4850-a950-ffe8015453b9)

![Screenshot 2023-06-03 174609](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/24988003-5833-48d9-b5c6-bc95d368c31f)

#### Customer segments Graph
![Screenshot 2023-06-03 174648](https://github.com/Yamunaasri/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/115707860/f6c560cf-f5bb-4719-b6a4-eefd4cece1e0)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
