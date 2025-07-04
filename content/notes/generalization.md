---
type: "page"
title: "Generalization in Deep Learning"
date: 2022-12-05
---
<!-- change date before commiting --> 

*These are the notes from **Roger Grosse's lecture on generalization in deep learning**.*

- In our ML models we don't want them to learn to model the training data, but rather to *generalize* to the data it hasn't senn before.

- The way to measure this *Generalization performance* thorugh a held-out test set, that has unseen data/examples.
- Overfitting: If the algorithm works well on the training set but fails to generalize on the test set, we say that it has overfitted to the training data.

- Some strategies to improve generalization and reducing overfitting : 
    1. Reducing the capacity of the model
    2. Early Stopping
    3. Regularization and Weight Decay
    4. Ensemble Methods
    5. Input Transformations / Data Augmentation
    6. Stochastic Regularization

### Measuring Generalization: 

- Cost Function : The average loss over the entire training set
$$
\frac{1}{N} \sum_{i=1}^{N} \mathcal{L}(y(x^{(i)}), t^{(i)})
$$

- We partition our data into three subsets to measure network's generalization (and there are other reasons as well):
    - A **Training Set**, a set of training examples the network is trained on.
    - A **Validation Set**, which is used to tune *hyperparameters* such as number of hidden units, or the learning rate.
    - A **Test Set**, which is used to measure the **generalization performance**

*There are various ways to perform this partitioning, one of which is cross-validation. I will write separate notes on that.*

- We can't tune hyperparameters on the training set, because we want to choose values that will generalize.
- We can't also tune hyperparameters on the test set, because that would be "cheating", and we are only allowed to use the test set once, to report the final perfomance.

#### The most basic strategy for tuning hyperparameters is :
1. **Grid Search**: In grid search, for each hyperparameter, choose a set of candidate values. Separately train the models using all possible combinations of these values, and choose whiever confifuration gives the best validation erorr (minimum validation error).

2. **Random Search**: In random search, we train a bunch of networks uisng random configurations of the hyperparameters, and pick whichever one has the best validation error (minimum) 

*Random search* is advantageous over *grid search* when only a few of many hyperparameters (e.g., 2 out of 10) are important. While *grid search* becomes infeasible in high dimensions, *random search* can still effectively explore the space of the important hyperparameters. However, *grid search* is easier to reproduce, which is beneficial in scientific settings.


### Reasoning about generalization

- One reason for overfitting is that the training set contains accidental irregularities. For example, in the case of classifying handwritten digits, all training examples of the digit '9' might have pixel 122 turned on, while all others have it off. The network may mistakenly learn this as a useful feature.

- **Capacity** of a model is the ability to remember information about its training data. It is roughly the number of parameters (i.e., weights) 

1. **Effect of Training Set Size:** More training data improves generalization because it's more likely that test examples resemble training examples. It also reduces the impact of accidental regularities, forcing the model to learn true patterns. If test error increases with more data, it likely indicates a bug or model issue. However, training error typically increases with more data, as larger datasets are harder to memorize.

    - Training vs. Generalization Error: As training set size increases, training error goes up and generalization error (or test error) goes down, eventually converging.

2. **Effect of Model Capacity (Number of Parameters):** Increasing parameters reduces training error by helping the model fit both true and accidental patterns. But generalization error behaves non-monotonically—decreasing at first (as the model learns real patterns), then increasing (as the model starts memorizing noise).

    - Ideal Model Capacity: The goal is to build models with just enough capacity to learn meaningful regularities in the data without memorizing or overfitting to accidental ones.

![Qualitative relationship b/w 1. number of training examples and training and test eror. 2. the number of parameters (model capacity) and training and test error](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fanalyticsindiamag.com%2Fwp-content%2Fuploads%2F2021%2F10%2Fgraph.png&f=1&nofb=1&ipt=15fd8430dcf06a18bbeab59e59c3d0b971880c0ecce6f222a5f139dd01355c48&ipo=images)

### Bais and Variance
...

### Improving Generalization and Reducing Overfitting
...
#### 1. Reducing Capacity
...

#### 2. Early Stopping
....

#### 3. Regularization and Weight Decay
...
#### 4. Ensemble Methods
....

#### 5. Input Transformations / Data Augmentation
....

#### 6. Stochastic Regularization
....







