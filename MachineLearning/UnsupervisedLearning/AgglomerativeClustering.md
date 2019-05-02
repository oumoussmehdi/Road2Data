# Agglomerative Clustering

performs a hierarchical clustering using a bottom up approach :
each obs starts in its own cluster, and clusters are successively merged together
the linkage criteria determines the metric used for the merge startegy :
- Ward :  min sum of squared differences within all clusters
- Maximum or complete linkage : min max dist between obs of pairs of clusters
- average linkage : min avg dist all obs of pairs of clusters 
- single linkage : min the dist between the closest obs of pairs of clusters 

connectivity constraints
