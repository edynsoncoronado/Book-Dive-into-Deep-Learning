# The Key Components:
No matter what kind of ML problem we take on:
1. The data that we can learn from.
1. A model of how to transform the data.
1. A loss function that quantifies the badness of our model.
1. An algorithm to adjust the modelʼs parameters to minimize the loss.

## Data:
- It might go without saying that you cannot do data science without data.
- In the supervised learning problems above, a special feature is designated as the prediction target, **(sometimes called the label or dependent variable).**
- The given features from which the model must make its predictions can then simply be called the features, **(or often, the inputs, covariates, or independent variables).**
- It is not enough to have lots of data and to process it cleverly. **We need the right data.**
	- If the data is full of mistakes, or if the chosen features are not predictive of the target quantity of interest, learning is going to fail.
- Poor predictive performance is not the only potential consequence.
	- One common failure mode occurs in datasets where some groups of people are unrepresented in the training data.
	- Imagine applying a skin cancer recognition system in the wild that had never seen black skin before.
- For example, if past hiring decisions are used to train a predictive model that will be used to screen resumes, then machine learning models could inadvertently capture and automate historical injustices.


## Models:
- Most machine learning involves transforming the data in some sense.
	- We might want to build a system that ingests photos and predicts smiley-ness.
- These models consist of many successive transformations of the data that are chained together top to bottom, thus the name deep learning.

## Objective functions:
- **Learning from experience**
	- By learning here, we mean improving at some task over time.
- But **who is to say what constitutes an improvement?**
	- In order to develop a formal mathematical system of learning machines, we need to have formal measures of how good (or bad) our models are.
	- In machine learning, and optimization more generally, we call these objective functions.
	- **We usually define objective functions so that lower is better.**
		- You can take any function **f** for which higher is better, and turn it into a new function **f'** that is qualitatively identical but for which lower is better by setting f' = -f.
		- Because lower is better, these functions are sometimes called loss functions or cost functions.
- The most common objective function is squared error (y−ŷ)^2.
	- For classification, the most common objective is to minimize error rate.
- We will typically want to split the available data into two partitions: **the training data** (for fitting model parameters) and **the test data** (which is held out for evaluation).
	- **Training Error:** The error on that data on which the model was trained.
		- You could think of this as being like a student's scores on practice exams used to prepare for some real exam.
	- **Test Error:** This is the error incurred on an unseen test set. This can deviate significantly from the training error.
		- When a model performs well on the training data but fails to generalize to unseen data, we say that it is **overfitting**.

## Optimization algorithms
- Once we have got some data source and representation, a model, and a well-defined objective function, we need an algorithm capable of searching for the best possible parameters for minimizing the loss function.
- The most popular optimization algorithms for neural networks follow an approach called **gradient descent**.
	- In short, at each step, they check to see, for each parameter, which way the training set loss would move if you perturbed that parameter just a small amount.
	- They then update the parameter in the direction that reduces the loss.