# Kmeans 

kmeans algo clusters data by trying to separate samples in n groups of equal variance,
minimizing a criterion known as the inertia or wihtin-cluster sum-of-squares

requires:
- the number of clusters to be specified
- scales well to large number of samples

kmeans divides a set X of N samples into K disjoint clusters C
each cluster is described by the mean mu of the samples, called centroid
note that centroids are not in general points from X, although they live in the same space 
kmeans aims to choose centroids taht minimise the inertia:
sum(min(|xi-muj|^2)

inertia, or the within-cluster sum of squares criterion, is a measure of how internally coherent clusters are 
drawbacks : 
- inertia makes the assumption that clusters are convex and isotropic (which is not always the case)
  it responds poorly to elongated clusters or manifolds with irregular shapes.
- inertia is not a normalized metric (zero is optimal)
  in very high-dimensional spaces , euclidean distances tend to become inflated (curse of dimensionality)  
  running a PCA prior to k-means can alleviate this problem and speed up the computation

kmeans has 3 steps : 
1. choose the initial centroids 
2. create new centroids by taking the mean value of all of the samples assigned to each previous centroid
the difference between the old and new centroids are computed 
3. the algo repeats these laast steps until this value is less than a threshold 
in other words, it repeats untill hte centroids do not move significantly

kmeans is equivalent ot the xprectation-maximization algorithm with a small, all-equal, diagonal cov matrix


kmeans will always converge, however this may be to a local minimum, it depends on the initialization fo the centroids
as a result, the computation is often done several times with different init of centroids 

The common stopping conditions I have seen:
- Convergence. (No further changes) : |the vector of means in t |m(t)-m(t-1)| < gamma : conv threshold
- Maximum number of iterations.
- Va<riance did not improve by at least x
- Variance did not improve by at least x * initial variance

If you use MiniBatch k-means, it will not converge, so you need one of the other criteria. The usual one is the number of iterations.

# Mini Batch K-Means
