
Most traditional learning algorithms are developed for single-label classification problems. 
Therefore a lot of approaches in the literature transform the multi-label problem into multiple single-label problems, 
so that the existing single-label algorithms can be used.

1. OneVsRest
Traditional two-class and multi-class problems can both be cast into multi-label ones by restricting each instance to have only one label.
On the other hand, the generality of multi-label problems inevitably makes it more difficult to learn.
An intuitive approach to solving multi-label problem is to decompose it into multiple independent binary classification problems (one per category).

* The main assumption here is that the labels are mutually exclusive. You do not consider any underlying correlation between the classes in this method.

2. Binary Relevance
In this case an ensemble of single-label binary classifiers is trained, one for each class. 
Each classifier predicts either the membership or the non-membership of one class. 
The union of all classes that were predicted is taken as the multi-label output. 
This approach is popular because it is easy to implement, **however it also ignores the possible correlations between class labels**.
In other words, if there’s q labels, the binary relevance method create q new data sets from the images, one for each label and train single-label classifiers on each new data set. 
One classifier may answer yes/no to the question “does it contain trees?”, thus the “binary” in “binary relevance”. 
This is a simple approach but does not work well when there’s dependencies between the labels.
OneVsRest & Binary Relevance seem very much alike. If multiple classifiers in OneVsRest answer “yes” then you are back to the binary relevance scenario.

3. Classifier Chains
A chain of binary classifiers C0, C1, . . . , Cn is constructed, where a classifier Ci uses the predictions of all the classifier Cj , 
where j < i. This way the method, also called classifier chains (CC), can take into account label correlations.
The total number of classifiers needed for this approach is equal to the number of classes, but the training of the classifiers is more involved.

4. Label Powerset
This approach does take possible correlations between class labels into account. 
This approach considers each member of the power set of labels in the training set as a single label.
This method needs worst case (2^|C|) classifiers, and has a high computational complexity.
However when the number of classes increases the number of distinct label combinations can grow exponentially. 
This easily leads to combinatorial explosion and thus computational infeasibility. 
Furthermore, some label combinations will have very few positive examples.

ex: from skmultilearn.problem_transform import LabelPowerset

5. Adapted Algorithm
Algorithm adaptation methods for multi-label classification concentrate on adapting single-label classification algorithms to the multi-label case usually by changes in cost/decision functions.
Here we use a multi-label lazy learning approach named ML-KNN which is derived from the traditional K-nearest neighbor (KNN) algorithm.
The skmultilearn.adapt module implements algorithm adaptation approaches to multi-label classification, including but not limited to ML-KNN.

ex: from skmultilearn.adapt import MLkNN

### REF : 
* https://towardsdatascience.com/journey-to-the-center-of-multi-label-classification-384c40229bff
* http://scikit.ml/tutorial.html
