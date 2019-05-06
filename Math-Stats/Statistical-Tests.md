

## Hypothesis Testing
H0 : null hypothesis
H1 : alternative hypothesis (suspect)

### P-value and significance 
significance level : alpha = 0.05
population (mean) > sample (mean)
if we assume that H0 is true, what is the probability of getting a sample with the stats that we get
if that proba is lower than our significance level, then we say we reject the H0 and we have an evidence for the alternative

ex: take sample (n, mean, sd)
calculate : p(mean >= val|H0 true)
p-val < alpha => reject H0
p-val > alpha => do not reject H0


## Parametric Tests:

* (independent-samples) t-tests
* (paired-samples) t-test
* (One-way) Anova

Assumptions:
- random independent samples
- interval or ratio level measuremnet 
- normally distributed
- no outliers
- homogeneity of variance
- sample sizes larger than minimum for many nonparam tests

more powerful compared to non-param tests - more likely to detect a difference that truly exists
less likely than nonparam tests to make type II error


## Non-Parametric Tests : 

* Mann-whitney test
* Wilcoxon signed-rank test
* Kruskal-Wallis Test

### Assumptions
- random indep samples
- mann-whitney test : two samples that have the same shape
- wilcoxon signer-rank test : symmetric distribution
- Kruskal-Wallis and Friedman's Anova : same shape and equal variance 

- more conservative
- less statistical power 
- more likely to produce a type II erro

|param test| non param|
|---|---|
|independent samples t test|mann whitney test|
|paired samples t test|wilcoxon |
|one-way ANOVA|kruskal|
|one-way Repeated measures ANOVA|friedman's|



##

|	|Random sampling|	Not random sampling|
|---|---|---|
|Random assignment|	Can determine causal relationship in population. This design is relatively rare in the real world.	|Can determine causal relationship in that sample only. This design is where most experiments would fit.|
|No random assignment	|Can detect relationships in population, but cannot determine causality. This design is where many surveys and observational studies would fit.	|Can detect relationships in that sample only, but cannot determine causality. This design is where many unscientific surveys and polls would fit.
