# Cryptocurrency Clusters

## Steps

### Data Preparation

* Read `crypto_data.csv` into Pandas. The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

* Discarded all cryptocurrencies that are not being traded & dropped the `IsTrading` column from the dataframe.

* Removed all rows that have at least one null value.

* Filtered for cryptocurrencies that have been mined so that the total coins mined should be greater than zero.

* Delete the `CoinName` from the original dataframe so that the dataset to be comprehensible to a machine learning algorithm.

* Converted the remaining features with text values, `Algorithm` and `ProofType`, into numerical data. I used Pandas to create dummy variables and examine the number of rows and columns of the dataset.

* Standardized the dataset so that columns that contain larger values do not unduly influence the outcome.

### Dimensionality Reduction

* Creating dummy variables above dramatically increased the number of features in your dataset.

* Reduced the dataset dimensions with t-SNE and visually inspect the results. In order to accomplish this task, I ran t-SNE on the principal components: the output of the PCA transformation. Then created a scatter plot of the t-SNE output..

### Cluster Analysis with k-Means

* Created an elbow plot to identify the best number of clusters and used a for-loop to determine the inertia for each `k` between 1 through 10.

### Recommendation

* Based on your findings, make a brief (1-2 sentences) recommendation to your clients. Can the cryptocurrencies be clustered together? If so, into how many clusters? 


## References

Crypto Coin Comparison Ltd. (2020) Coin market capitalization lists of crypto currencies and prices. Retrieved from [https://www.cryptocompare.com/coins/list/all/USD/1](https://www.cryptocompare.com/coins/list/all/USD/1)

