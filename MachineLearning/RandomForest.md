

each decision tree in the forest considers a random subset of features when forming questions and only has access to a random set of the training data points. T

There are two fundamental ideas behind a random forest, both of which are well known to us in our daily life:
- Constructing a flowchart of questions and answers leading to a decision
- The wisdom of the (random and diverse) crowd

hyper-params tuning :
- n_estimators = number of trees in the foreset
- max_features = max number of features considered for splitting a node
- max_depth = max number of levels in each decision tree
- min_samples_split = min number of data points placed in a node before the node is split
- min_samples_leaf = min number of data points allowed in a leaf node
- bootstrap = method for sampling data points (with or without replacement)

Scikit-learn
- RandomizedSearchCV
- GridSearchC
