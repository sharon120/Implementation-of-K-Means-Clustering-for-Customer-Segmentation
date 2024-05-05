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

5.Print the outputs and end the program.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Sharon Harshini L M
RegisterNumber: 212223040193
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv(r'Mall_Customers.csv')

data.head()
data.info()
data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
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
Head()

![325059598-b456b834-cd05-4854-ae81-9bdfed9b3c6a](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/e50d1c7a-babc-490b-988e-9abcad499402)

Info()

![325059830-e57cb1e9-621e-46e2-83bb-b4886f663fa8](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/171c430a-1ef0-4db1-9bcc-4e02aee8dd59)

isnull.sum()

![325060452-c3e12196-8ca0-40c6-bdfe-e9a30411566c](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/d3a55785-6e3b-42d0-be96-d5d7fe3cba55)

Elbow method()

![325060077-75bcf084-8bd2-425d-ac42-72ae8b6b4870](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/f757c247-60bf-472c-ad7a-b5bfb8be4de5)

Fitting the no of clusters

![325060182-a6d6d758-7171-479b-9d41-6a7d23000f07](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/37a4f7b1-8e44-4113-ab7a-17151198d382)

Prediction of Y

![325060267-7582d183-b350-4875-b532-39cab3dcc4cb](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/29127f03-740e-4b0f-a01e-7077e55d6f08)

Customer Segments

![325060545-3e08df8f-5472-4583-aeef-3019bf0b9f85](https://github.com/sharon120/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/149555539/9c42a880-c101-4d1a-b9e4-93855e483cd3)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
