# Cryptocurrency-Clusters
### Unsupervised Machine Learning Ctryptocurrency Analysis 

## Introduction

In the proposed scenario I am part of the Advisory Services Team of a financial consultancy.  A client, a prominent investment bank, is interested in offering a new cryptocurrency investment profolio to its customers.  I will create a report that includes what cryptocurrencies are on the trading market and determine if they can be grouped to create a classification system.

## Methods

Raw data is provided for analysis. The data was cleaned in Jupyter notebooks using pandas.  Cryptocurrency not being traded were removed.  Rows with at least one null value were removed. The dataframe was then filtered for cryptocurrencies that have been mined.  Coin names were removed and data with text values was converted into numerical data via creation of dummy variables.  Data was standardized using StandardScaler from sklearn.  Dimensionality Reduction was performed using PCA preserving 90% of the explained variance and t-SNE.  An elbow plot was then cretaed to identify the best number of clusters. 

## Analysis/ Results

The dataset started with 1252 rows and 7 columns of data. There are 1144 Cryptocurrencies being traded, that column was then removed.  Removal of the null values resulted in (685, 6).  Filtering for mined Cryptocurrencies left the dataset at (532, 6).  The shape of the dataset was (532, 98) after removal of the CoinName and Unnamed columns and using get_dummies on the Algorithm and ProofType columns.  The PCA dimensionality reduction was performed resulting in  (532, 74) data set shape.  Lastly after applying the t-SNE dimenionality reduction the final dataset shape is (532, 2).

The resulting scatter plot of the t-SNE output :

![t-SNE scatter plot](https://user-images.githubusercontent.com/88807979/153791574-13d6bcf8-3d9a-4d41-b3a0-e33bc1936462.png)

The elbow plot for identification of clusters:

![elbow plot](https://user-images.githubusercontent.com/88807979/153791592-5fd6f5b6-2c0e-4198-8774-045308e32afe.png)

## Discussion/ Conclusion

After the removal of non traded cryptocurrencies and filtering the data set for currency that have not been mined the resulting data set was analyzed. Based on the resulting elbow plot the 532 remaining crytocurrencies could be clustered into 3 clusters, based on the bend in the data.
