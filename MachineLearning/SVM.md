Support Vector Machines SVM
Séparateur à vaste marge
méthode à noyau
https://www.math.univ-toulouse.fr/~besse/Wikistat/pdf/st-m-app-svm.pdf
https://en.wikipedia.org/wiki/Support_vector_machine
https://www.lri.fr/~antoine/Courses/Master-ISI/ISI-10/Tr-cours-SVM_2014_2x2.pdf
 
SVM sont un ensemble de techniques d'apprentissage supervisé destinées à résoudre des problèmes de discrimination et de régression. 
Les SVM sont une généralisation des classifieurs linéaires.
travailler avec des données de grandes dimensions, le faible nombre d'hyperparamètres, leurs garanties théoriques, et leurs bons résultats en pratique.
non-probabilistic binary linear classifier.
 
Les séparateurs à vastes marges sont des classificateurs qui reposent sur deux idées clés, qui permettent de traiter des problèmes de discrimination non linéaire, et de reformuler le problème de classement comme un problème d'optimisation quadratique.
La première idée clé est la notion de marge maximale. La marge est la distance entre la frontière de séparation et les échantillons les plus proches. Ces derniers sont appelés vecteurs supports. Dans les SVM, la frontière de séparation est choisie comme celle qui maximise la marge. Ce choix est justifié par la théorie de Vapnik-Chervonenkis (ou théorie statistique de l'apprentissage), qui montre que la frontière de séparation de marge maximale possède la plus petite capacité[10]. Le problème est de trouver cette frontière séparatrice optimale, à partir d'un ensemble d'apprentissage. Ceci est fait en formulant le problème comme un problème d'optimisation quadratique, pour lequel il existe des algorithmes connus.

Afin de pouvoir traiter des cas où les données ne sont pas linéairement séparables, la deuxième idée clé des SVM est de transformer l'espace de représentation des données d'entrées en un espace de plus grande dimension (possiblement de dimension infinie), dans lequel il est probable qu'il existe une séparation linéaire. Ceci est réalisé grâce à une fonction noyau, qui doit respecter les conditions du théorème de Mercer, et qui a l'avantage de ne pas nécessiter la connaissance explicite de la transformation à appliquer pour le changement d'espace. Les fonctions noyau permettent de transformer un produit scalaire dans un espace de grande dimension, ce qui est coûteux, en une simple évaluation ponctuelle d'une fonction. Cette technique est connue sous le nom de kernel trick.

An SVM model is a representation of the examples as points in space, mapped so that the examples of the separate categories are divided by a clear gap that is as wide as possible. 

New examples are then mapped into that same space and predicted to belong to a category based on which side of the gap they fall.
 
SVMs can efficiently perform a non-linear classification using what is called the kernel trick, implicitly mapping their inputs into high-dimensional feature spaces.
 
(clustering : support vector clustering)
## Advantages:
- High accuracy
- Theoretical guarantees regarding overfitting
- with an appropriate kernel they can work well even if your data isn’t linearly separable in the base feature space.
- Popular in text classification problems where very high-dimensional spaces are the norm.
 
## Disadvantages:
- Picking/finding the right kernel can be a challenge
- Results/output are incomprehensible
- Memory-intensive, hard to interpret, and kind of annoying to run and tune
- No standardized way for dealing with multiclass problems; fundamentally a binary classifier
- can be painfully inefficient to train. not recommend when having many training examples)
 
 
SVM with a linear kernel is not very different from a Logistic Regression
use a different loss function (Hinge) from LR.
They are also interpreted differently (maximum-margin).
 
The main reason you would want to use an SVM instead of a Logistic Regression :
your problem might not be linearly separable. In that case, you will have to use an SVM with a non linear kernel (e.g. RBF).
you are in a highly dimensional space
