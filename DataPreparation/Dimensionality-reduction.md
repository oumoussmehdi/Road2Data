

## LDA : Linear Discriminant Analysis

supervised learning - dimensionality reduction technique 
**Goal:** 
reduce the dimensions by removing the redundant and dependent freatures 
by transforming the features from a higher dimensional space to a lower one
project the features in higher dim space onto a lower dim space

**How** 
3 steps: 
1. calculate the separability between different classes (i.e distance between means of diff classes)
> between-class variance 

Sb =

2. calculate the distance between the mean and sample of each class 
> within class variance

Sw =

3. to construct the lower dimensional space which maximizes the Sb and minimizes Sw
> Fisher's criterion:

Plda

**Extension:**
QDA: quadratic da
FDA: flexible da
RDA: regularized da


ref: 
- https://medium.com/@srishtisawla/linear-discriminant-analysis-d38decf48105





https://www.analyticsvidhya.com/blog/2018/08/dimensionality-reduction-techniques-python/
