

* Random variable: A variable that can take different values of the sample space randomly.

* Probability distribution is a description of how likely the random variable is to take on different values of the sample space.

* the probability distribution may be discrete or may be continuous
- In a discrete distribution, the probability distribution is provided by a probability mass function (pmf) denoted by P(X=x)
- Continuous distributions: These are defined for continuous random variables.In continuous distribution, we describe the distribution using probability density functions(pdf) denoted by p(x).
Their integral is equal to 1.

- joint probability : What is the probability of two events occurring simultaneously .denoted by P(Y=y,X=x) or p(y and x).

- conditional probability : What is the probability of some event y happening, given that other event x had happened .denoted by P(Y = y | X =x).

P(Y=y | X=x) = P(y,x) / P(x)


- marginal probability : what is the probability of a subset of random variables from a superset of them 
P(X=x) = Sum(P(X=x,Y=y)y

* Bayes’ theorem: It describes the probability of an event based on prior knowledge of other events related to that event.
P(Y/X) = P(X/Y).P(Y) / P(X)

Bayes theorem exploits the concept of belief in probability. “I am 40% sure that this event will happen” is not the same as “The dice has 16% chance of showing 6”.The former utilizes belief and is called as bayesian probability while the latter depends on previous data and is called as frequentist probability

## probability distribution

### Binomial distribution: coin toss
A binomial random variable is the number of successes in n trials of a random experiment. A random variable x is said to follow binomial distribution when, the random variable can have only two outcomes(success and failure).Naturally , binomial distribution is for discrete random variables. 

Ex: draw a ball and note whether it is black, then put it back. Repeat. How many times did you draw a black ball? This count also follows a binomial distribution.

###  hypergeometric distribution
This is the distribution of that same count if the balls were drawn without replacement instead.

### Uniform Distribution: die toss
Every element of the sample space is equally likely

### Poisson distribution
Like the binomial distribution, the Poisson distribution is the distribution of a count — the count of times something happened. It’s parameterized not by a probability p and number of trials n but by an average rate λ, which in this analogy is simply the constant value of np. The Poisson distribution is what you must think of when trying to count events over a time given the continuous rate of events occurring.
When things like packets arrive at routers, or customers arrive at a store, or things wait in some kind of queue, think “Poisson.”

### geometric distribution
From simple Bernoulli trials arises another distribution. How many times does a flipped coin come up tails before it first comes up heads? This count of tails follows a geometric distribution
If the binomial distribution is “How many successes?” then the geometric distribution is “How many failures until a success?”

###  negative binomial distribution 
The negative binomial distribution is a simple generalization. It’s the number of failures until r successes have occurred, not just 1. It’s therefore parameterized also by r. Sometimes it’s described as the number of successes until r failures. 

### Exponential 

### Weibull

### Normal/Gaussian distribution: “Order from Chaos” 
In the absence of prior knowledge about what form a distribution over the real numbers should take, the normal distribution is a good choice because, 
it has high entropy and central limit theorem suggests that sum of several independent random variables is normally distributed. 

> if the mean is 0 and the standard deviation is 1, then it is called as standard normal distribution.

### Log-Normal
### Student’s t
### Chi-squared

### Softmax distribution
It is a probability distribution kinda.It is best used to represent 1 of N class categorical distribution. It is also the most commonly used distributions in deep learning.It is very convenient to differentiate.

ref : 
- https://towardsdatascience.com/probability-and-statistics-explained-in-the-context-of-deep-learning-ed1509b2eb3f
- https://medium.com/@srowen/common-probability-distributions-347e6b945ce4
