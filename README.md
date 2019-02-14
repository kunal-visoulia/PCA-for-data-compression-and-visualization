# PCA-for-data-compression
Data Compression and Visualization using Principle Component Analysis (PCA) in Python

## DATASET
I used the standard Iris Dataset from sklearn. No preprocessing was required other than converting the daaset to a pandas dataframe.

## Methodology
![](images/1.png)
Petal length and Petal Width shows very high linear correlation ,i.e., they can be compressed down(reduced to its principle components) to a single feature using PCA reduction.<br/> Sepal length and Sepal width are somewhat correlated so they can be reduced too.

We see almost none random distribution of data and clusters are also visible(Obviously deep neural n/ws or even a simple neural n/w will give amazing results but still clustering algo will work good too)

There were 3 classes in the dataset, but still to for experimentation purposes I used Elbow Method to determine the appropriate number of clusters for a dataset. I took number of clusters from 1 to 30 and calculated **average within-cluster sum of squares**(awcss,averaged over 150 so as to not get total wcss which is actually the inertia) for each value and plotted the following curve:<br/>
![](images/2.png)<br/>
From the curve, optimal number of clusters is 3 as it right on the elbow(it may seem 4 could be too, but as seen later, it is not)


