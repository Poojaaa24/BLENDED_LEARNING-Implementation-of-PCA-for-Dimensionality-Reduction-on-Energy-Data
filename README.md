# BLENDED LEARNING
# Implementation of Principal Component Analysis (PCA) for Dimensionality Reduction on Energy Data

## AIM:
To implement Principal Component Analysis (PCA) to reduce the dimensionality of the energy data.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required Python libraries and load the HeightsWeights dataset using pandas.

2. Select the features (Height and Weight) and standardize the data using StandardScaler.

3. Apply Principal Component Analysis (PCA) to reduce the dataset into principal components.

4. Visualize the transformed data using a scatter plot of PC1 and PC2.

## Program:
```
/*
Program to implement Principal Component Analysis (PCA) for dimensionality reduction on the energy data.
Developed by: POOJA U
RegisterNumber:  212225230209
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
import seaborn as sns
data=pd.read_csv('HeightsWeights.csv')
print("First 5 rows of a dataset:")
print(data.head())
print(data.columns)
X=data[['Height(Inches)','Weight(Pounds)']]
plt.figure(figsize=(6,5))
sns.scatterplot(x='Height(Inches)',y='Weight(Pounds)',data=data)
plt.title("Original Data Distribution")
plt.show()

scaler=StandardScaler()
X_scaled=scaler.fit_transform(X)

pca=PCA(n_components=2)
X_pca=pca.fit_transform(X_scaled)

print("Name: POOJA U")
print("Reg Num: 212225230209")
print("Explained Variance Ratio:",pca.explained_variance_ratio_)

pca_df=pd.DataFrame(X_pca,columns=['PC1','PC2'])


plt.figure(figsize=(6,5))
sns.scatterplot(x='PC1',y='PC2',data=pca_df)
plt.title("PCA Projection of Height and Weight")
plt.xlabel("Principale Component 1")
plt.ylabel("Principle Component 2")
plt.show()

*/
```

## Output:



## Result:
Thus, Principal Component Analysis (PCA) was successfully implemented to reduce the dimensionality of the energy dataset.
