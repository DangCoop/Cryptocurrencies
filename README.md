# Cryptocurrencies
___
![](/Images/Front.jpg)

***Analysis the biggest part of Cryptocurrencies using unsupervised machine learning and Python***


## Overview
___
The goal of this project was to analyze a dataset of many alternative cryptocurrencies in order to identify trends that make a firm or individual want to invest in them. The problem with cryptocurrencies is that the most common ones, such as Bitcoin or Ethereum, become inaccessible to the general public due to their cost. With the help of unsupervised machine learning, we will try to calculate any alternatives and approach to them.

## Resources
___
- Datasets
    - [crypto_data.csv](/Resources/crypto_data.csv)
- Software
    - Python
    - VS Code
    - Sklearn and hvplot libraries
    - Unsupervised Machine Learning

## Results
Full code you can check [crypto_clustering.ipynb](/crypto_clustering.ipynb)

**`First step`** - preprocess and transform the data. This included 
dropping null values, using only tradaeble and mined cryptocurrencies, numerically encoding categorical columns using the `pandas.get_dummies` method, and scaling the data using the `StandardScaler()` method as well.
![](/Images/Step1:1.png)
![](/Images/Step2:2.png)
![](/Images/Step1:3.png)


**`Step Two`** is Principal Component Analysis (PCA) to reduce the number of columns available to three principal.
![](/Images/Step2.png)

**`Step Three`** - I created an elbow curve to check how many clusters is possible to use for dividing the cryptos
![](/Images/Step3.png)

As shown on curve - the optimal result was 4 clusters.

**`Step Four`** is a clustered_df table with a "Class" column that showed predictions of which group it belonged to.
![](/Images/Step4.png)

**`Step Five`** - I create some visualizations to better understand the results.

- [x] In the 3D scatter plot, you can see that each grouped crypto was located in relation to the three main components created on the PCA, there are 3 main groups and one outlier.
![](/Images/Step5.png) 

- [x] Similarly, when trying to graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins (BitTorrent Crypto) and another one with a lot of supply but not too many coins mined (TurtleCoin).
![](/Images/Step6.png)

## Summary
___
At the end of our analysis, we can state that we have successfully grouped cryptocurrencies into 4 groups. If we were going to create a portfolio of crypto investments, we would need further analysis of the clusters. However, we have a good starting point where we see that the most profitable and well-known cryptocurrencies are in about two groups that have less supply and mined coins compared to others.
The task of unsupervised machine learning is to discover patterns or groups of data when there is no known output. And as we have already checked on ourselves, it copes with this perfectly !!!
![](/Images/Back.jpg)
```Denis Antonov 10.27.2022```

```Contact: antonov.resu@gmail.com```
