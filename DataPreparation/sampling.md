In each sub-sample, observations are drawn from the population, either with or without replacement. Whenever possible, drawing without replacement is the preferred method as it leads to maximum variance reduction, with no duplicated observations. Interesting cases include:

** Leaving-one-out method **: Each sub-sample consists of N-1 distinct observations. We just remove one observation in turn from the population, to create each sub-sample. 
** Adding-one-over method **: This is the dual version of the leaving-one-out method, but it is never mentioned in the literature. Each sub-sample consists of N+1 observations, with N distinct observations. One  observation (different for each sub-sample) is duplicated in each sub-sample. 
** Bootstrapping **: Each sub-sample consists of N observations, drawn with replacement from the original population. So the proportion of duplicated observations in each sub-sample is high. The expected number of distinct observations in each sub-sample is of the order (1 - exp(-1)) N. 
** K-fold cross-validation **: In this machine learning technique, the original data set is split into K subsets, with one of them used for validation, and K-1 used for training. Typically, sampling is done without replacement, and the sub-samples form a partition of the original data set.


https://www.analyticsvidhya.com/blog/2019/09/data-scientists-guide-8-types-of-sampling-techniques/?utm_source=feedburner&utm_medium=email&utm_campaign=Feed%3A+AnalyticsVidhya+%28Analytics+Vidhya%29
