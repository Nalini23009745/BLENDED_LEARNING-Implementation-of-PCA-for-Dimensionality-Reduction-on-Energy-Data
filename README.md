# BLENDED LEARNING
# Implementation of Principal Component Analysis (PCA) for Dimensionality Reduction on Energy Data

## AIM:
To implement Principal Component Analysis (PCA) to reduce the dimensionality of the energy data.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import Libraries: Import pandas, PCA, StandardScaler, and matplotlib.
2.Load Data: Load the dataset using pandas.read_csv().
3.Select Features: Choose 'Height(Inches)', 'Weight(Pounds)', 'Weight(Kilograms)' for PCA.
4.Scale Data: Standardize the features with StandardScaler.
5.Perform PCA: Apply PCA to reduce the data to 2 components.
6.Create PCA DataFrame: Convert the PCA output into a DataFrame.
7.Visualize Data: Plot the data in 2D using a scatter plot.
8.Explain Variance: Print the explained variance ratio for each component and the total variance.
``` 

## Program:
```
/*
Program to implement Principal Component Analysis (PCA) for dimensionality reduction on the energy data.
Developed by: Nalini P
RegisterNumber: 212223220063
*/
```python
# Import necessary libraries  
import pandas as pd  
from sklearn.decomposition import PCA  
from sklearn.preprocessing import StandardScaler  
import matplotlib.pyplot as plt  

# Load the dataset  
df = pd.read_csv(r'C:\Users\admin\Downloads\HeightsWeights.csv')  

# Select the relevant features for PCA  
features = df[['Height(Inches)', 'Weight(Pounds)', 'Weight(Kilograms)']]  

# Scale the data using StandardScaler  
scaler = StandardScaler()  
scaled_features = scaler.fit_transform(features)  

# Perform PCA to reduce dimensionality to 2 components  
pca = PCA(n_components=2)  
pca_features = pca.fit_transform(scaled_features)  

# Convert PCA features to a DataFrame  
pca_df = pd.DataFrame(pca_features, columns=['Principal Component 1', 'Principal Component 2'])  

# Visualize the data in 2D space  
plt.scatter(pca_df['Principal Component 1'], pca_df['Principal Component 2'])  
plt.title('Data in 2D Space using PCA')  
plt.xlabel('Principal Component 1')  
plt.ylabel('Principal Component 2')  
plt.show()  

# Print the explained variance ratio for each principal component  
explained_variance_ratio = pca.explained_variance_ratio_
print("Explained Variance Ratio (Individual):", explained_variance_ratio)

# Calculate and print the total explained variance ratio  
total_explained_variance = explained_variance_ratio.sum()
print("Total Explained Variance Ratio:", total_explained_variance)
/*
Program to implement Principal Component Analysis (PCA) for dimensionality reduction on the energy data.
Developed by: 
RegisterNumber:  
*/
```

## Output:
![image](https://github.com/user-attachments/assets/db9bebad-0da7-4632-88b2-e76e55cd598a)
![image](https://github.com/user-attachments/assets/781d621c-452d-4592-a41f-4039c6ec8d65)



## Result:
Thus, Principal Component Analysis (PCA) was successfully implemented to reduce the dimensionality of the energy dataset.
