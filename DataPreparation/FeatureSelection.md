# Feature Selection

- reduce overfitting
- improves accuracy 
- reduce training time 

## Univariate Selection
the use of statistical test to select those features that have the strongest relationship with the output variable.
ex :  the use of chi-squared (chi²) statistical test for non-negative features to select 10 of the best features

```
from sklearn.feature_selection import SelectKBest

```

## Feature Importance
You can get the feature importance of each feature of your dataset by using the feature importance property of the model.

Feature importance gives you a score for each feature of your data, the higher the score more important or relevant is the feature towards your output variable.

Feature importance is an inbuilt class that comes with Tree Based Classifiers

## Correlation Matrix with Heatmap 
Correlation states how the features are related to each other or the target variable.

Correlation can be positive (increase in one value of feature increases the value of the target variable) or negative (increase in one value of feature decreases the value of the target variable)

Heatmap makes it easy to identify which features are most related to the target variable
```
import seaborn as sns
corrmat = df.corr()
top_corr_features = corrmat.index
plt.figure(figsize=(20,20))
#plot heat map
g=sns.heatmap(data[top_corr_features].corr(),annot=True,cmap="RdYlGn")
```
## RFE: Recursive Feature Elimination

the idea is to repeatedly construct a model and choose either the best or worst perfoming feature, setting the feature aside and then repeating the process with the rest of the features.
This process is applied until all features in the data set are exhausted
the goal of FRE is to select features by recursively considering smaller and amaller sets of features 

```
import statsmodels.api as sm
logit_model = sm.Logit(y,X)
result=logit_model.fit()
print(result.summary2()
### remove the feature with a p value > 0.05
```
