# CryptoClustering

## Background 

In this challenge, I’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Data Preparation

* I used `StandardScaler()` module from `scikit-learn` to normalize the data. Then I created a DataFrame with the new scaled data.

* I found the best value for k using the original scaled DataFrame.
    * Created a list with a number of k values from 1-11.
    * Created an empty list to store the inertia values.
    * Created a `for` loop to compute the inertia with each possible value of `k`.
    * Created a dictionary with the data to plot the elbow curve.
    * Plotted a line chart with all the inertia calues computer with the different values of `k` to visually identify the optimal value for `k`.


* Here are the steps I used to cluster cryptocurrencies, aiming to find the best value for K using the original scaled data:
    
    * Initialized the K-Means Model with the Optimal K Value.

    * Fitted the K-Means Model on the Original Scaled Data.

    * Predict the Clusters.

    * Add the Predicted Clusters to a Copy of the Original Data.

    * Create a Scatter Plot with hvPlot.
    
    ~ Using hvPlot, I created a scatter plot to visualize the clusters. Here's how I configured the plot:

    - Set the x-axis to "PC1" and the y-axis to "PC2" to represent the principal components.

    - Colour the graph points based on the cluster labels derived from K-means.

    - Added the "coin_id" column to the hover_cols parameter, allowing me to identify which cryptocurrency each data point represents when I hover over it.

* I optimised clusters with Principal Component Analysis.
* I found the Best Value of k using the PCA data
* I created clusters for cryptocurencies with K-means using the PCA Data.
* Compared both plots and provided analysis.

## File list:
* `Crypto_Clustering_starter_code.ipynb`
* Resources Folder - containing CSV file with data 
* README.md