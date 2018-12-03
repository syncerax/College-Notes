# Machine Learning and Applications

## Units 1-3 (Introduction to Machine Learning, Classification, Regression and Generalization)

### 1. What is machine learning? *OR* Give a detailed overview of machine learning.

- Machine learning is the systematic study of algorithms and systems that improve in performance with experience. It is the field of study that enables computers to learn without being explicitly programmed.
- Machine learning is used when
    - the rules are too complex to be coded by hand
    - the system cannot scale up to handle Big Data
    - the environment is dynamic and ever changing
- Machine learning is formally defined as follows: "A machine is said to learn from experience E, with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E."
- Machine learning algorithms can be categorised into:
    - Supervised learning
    - Unsupervised learning
    - Semi-supervised learning
    - Reinforcement learning
    - Recommender systems (not sure)
- Examples of machine learning applications are:
    - Regression
    - Classification
    - Clustering
    - Finding associations

### 2. Explain different learning types.

The different types of learning are:
- **Supervised learning:** In supervised learning, the dataset is labelled. That is, for each example, we already know what the correct output looks like. The data is in the form of (X, Y) pairs, where X is a vector of features and Y is the correct output. The aim in supervised learning is to learn a mapping from the input to the output. Supervised learning is categorised into classification and regression.
- **Unsupervised learning:** In unsupervised learning, the dataset is unlabelled. That is, we do not know the correct output for the examples in the dataset. The aim here is to find regularities in the data in order to find hidden structure in it. Some examples of unsupervised learning are clustering and learning association rules.
- **Semi-supervised learning:** In semi-supervised learning, the dataset is partly labelled and partly unlabelled. One approach in semi-supervised learning is to build an initial model using the labelled training data and to use it to make predictions on the unlabelled data. Following this, the most confident predictions of the model are added to the training set, and the model is retrained on the enlarged training set.
- **Reinforcement learning:** In reinforcement learning, the output of the system is a sequence of actions. The agent (model) receives a reward (or penalty) based on its actions. The aim here is to learn the best policy for deciding which action to take in a particular situation/state so as to maximize the total reward.

### 3. What are supervised and unsupervised learning?

See 2.

### 4. What do you mean by dimensionality reduction?

- Dimensionality reduction is the process of reducing the number of random variables taken into consideration by obtaining a set of principal variables. It is divided into feature selection and feature extraction.
- Feature selection is the process of selecting selecting the most important `k` dimensions (features) out of the `d` input dimensions and discarding the remaining `(d - k)` dimensions.
- Feature extraction is the process of finding a new set of `k` dimensions, which are combinations/functions of the original `d` dimensions.
- Eg: Principal Component Analysis (feature extraction), subset selection (feature selections), Linear Discriminant Analysis (feature extraction).

### 5. Explain the subset selection method.

Subset selection is the process of finding the best subset of the set of features. The best subset contains the least number of features that contribute the most to accuracy. The remaining, less important features are discarded. For `d` input dimensions, there are `2^d` possible subsets.

### 6. What are the different ways of feature selection?

There are two approaches for selecting features: forward selection and backward selection.
- **Forward selection:** In forward selection, we start with no variables, and add them one by one, at each step adding the one that decreases the error the most, until further addition does not decrease the error (or decreases it very slightly).
- **Backward selection:** In backward selection, we start with all variables and remove them one by one, at each step removing the one that decreases the error the most (or increases it only slightly), until further removal increases the error significantly.

### 7. Explain PCA in detail.

- Principal Components Analysis (PCA) is a dimensionality reduction technique. It is an unsupervised learning algorithm, since it does not use the output information.
- It is a statistical learning procedure that uses a series of orthogonal transformations to convert a set of observations of possibly correlated variables into a set of values of linearly uncorrelated variables called principal components. For a set of `n` observations of `d` variables, the number of principal components is `min(n - 1, d)`.
- This transformation is defined in such a way that the first principal component has the highest possible variance and each of the subsequent components has the highest variance under the constraint that it is orthogonal to the preceding components.
- The PCA algorithm:
    1. Normalize the data. (Mean normalization and feature scaling).
    2. Calculate the covariance matrix. (`(d * d)` dimensional matrix)
    3. Calculate the eigenvectors and the corresponding eigenvalues for the covariance matrix. (`d` number of `d` dimensional vectors, arranged in descending order of the eigenvalues).
    4. Select the first `k` eigenvectors and discard the remaining `(d - k)` eigenvectors. These are the principal components.
    5. Project the data onto the linear subspace spanned by this set of `k` vectors.

### 8. What is feature selection? Explain how it is performed.

See 4, 5, 6.

### 9. Explain overfitting and underfitting.

