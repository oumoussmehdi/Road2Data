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
