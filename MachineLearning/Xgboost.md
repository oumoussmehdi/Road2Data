


XGBoost (eXtreme Gradient Boosting) is an advanced implementation of gradient boosting algorithm
also known as ‘regularized boosting‘ technique.

many advantages
1. regularization
2. parallel processing
3. high flexibility
allow users to define custom optimization objectives and evaluation criteria.
4. handling missing values
5. tree pruning
6. built-in Cross-Validation
7. continue on existing model


Xgboost params : 
I. General Parameters

* booster [default=gbtree]
Select the type of model to run at each iteration. It has 2 options:
gbtree: tree-based models
gblinear: linear models

* silent [default=0]

* nthread [default to maximum number of threads available if not set]
This is used for parallel processing and number of cores in the system should be entered

II. Booster Parameters

* eta [default=0.3] : learning rate (0.01-0.2)

* min_child_weight [default=1]
the minimum sum of weights of all observations required in a child.

* max_depth [default=6]
The maximum depth of a tree, 3-10

* max_leaf_nodes
The maximum number of terminal nodes or leaves in a tree.

* gamma [default=0]
A node is split only when the resulting split gives a positive reduction in the loss function. 
Gamma specifies the minimum loss reduction required to make a split.

* max_delta_step [default=0]
In maximum delta step we allow each tree’s weight estimation to be. If the value is set to 0, it means there is no constraint. If it is set to a positive value, it can help making the update step more conservative.
Usually this parameter is not needed, but it might help in logistic regression when class is extremely imbalanced.
This is generally not used but you can explore further if you wish.
* subsample [default=1]
Same as the subsample of GBM. Denotes the fraction of observations to be randomly samples for each tree.
Lower values make the algorithm more conservative and prevents overfitting but too small values might lead to under-fitting.
Typical values: 0.5-1
* colsample_bytree [default=1]
Similar to max_features in GBM. Denotes the fraction of columns to be randomly samples for each tree.
Typical values: 0.5-1
* colsample_bylevel [default=1]
Denotes the subsample ratio of columns for each split, in each level.
I don’t use this often because subsample and colsample_bytree will do the job for you. but you can explore further if you feel so.
* lambda [default=1]
L2 regularization term on weights (analogous to Ridge regression)
This used to handle the regularization part of XGBoost. Though many data scientists don’t use it often, it should be explored to reduce overfitting.

* alpha [default=0]
L1 regularization term on weight (analogous to Lasso regression)
Can be used in case of very high dimensionality so that the algorithm runs faster when implemented

* scale_pos_weight [default=1]
A value greater than 0 should be used in case of high class imbalance as it helps in faster convergence.
 
 
III. Learning Task Parameters

* objective [default=reg:linear]
* eval_metric [ default according to objective ]
* seed [default=0]

Ref:
* https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/
* https://towardsdatascience.com/understanding-gradient-boosting-machines-9be756fe76ab
* https://towardsdatascience.com/xgboost-mathematics-explained-58262530904a
