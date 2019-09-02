# Noise

Noise in tabular data can be of three types:

1. Anomalies at the level of features and/or target (noise 1)
2. Features that don’t help in explaining the target (Noise 2: irrelevant/weak features)
3. Records which don’t follow the form or relation which the rest of records do (Noise 3: noisy records)

# Outliers :

Extreme values can be present in both dependent & independent variables, in the case of supervised learning methods.

## box-plots
I would highly recommend you build scatter plots & box-plots of variables. 

The box plot uses inter-quartile range to detect outliers. Here, we first determine the quartiles Q1 and Q3.

Interquartile range is given by, IQR = Q3 — Q1

Upper limit = Q3+1.5*IQR

Lower limit = Q1–1.5*IQR

Anything below the lower limit and above the upper limit is considered an outlier


## Cook’s Distance
This is a multivariate approach for finding influential points. These points may or may not be outliers as explained above, but they have the power to influence the regression model. 
This method is used only for linear regression and therefore has a limited application. 
Cook’s distance measures the effect of deleting a given observation. 
It’s represents the sum of all the changes in the regression model when observation “i” is removed from it.

Di = 

A rule of thumb is that D(i) > 4/n, can be good cut off for influential points

see also : Another similar approach is DFFITS

## Z-Score
This method assumes that the variable has a Gaussian distribution. It represents the number of standard deviations an observation is away from the mean:

outliers = +/-3sd

All the above methods are good for initial analysis of data, but they don’t have much value in multivariate settings or with high dimensional data. For such datasets, we have to use advanced methods like :
- PCA, 
- LOF (Local Outlier Factor) 
- HiCS: High Contrast Subspaces for Density-Based Outlier Ranking.


* droping obs or not ?

Other Data-Based Methods
- Winsorizing: This method involves setting the extreme values of an attribute to some specified value. For example, for a 90% Winsorization, the bottom 5% of values are set equal to the minimum value in the 5th percentile, while the upper 5% of values are set equal to the maximum value in the 95th percentile. This is more advanced than trimming where we just exclude the extreme values.
- Log-Scale Transformation: This method is often used to reduce the variability of data including outlying observation. Here, the y value is changed to log(y). It’s often preferred when the response variable follows exponential distribution or is right-skewed

use another model that is resilient to outliers 

-----
! Novelties: Many times we’re dealing with novelties, and the problem is often called supervised anomaly detection


### Why not remove outliers
Outliers often tell you something different than central values. For example, in the distribution of human height, outliers generally result from specific genetic conditions. Some researchers are concerned primarily with these types of conditions, others with the more usual factors that determine heights of 99.7% of adult humans.

In this case it makes sense to study outliers and central values separately, but there’s no reason to assume one is more important than the other. In many cases outliers are more consequential in aggregate than central values, despite being rare.

It’s usually important to keep in mind that many outliers will be censored from your data set, or misrepresented. In measuring adult human height, for example, you have to think about how to treat people with amputated legs. It probably makes sense to exclude them from general height studies—or to adjust measurements to account for amputation.

Outliers frequently represent data errors, such as misplaced decimal points or misrecorded units. But legitimate outliers are often suppressed on the assumption they are data errors, or because they don’t fit in data collection boxes.

My father worked in graduate school for a guy who collected cosmic ray data on mountaintop automated recorders. In 1940s technology, these collector plates could get dirty and produce extreme high values. When this happened, you had to drive up the mountain, take the box taken apart and clean the plate. My Dad’s boss did this one day, but the high readings persisted. So he did it again. He reassembled the box for the second time and caught the tail end of the cosmic ray event of the century. Remember that before you discard outliers.

But there is another scenario in which outliers result from the same process as central values. These can be tricky to deal with but sometimes produce the deepest insights.

/ans
There are several reasons why you would not delete outliers. it depends on the size, shape, and structure of your data set, as well as what you want to do with the data and what models you might use to analyze it.

* First why would you ever delete any data anyways? 
- because it helps you model the data better and predict future data better. If this is true then it is fast and easy to just delete outliers that don't help you predict. 
- But what if you could just change parts of the outliers and you get better prediction? This can be the case, so if you have time, transforming the outliers can be better than deletion because while parts of the outlier observations hurt prediction other parts may help.

* Second, you may have a lot of data and deleting a few pesky outliers doesn't effect the model either way but it looks better when graphed. This seems unethical but if you don't want to draw attention to outliers then maybe you should not model them.

* Third you may have a very small data set and the model you choose is greatly affected by the outliers. In this case you must be careful because the outcome is significantly different if outliers are included. And if you have no good reason to see those values as not truly belonging in the data set then deleting them would bias your results significantly. You may think the values are outliers but in reality they represent an under sampled part of the data and so if you throw them out your model only represents part of the real data and can not predict a significant portion of reality.

Throwing away data is the same as only modeling part of the data! In general the more data you have the better your model.

In the end it depends. It is generally a good idea to find a model that can incorporate outliers. However depending on the reason for the analysis deleting or better yet transforming the outliers could be a better strategy.

If the outliers don't reflect reality because they are mistakes then delete them. But the real world is filled with outliers, so if you want to model the real world you can't delete the parts of it you think don't belong.

Whenever you find an outlier stop to think and analyze it. Justify your decision to drop/impute/keep it.

ref : 
- https://medium.com/analytics-vidhya/dealing-with-noisy-data-in-data-science-e177a4e32621
