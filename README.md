#  Cryptocurrencies

## Overview
I used unsupervised machine learning with principal component analysis and K Means to classify various cryptocurrencies and display the clustered results.

## Resources
- Crypto_data.csv
- Python Pandas, Scikit, Imbalance, Hvplot
- Jupyter Notebook, VS Code

## Process
I read in the data from the .csv file, then worked on the transformation of the data to ensure I was working with currently traded cryptocurrencies that were actively being mined.  I then made sure I could use the data for the crypto algorithm and proof-type with the `get_dummies()` method.

I then used `StandardScaler()` to scale the data and employed the Principal Component Analysis algorithm to reduce the number of inputs to 3 components.

Using the Elbow Curve on the data, I found it best to use a KMeans of 4 to run the model.

![image](https://github.com/jakatz87/Cryptocurrencies/blob/main/Resources/Elbow%20Curve.png)

Once the model was run, I created a comprehensive DataFrame with all the cryptocurrency information and the projected Classes from the Machine Learning model.

![image](https://github.com/jakatz87/Cryptocurrencies/blob/main/Resources/Clustered_df.png)

## Results
The 3 Dimensional Scatterplot shows that the KMeans of 4 was the right amount, even though there was one outlier in its own class: BitTorrent

![image](https://github.com/jakatz87/Cryptocurrencies/blob/main/Resources/scatter_3d.png)

I then created a 2 D Plot to show tradable coins by supply and number of coins mined.

![image](https://github.com/jakatz87/Cryptocurrencies/blob/main/Resources/hvplot.png)


## Summary
Based on the 2 D Plot, it would seem TurtleCoin would have the highest potential in investment, as its supply is high, although the number of coins mined is low.  
Overall, I would question the accuracy of this model, since running the PCA Explained Variance Ratio, `pca.explained_variance_ratio_`, resulted in extremely low accuracy, below a 7% total.  

