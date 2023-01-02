# Random Forests
## Bootstrapping
You might be wondering how the trees in the random forest get created.
After all, right now, our algorithm for creating a decision tree is deterministic — given a training set, the same tree will be made every time.
To make a random forest, we use a technique called bagging, which is short for bootstrap aggregating.
This exercise will explain bootstrapping, which is a type of sampling method done with replacement.

How it works is as follows: every time a decision tree is made, it is created using a different subset of the points in the training set.
For example, if our training set had 1000 rows in it, we could make a decision tree by picking 100 of those rows at random to build the tree.
This way, every tree is different, but all trees will still be created from a portion of the training data.

In bootstrapping, we’re doing this process with replacement. Picture putting all 100 rows in a bag and reaching in and grabbing one row at random.
After writing down what row we picked, we put that row back in our bag.
This means that when we’re picking our 100 random rows, we could pick the same row more than once.
In fact, it’s very unlikely, but all 100 randomly picked rows could all be the same row! Because we’re picking these rows with replacement, there’s no need to
shrink our bagged training set from 1000 rows to 100. We can pick 1000 rows at random, and because we can get the same row more than once, we’ll still end up
with a unique data set.

We’ve loaded a dataset about cars here.
An important field within the dataset is the safety rating denoted by safety that can be “low”, “med”, or “high.” We’re going to implement bootstrapping
and estimate the average safety rating across the different bootstrapped samples.
