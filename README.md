# Crypto Clustering

This challenge looks into various cryptocurrency datas and examines their price changes over different time periods. Selected time intervals are 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year. The data was noramlized by using the Standard Scaler.


### Summary

Best k value is found by creating an elbow curve. I used the original scaled data and computed its inertia values with all possible k values. By observing the line graph, best k value was found to be 4. 

Then, this k value was used to create a new KMeans model and predict the clusters. The scatter plot compares and visualizes two features, price change in 24 hours and 7 days, with the predicted clusters.

PCA model was also used to find out the explained variances and create an elbow curve again. The best k value turns out to be 4 which is the same value we got by using the original scaled data. PCA values also helped to determine the influences of each time interval features on each component.


### Conclusion

By using two different methods to get the elbow curve, best k value was found to be 4.

For PCA1, price_change_percentage_200d has the strongest positive influence and price_change_percentage_24h has the strongest negative influence.

For PCA2, price_change_percentage_30d has the strongest positive influence and price_change_percentage_1y has the strongest negative influence.

For PCA3, price_change_percentage_7d has the strongest positive influence and price_change_percentage_60d has the strongest negative influence.