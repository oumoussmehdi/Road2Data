
# Decision trees
(divide-and-conquer algorithms)

http://www.saedsayad.com/decision_tree.htm

Un arbre de décision est un outil d'aide à la décision représentant un ensemble de choix sous la forme graphique d'un arbre. Les différentes décisions possibles sont situées aux extrémités des branches (les « feuilles » de l'arbre), et sont atteints en fonction de décisions prises à chaque étape. 

Il a l'avantage d'être lisible et rapide à exécuter. Il s'agit de plus d'une représentation calculable automatiquement par des algorithmes d'apprentissage supervisé.

### Advantages:
- Easy to interpret and explain
- They easily handle feature interactions and they’re non-parametric, so you don’t have to worry about outliers or whether the data is linearly separable
 
### Disadvantage:
- easily overfit,
- May get stuck in local minima so need ensembles to help reduce the variance
- don’t support online learning (you have to rebuild your tree when new examples come on. Another disadvantage is that they
 
### Algo:
The core algorithm for building decision trees called ID3:
employs a top-down, greedy search through the space of possible branches with no backtracking.
ID3 uses Entropy and Information Gain to construct a decision tree.
 
### Entropy
A decision tree is built top-down from a root node and involves partitioning the data into subsets that contain instances with similar values (homogenous).
ID3 algorithm uses entropy to calculate the homogeneity of a sample.
* If the sample is completely homogeneous: entropy = 0
* If the sample is an equally divided : entropy = 1.
 
To build a decision tree, we need to calculate two types of entropy using frequency tables
- Entropy using the frequency table of one attribute
- Entropy using the frequency table of two attribute
 
 
### Information Gain

The information gain is based on the decrease in entropy after a dataset is split on an attribute. Constructing a decision tree is all about finding attribute that returns the highest information gain (i.e., the most homogeneous branches).
 
 
https://www.kaggle.com/dansbecker/underfitting-and-overfitting

