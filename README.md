# Customer-Segmentation
In this project, my goal is suggest recommendations to the superstore for increasing sales. For increaing sales, the superstore should announce offers. I should analyse the data, uncover insights and based on insights, give rceommmendatsions for offer schemes that will be well recieved, increasing sales.

I have the data from superstore in CSV file.

After data loading, there is general data exploration and data cleaning. My approach is to apply Exploratory Data Analysis(EDA) and then Customer Segmentation.

In EDA, I have done following things:
- looked at descriptive statistics
- fitted probability distributions using scipy's stats module
- created insightful charts using seaborn and matplotlib libraries.

I have done customer segmentation on demographic basis(Demographic Segmentation). I have experimented with K-Means Clustering and DBSCAN(Density-Based Spatial Clustering of Applications with Noise). I optimized for silhoutte score. For tuning K-Means, I used Elbow method. In elbow method, I focus on the point where further adding clusters doesn't decrease WCSS(Within-Cluster Sum of Squares) significantly. This point is called elbow point and we choose it as the number of clusters. With K-Means, I achieved a silhouette score of 0.24 with K=4. In tuning DBSCAN, I first found the best number of min samples. I found the best value is 4. Then for that min samples, I constructed a K-distance plot to find radius. In the K-distance plot, I looked for elbow and experimented around it. The best radius is found to be 0.4. With this, I was able to achieve a silhoette score of 0.38. But, I went for K-Means finally because, in DBSCAN, the number of clusters was coming at 74, which is impractically high. I then analysed the clusters.

Finally, I made recommendations based my EDA and Cluster Analysis(Customer Segmentation).
