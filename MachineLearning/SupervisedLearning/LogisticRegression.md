## Logistic regression

La régression logistique ou modèle logit est un modèle de régression binomiale. Comme pour tous les modèles de régression binomiale, il s'agit de modéliser l'effet d'un vecteur de variables aléatoires ( x 1 , … , x K ) sur une variable aléatoire binomiale génériquement notée y . La régression logistique est un cas particulier du modèle linéaire généralisé. 

Use it if :
- you expect your features to be roughly linear and the problem to be linearly separable.
- you want a probabilistic framework (e.g., to easily adjust classification thresholds, to say when you’re unsure, or to get confidence intervals)
- you expect to receive more training data in the future that you want to be able to quickly incorporate into your model.
 
### Advantages :
- pretty robust to noise and you can avoid overfitting
- feature selection by using l2 or l1 regularization.
- can be distributed using, for example, ADMM (see logreg).
- output can be interpreted as a probability.
- Lots of ways to regularize your model, and you don’t have to worry as much about your features being correlated, like you do in Naive Bayes.
- nice probabilistic interpretation, and you can easily update your model to take in new data (using an online gradient descent method), unlike decision trees or SVMs,
- You can do some feature engineering to turn most non-linear features into linear pretty easily.
 
### Disadvantage:
- it can hardly handle categorical (binary) features
- Limited expressive power
- Fundamentally a binary classifier
- Hard to make incremental
