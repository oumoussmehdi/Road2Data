
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
