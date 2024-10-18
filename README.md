# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program



## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: VINOTH M P
RegisterNumber: 212223240182

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
print("data.head()")
data.head()
print("data.info()")
data.info()
print("data.isnull()")
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]
for i in range(1,11):
    kmeans=KMeans(n_clusters=i,init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
KMeans(n_clusters=5)
y_pred=km.predict(data.iloc[:,3:])
print("Prediction")
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="green",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="pink",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="yellow",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="blue",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
![Screenshot 2024-10-18 205024](https://github.com/user-attachments/assets/03029fec-cd69-4724-8edb-2f2557d12033)

![Screenshot 2024-10-18 205032](https://github.com/user-attachments/assets/62b3bef7-8de4-433e-81e5-1a9d9481381e)

![Screenshot 2024-10-18 205037 (1)](https://github.com/user-attachments/assets/333939c4-c2a1-44fa-94c5-fc2e6cd0f9e9)


![unnamed](https://github.com/user-attachments/assets/ae8da30d-7bb7-464a-8f61-3afa45939fc0)

![unnamed](https://github.com/user-attachments/assets/7ea60be4-1291-4e2b-9617-104031d4423f)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.

