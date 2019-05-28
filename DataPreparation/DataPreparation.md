

very important step in the data science journey 
ensures the data reliability & accuracy 

- import data
- merge data set
- rebuild missing data
- standarize data
- nomalize data 
- Deduplicate 
- Verify & enrich
- Export


* normalization : mapping the features into [-1,1]. converts all data points to decimals between 0 and 1
- min = 0 : dividing by the largest values in the sample
- min < 0 : subtract the min from each point, and then divide by the min-max difference. (x-min)/(max-min)

* standarization : when I convert to z-score (i.e. standard deviations from the mean value of the sample)

>> Transforming Skewed Data
* sigmoid function 
* log function (+1)
when numbers are too large, one can try fractional exponents 
* cube root
* log max root
* hyperbolic tangent
The hyperbolic tangent distorts the data more than the sigmoid.

* Percentile Linearization
Percentiles provide yet another option. Each data point can be ranked according to its percentile, and pandas provides a nice built-in method, .rank, for dealing with this.


-----

* pandas.get_dummies : Convert categorical variable into dummy/indicator variables

```
  s = pd.Series(list('abca'))
  pd.get_dummies(s)
     a  b  c
  0  1  0  0
  1  0  1  0
  2  0  0  1
  3  1  0  0
  ```
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.get_dummies.html

* sklearn.preprocessing.labelEncoder : Encode labels with value between 0 and n_classes-1.
  can transform numerical and non-numerical labels 
  
  ```
  from sklearn import preprocessing
  le = preprocessing.LabelEncoder()
  le.fit([1, 2, 2, 6])
  le.classes_ # array([1, 2, 6])
  >>> le.transform([1, 1, 2, 6]) 
  array([0, 0, 1, 2]...)
  >>> le.inverse_transform([0, 0, 1, 2])
  array([1, 1, 2, 6])
  ```
  
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelEncoder.html

* sklearn.preprocessing.labelBinarizer : Binarize labels in a one-vs-all fashion
  ```
  lb = preprocessing.LabelBinarizer()
  lb.fit([1, 2, 6, 4, 2])
  lb.classes_ 
  # array([1, 2, 4, 6])
  lb.transform([1, 6])  
  # array([[1, 0, 0, 0], [0, 0, 0, 1]])
  
  lb = preprocessing.LabelBinarizer()
  lb.fit_transform(['yes', 'no', 'no', 'yes'])
  array([[1], [0], [0], [1]])
  ```
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelBinarizer.html

* sklearn.preprocessing.oneHotEncoder : Encode categorical integer features as a one-hot numeric array.
  
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html

* a python map


* sklearn.preprocessing import StandardScaler

data encoding / data embedding : 
bert/gensim/glove/tfidf