- How well a model trained on a training set predicts the right output for new unseen instances is called generalization. When a model does not generalize well from the training set to unseen data, it has either underfit or overfit to the training set.
- For best generalization, the complexity of the hypothesis `h` should match the complexity of the function underlying the data.
- If `h` is less complex than the function, underfitting occurs. For example, when we try to fit a straight line to data sampled from a third degree polynomial. (Draw diagram)
- However, if `h` is overcomplex, then not only will it learn the underlying function in the data, but also the noise in it, and will hence be a bad fit. For example, trying to fit a sixth degree polynomial to data sampled from a third degree polynomial. This is called overfitting. (Draw diagram)

### 10. Define squared error and mean squared error with respect to regression.

- In regression, the differences between the actual output and the predicted output on the training examples are called residuals. These are a measure of the error of a hypothesis.
- Squared error for an example is defined as half of the square of the residual for that training example.
- Sum of squared errors is defined as the sum of squared errors over all the instances in the dataset.
- Mean squared error is defined as the average squared error over all the instances in the dataset.
- For finding the best fit to the data, we find the set of parameters that minimise either the sum of squared errors or the mean squared error.

Write alternative formulae as well. (both with and without the 1/2 term)

### 11. What is cross validation?

- We can measure the generalization ability of a hypothesis if we have access to data outside the training set. This is simulated by dividing the training set into two parts: one part for fitting the hypothesis (training set) and the other for testing the model's generalization ability (validation set).
- Given a set of hypotheses `H`, we fit all the hypotheses in `H` to the training set. Following this, the hypothesis that is the most accurate on the validation set is the best one. This process is called cross validation.

### 12. Explain output code matrix for OVO and OVA schemes for multiclass classifiers (for 3 classes).

Explained best in Peter Flach

### 13. Explain perceptron.

- A perceptron is a linear classifier that takes inputs `x0, ... , xd`, where `x0 = 1` (bias unit) and has weights associated with every input `w0, ... , wd`.
- Diagram
- In the simplest case, the perceptron calculates a weighted sum of its inputs: `y = ∑wixi = wTx`, where `w = [ (d + 1, 1) ]` and `x = [ (d + 1, 1) ]`. `w0` is the intercept term used to make the model more general and `x0` is the bias unit (which is always `1`).
- The perceptron defined above defines a hyperplane that can be used to divide the input space into two: the half space where its value is positive and the half space where its value is negative. This is done by using a nonlinear threshold function like the sign function or the sigmoid function.
- `z = wTx; y = sigmoid(z) = 1 / (1 + exp(-z))`

### 14. How is the performance of a classifier measured?

- The performance of a classifier is measured by using a table called a contingency table or a confusion matrix. In this table, each row represents the number of instances of an actual class and each column represents the number of instances of a predicted class. The last row and last column are called marginals. They are important as they allow us to assess statistical significance.
- From a contingency table, we can calculate a range of performance indicators:
    - Accuracy (+ formula)
    - Error rate (+ formula)
    - Precision (+ formula)
    - True positive rate (Recall) (+ formula)
    - True negative rate (+ formula)
    - False positive rate (+ formula)
    - False negative rate (+ formula)

### 15. Prove that Precision = TP / (TP + FP)

- Precision is defined as the proportion of actual positives among the predicted positives.
- `∑ (I[c(x) = c_hat(x) = +ve]) / I[c_hat(x) = +ve]`
- `TP / (TP + FP)`

### 16. What is an SVM?

- Support Vector Machine (SVM) is a supervised learning algorithm that can be used for both classification and regression.
- It creates a geometric model.
- The distance from the hyperplane to the instances closest to it on either side is called the margin, which an SVM maximizes for best generalization. Hence, an SVM is also called a large-margin classifier.
- (Large-margin diagram)
- The training examples nearest to the decision boundary are called support vectors. The decision boundary of an SVM is defined as a linear combination of the support vectors.
- The optimization objective for an SVM is: (equation)

### 17. Explain kernels with respect to SVMs.

### 18. What are soft and hard margins?

### 19. Explain multivariate regression.

- In multivariate regression, the goal is to create a model that estimates a numeric (continuous valued) output `y` as the weighted sum of several input variables `x1, ... , xd`.
- It is called multivariate, since the output (dependent variable) is dependent on multiple features (independent variables).
- The multivariate regression model is: `y = h(x) + noise = w0 + w1x1 + ... + wdxd + noise`
- In order to find the best fit, we find the set of weights which minimize the sum of squared errors. (Write SSE equation)
- The optimal parameters are found as follows: (Write normal equation) and matrix format.

### 20. What is LASSO and Ridge regression?

### 21. What are the different types of regularizations?

### 22. Explain the bias-variance dilemma.
- If we underestimate the number of parameters in the model, we may not be able to reduce the training loss well, even if we have a lot of training data.
- On the other hand, a large number of parameters will mean that the model is highly dependent on the training sample, and small changes in the training data will lead to a considerably different model.
- This is called the bias-variance dilemma.
- A low complexity model does not suffer from high variance, but suffers from high bias, which even large amounts of training data cannot resolve.
- In contrast to this, a high complexity model eliminates the high bias problem but suffers from high variance.
- Draw the train/test error curves to show the high bias and high variance cases.