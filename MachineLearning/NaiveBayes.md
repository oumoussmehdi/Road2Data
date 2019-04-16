Naive Bayes

https://www.youtube.com/watch?v=XcwH9JGfZOU

Advantage:
simple, you’re just doing a bunch of counts.
good bet if want something fast and easy that performs pretty well.
 
Disadvantage:
 
Very simple representation doesn't allow for rich hypotheses
Assumption of independence of attributes is too constraining (although, see Domingos' paper on why it's not so bad)
Determining the topology of dependence is difficult
it can’t learn interactions between features (e.g., it can’t learn that although you love movies with Brad Pitt and Tom Cruise, you hate movies where they’re together).
 
Bayes networks/Graphical models
 
If the NB conditional independence assumption actually holds, a Naive Bayes classifier will converge quicker than discriminative models like logistic regression, so you need less training data.
if the NB assumption doesn’t hold, a NB classifier still often does a great job in practice.
