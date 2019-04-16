
KNN : K-Nearest Neighbours

works for regression and classification problems

How knn works ?

- calculate the distance between a point in the testing data with all points in the training data
- sort the different distances 
- keep the top k 
- make a majority vote between the k labels
- label the test instance with the label as result of the vote


How we choose k ?
- k must be odd, so that we don't have any tights during the votes 
- draw an ‘elbow curve‘ 
