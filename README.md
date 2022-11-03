# Cryptocurrencies
#### *Crypto Currency analysis using unsupervised machine learning, Python, and Jupyter Notebook*

## Overview

The purpose of this analysis was to analyze a dataset from different cryptocurrencies to identify trends that would assist a firm or person decide which to invest in. The main problem with cryptos is that the common ones, like bitcoin or ethereum, are becoming unaffordable for the majority of the public. With this in mind, I will be using unsupervised machine learning to determine if we can spot any trends that will result in opportunities for these altcoins. 

## Resources

Dataset:
  -crypto_data.csv

Software used: 
  - Python
  - Jupyter notebook
  - Sklearn, pandas, and hvplot libraries
  - Unsupervised Machine Learning


## Results

*Follow the code in the crypto_clustering.ipynb

I had to preprocess and transform the data so that unsupervised machine learning could work. This included dropping null values, using only tradaeble and mined cryptocurrencies, numerically encoding categorical columns using the `pandas.get_dummies` method, and scaling the data using the `StandardScaler()` method. 

I then proceeded with the Principal Component Analysis (PCA) to reduce the 98 scaled columns I had, to only 3 principal components. 

![Screenshot1]()

To determine how many clusters (k) I could divide the cryptos in, I created an elbow curve. 




![screenshot2]()

As it is displayed, the optimal result was 4 clusters. So, I proceeded with the KMeans analysis to fit the pca dataframe and predict the clustering. The product was this clustered_df with a 'Class' column that showed the predictions to which group it belonged to. 

![Screenshot3]()

lastly, I built some visualizations to better interpret the results. 

![screenshot4]()

This first one was a 3D scatter plot which located each clustered crypto in relation to the 3 principal components created on the PCA. As it is seen, there are 3 major groups and one outlier. 

![screenshot5]()

When trying to graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins (BitTorrent Crypto) and another one with a lot of supply but not too many coins mined (TurtleCoin). 

## Summary

The purpose of unsupervised machine learning is to indentify patterns or groups of data when there is no known output.This analysis was successful at grouping cryptocurrencies into 4 groups. If we were to configure a crypto investment portfolio we would need to further analyze the clusters. Endless to say, we have a good starting point where we can see that the most profitable and known cryptos are somewhat in the 2 groups that have less supply and mined coins in comparison to others. These cryptos are Bitcoin and Ethereum. Nevertheless, we should keep up with the innovations of technology where new altcoins are being created with very interesting value propositions. 