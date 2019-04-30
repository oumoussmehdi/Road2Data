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
