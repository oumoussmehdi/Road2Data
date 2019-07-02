
Data cleaning is a very important step in your data analysis :

some times you would have many field in your data which are empty (nulls, nas) therefore you should take in consideration this when you analyse your data. for instace, when you are trying to do machine learning many algorithms doesn’t know how to deal with data that contains nulls, as a result, it is your responsability to try and figure out how you can deal with the voids in your data. this can be solve in many ways:

either you remove the records that contains the nulls, which is not usually a good idea, especially if you have few data
or a better solution would be to replace the nulls with a certain values, this could be the mean, the median, or a default value
also, as my friends above mention it, data can contain errors especially if it comes from human input (human error) so it is recommended to fix such mistakes, a simple example would be: you have a column in your data called Country, and in it you have values for instance: Morocco, Moroko, unless you correct the second value, the two would be considered different.

Another example, which comes out especially when you receive data from different sources is the next one: let’s keep our country example, however this time you found out that in some values are as follow: USA, u.s.a, united states, we can agree that these values are all correct and refer to the same entity. however unless you try to map them to a single value your analysis will consider them different.

I hope you find my answer helpful

---

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
