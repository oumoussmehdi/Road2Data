

# ANOVA: Analysis of Variance 

the Analysis of Variance, shortly known as ANOVA is an extremely important tool for analysis of data. It is a technique employed by the researcher to make a comparison between more than two populations and help in performing simultaneous tests. There is a two-fold purpose of ANOVA :
* one-way ANOVA : we only take one factor.
* two-way ANOVA : investigates two factors concurrently. 

## one-way ANOVA:
One way ANOVA is based on the following assumptions:
- Normal distribution of the population from which the samples are drawn.
- Measurement of the dependent variable is at interval or ratio level.
- Two or more than two categorical independent groups in an independent variable.
- Independence of samples
- Homogeneity of the variance of the population.

## two-way ANOVA:
Normal distribution of the population from which the samples are drawn.
Measurement of dependent variable at continuous level.
Two or more than two categorical independent groups in two factors.
Categorical independent groups should have the same size.
Independence of observations
Homogeneity of the variance of the population.

Key Differences Between One-Way and Two-Way ANOVA
The differences between one- way and two-way ANOVA can be drawn clearly on the following grounds:

|||
|---|---|
|||
|||
|||
|||
|||
A hypothesis test that enables us to test the equality of three or more means simultaneously using variance is called One way ANOVA. A statistical technique in which the interrelationship between factors, influencing variable can be studied for effective decision making, is called Two-way ANOVA.
There is only one factor or independent variable in one way ANOVA whereas in the case of two-way ANOVA there are two independent variables.
One-way ANOVA compares three or more levels (conditions) of one factor. On the other hand, two-way ANOVA compares the effect of multiple levels of two factors.
In one-way ANOVA, the number of observations need not be same in each group whereas it should be same in the case of two-way ANOVA.
One-way ANOVA need to satisfy only two principles of design of experiments, i.e. replication and randomization. As opposed to Two-way ANOVA, which meets all three principles of design of experiments which are replication, randomization, and local control.


SST: total sum of squares
ground mean = mean of the means of each group

m*n members
m*n-1 degree of freedom

sst/degree-freedom = variance of the total group 

ssw : total sum of squares within
ssw = 
df = m*(n-1)

ssb :  total sum of squares between 
how much of the total var is due to the variation between the means from each sample and the ground mean
df = m-1

degree of freedom: if you know the mean you can figure out the nth element (n-1)


# Hypothesis test with F-statistic

H0 : no difference (means all equals)

H1 : 

alpha = .10 (significance level)
F-stat = [ssb/(m-1)]/[ssw/(m*(n-1))]
is a ratio of 2 chi distributions

REF:
https://keydifferences.com/difference-between-one-way-and-two-way-anova.html
