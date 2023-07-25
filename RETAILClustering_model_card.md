# Model Card

## Model Description
The models used in the notebook are clustering algorthims i.e. k-means clustering and hierarchical clustering to perform a RFM (Recency, Frequency, Monetary) analysis of customer transaction data and create customer clusters to derive targeted marketing strategies.

**Input:** 
The input into the model is customer transaction data. The original data includes Invoice Number, Customer ID, product description, Stock code, Date of ordering, quantity, unit price, Country. 
Therewith, 3 new features per customer are engineered to conduct the RFM analysis.
- recency (how many days there are between the last transaction of the customer and the most recent transaction in the overall dataset)
- frequency (how many orders customer placed in a certain timeframe)
- monetary (how large the sales volume in $ is the company made with this customer)


**Output:** 
The output of the model are 3 customer clusters that can be described based on the features given above.
Cluster 0: The "lost" customers (lots of days since last order, low total monetary order volume, low frequency)
Cluster 1: The most valuable customers (very recent orders, high total monetary order volume, high frequency of ordering)
Cluster 2: The new customers (recent orders, moderate total monetary order volume, limited frequency)

**Model Architecture:** 
Kmeans model and AgglomerativeClustering from sklearn package has been used.
Kmeans:
- Scaling of data: Standardization with mean 0 and variance 1
- Hyperparameter tuning: Using Elbow rule to identify 3 clusters
- Modeling: Default sklearn settings used (e.g. max_iter = 300)

Hierarchical:
- Dendogramm
- Agglomorative clustering
- Distance metric chosen: Euclidian

## Performance
To measure the performance of the model the silhouette score is used to assess how well similarity / dissimilarity has been identified by the algorithm.
The score is bounded between -1 for incorrect clustering and +1 for highly dense clustering. Scores around zero indicate overlapping clusters. The score is higher when clusters are dense and well separated, which relates to a standard concept of a cluster.
For k-means clustering is 0.51 and for hierarchial clustering the score is 0.45.

## Limitations
The dataset is quite old and the features available quite limited. To draw conclusions the model should be applied to more recent datasets.

## Trade-offs
Hierarchical clustering can suffer from myopic decisions whereas k-means clustering can lead to less intuitive results that can be harder to explain. Besides, computational time might be more intensive for k-means. In this case both methods seem to end up with similar clusters. Nevertheless this must not always be the case. For future usage these trade-offs need to be considered when deciding for certain method and respective clusters. 
