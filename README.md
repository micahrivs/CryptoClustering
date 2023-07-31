# CryptoClustering

## Project Overview
In this project, we will delve into the fascinating world of cryptocurrencies and explore their clustering using the powerful K-means algorithm. Clustering is a technique used to group similar data points together, and K-means is a popular unsupervised learning algorithm for this purpose. Our aim is to identify patterns and relationships among cryptocurrencies based on their market data.

## Instructions
To get started with this project, follow the step-by-step instructions provided below:

### 1. Rename Files
Before anything else, let's make things clear and organized. Rename the file "Crypto_Clustering_starter_code.ipynb" to "Crypto_Clustering.ipynb" for easy reference.

### 2. Load and Explore Data
It's essential to familiarize ourselves with the data. Load the market data from "crypto_market_data.csv" into a DataFrame. Once loaded, check the summary statistics and plot the data to gain an initial understanding of its distribution and characteristics.

### 3. Prepare the Data
For accurate clustering, we need to normalize the data from the CSV file. To achieve this, use the StandardScaler() module from scikit-learn to perform data normalization. Next, create a new DataFrame with the scaled data, and importantly, set the "coin_id" column from the original DataFrame as the index for the new DataFrame.

### 4. Find the Best Value for k Using the Original Scaled DataFrame
Determining the optimal number of clusters (k) is critical to obtaining meaningful results from K-means. Utilize the elbow method to find the best value for k using the following steps:

Create a list with k values ranging from 1 to 11.
Compute the inertia (within-cluster sum of squares) for each value of k and store the values in a list.
Plot a line chart with inertia values against different values of k to visually identify the best k.
Answer the question in the notebook: What is the best value for k?

### 5. Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Now that we have the best value for k, let's proceed with the clustering process using the original scaled DataFrame. Follow these steps:

Initialize the K-means model with the best value for k obtained in the previous step.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters for each cryptocurrency using the original scaled DataFrame.
Create a copy of the original data and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot with "PC1" on the x-axis, "PC2" on the y-axis, and color the points based on the K-means labels. Also, include the "coin_id" column in the hover to identify each cryptocurrency.

### 6. Optimize Clusters with Principal Component Analysis (PCA)
Principal Component Analysis (PCA) allows us to reduce the feature dimensionality and visualize the data better. Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components. Retrieve the explained variance for each principal component and answer the question in the notebook: What is the total explained variance of the three principal components?

Create a new DataFrame with the PCA data and set the "coin_id" column from the original DataFrame as the index.

### 7. Find the Best Value for k Using the PCA Data
Now, we need to find the best value for k using the PCA data. Repeat the elbow method using the following steps:

Create a list with k values ranging from 1 to 11.
Compute the inertia for each value of k and store the values in a list.
Plot a line chart with inertia values against different values of k to visually identify the best k.
Answer the question in the notebook: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

### 8. Cluster Cryptocurrencies with K-means Using the PCA Data
With the optimal value for k determined from the PCA data, proceed with clustering using the following steps:

Initialize the K-means model with the best value for k obtained in the previous step.
Fit the K-means model using the PCA data.
Predict the clusters for each cryptocurrency using the PCA data.
Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot with "price_change_percentage_24h" on the x-axis, "price_change_percentage_7d" on the y-axis, and color the points based on the K-means labels. Also, include the "coin_id" column in the hover to identify each cryptocurrency.

### 9. Answer the Final Question
Finally, in the notebook, answer the following question: What is the impact of using fewer features to cluster the data using K-Means?
