# Machine Learning and Applications

## Unit 6: Trends in Machine Learning

### Ensemble Learning

- Combinations of models are known as model ensembles.
- They are among the most powerful techniques in machine learning, and they often outperform other methods.
- However, this comes at the cost of increased algorithmic complexity and model complexity.
- In essence, ensemble learning methods:
  - construct multiple, diverse models from adapted versions of the training data (most often resampled or reweighted).
  - combine the predictions of these models in some way (often by averaging or voting).
- Some common ensemble learning methods are bagging, boosting and stacking.

### Bagging

- Bagging, short for 'bootstrap aggregating' is a simple, but highly effective ensemble learning method that creates diverse models on different random samples of the original dataset.
- These samples are taken uniformly with replacement, and are called bootstrap samples.
- Differences between the bootstrap samples will create diversity among the models in the ensemble.
- Bagging algorithm (Peter Flach)
- We can choose to combine the predictions from the different models by voting (the class predicted by the majority of models wins) or averaging, which is more appropriate is the model outputs real numbers like probabilities.

### Boosting

- Boosting is an ensemble learning technique that is superficially similar to bagging, but uses a more sophisticated technique than bootstrap sampling to create diverse training sets. It essentially converts weak models into strong ones.
- Suppose we train a linear classifier on a dataset and find that its training error is $\epsilon$. The goal is to add another classifier to the ensemble that does better on the misclassifications of the first instance.
- Boosting does this by assigning a higher weight to the misclassified instances, and modifies the classifier to take these weights into account.
- If the error rate of a model (or ensemble of models) is $\epsilon$, the current weights of the misclassified instances are multiplied by $1/2\epsilon$, and the current weights of the correctly classified instances are multiplied by $1/2(1-\epsilon)$.
- A confidence factor $\alpha$ is also assigned to each model. It is calculated as: $\alpha_t = \frac{1}{2}ln\frac{1-\epsilon_t}{\epsilon_t}$.
- Boosting algorithm (Peter Flach). Or maybe AdaBoost?

### Deep Learning
*Refer to Fundamentals of Deep Learning - Nikhil Buduma. A free sample that covers the required syllabus topics is available at the O'Reilly website.*

- Deep learning refers to a subset of machine learning algorithms called deep neural networks which almost always outperform almost every other machine learning model, when given large amounts of training data and computational power.
- A neural network is a machine learning model that loosely models the working of the human brain. It is made up of artificial neurons. Each neuron is a basic computational unit that takes in a number of inputs. The neuron calculates a weighted sum of them and passes it through an activation function (which is generally non-linear). The output of a neuron is a real number.
- Diagram of an artifical neuron + formulae for weighted sum, activation
- In a neural network, neurons are arranged in layers. The first layer is called the input layer, the last layer is caleld the output layer, and any layers in between them are called hidden layers.
- A deep neural network is one that has two or more hidden layers.
- Diagram of a deep neural network.

### The Neuron

- The fundamental unit of the human brain is the neuron. At its core, it is optimized to receive information from other neurons, process this information and send its result to other neurons.
- Diagram of a biological neuron.
- A neuron receives its inputs from dendrites, processes the inputs in the cell body, and transmits the output through the axon to other neurons.
- Biological neurons can be modelled artifically.
- An artifical neuron is a basic computational unit that takes in a number of inputs. The neuron calculates a weighted sum of them and passes it through an activation function (which is generally non-linear). The output of a neuron is a real number. The output of a neuron is sent to other neurons.
- Diagram of an artifical neuron + formulae for weighted sum, activation.