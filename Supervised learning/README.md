# Supervised learning

**Supervised learning (SL)** is the [machine learning](https://en.wikipedia.org/wiki/Machine_learning) task of learning a function that [maps](https://en.wikipedia.org/wiki/Map_(mathematics)) an input to an output based on example input-output pairs.[[1]](https://en.wikipedia.org/wiki/Supervised_learning#cite_note-1) It infers a function from _labeled _[_training data_](https://en.wikipedia.org/wiki/Training_set) consisting of a set of _training examples_.[[2]](https://en.wikipedia.org/wiki/Supervised_learning#cite_note-2) In supervised learning, each example is a _pair_ consisting of an input object (typically a vector) and a desired output value (also called the _supervisory signal_). A supervised learning algorithm analyzes the training data and produces an inferred function, which can be used for mapping new examples. An optimal scenario will allow for the algorithm to correctly determine the class labels for unseen instances. This requires the learning algorithm to generalize from the training data to unseen situations in a &quot;reasonable&quot; way (see [inductive bias](https://en.wikipedia.org/wiki/Inductive_bias)). This statistical quality of an algorithm is measured through the so-called [generalization error](https://en.wikipedia.org/wiki/Generalization_error).

The parallel task in human and animal [psychology](https://en.wikipedia.org/wiki/Psychology) is often referred to as [concept learning](https://en.wikipedia.org/wiki/Concept_learning).

## **Steps to follow**

To solve a given problem of supervised learning, one has to perform the following steps:

1.Determine the type of training examples. Before doing anything else, the user should decide what kind of data is to be used as a training set. In the case of [handwriting analysis](https://en.wikipedia.org/wiki/Handwriting_analysis), for example, this might be a single handwritten character, an entire handwritten word, an entire sentence of handwriting or perhaps a full paragraph of handwriting.

2Gather a training set. The training set needs to be representative of the real-world use of the function. Thus, a set of input objects is gathered and corresponding outputs are also gathered, either from human experts or from measurements.

3.Determine the input feature representation of the learned function. The accuracy of the learned function depends strongly on how the input object is represented. Typically, the input object is transformed into a [feature vector](https://en.wikipedia.org/wiki/Feature_vector), which contains a number of features that are descriptive of the object. The number of features should not be too large, because of the [curse of dimensionality](https://en.wikipedia.org/wiki/Curse_of_dimensionality); but should contain enough information to accurately predict the output.

4.Determine the structure of the learned function and corresponding learning algorithm. For example, the engineer may choose to use [support-vector machines](https://en.wikipedia.org/wiki/Support-vector_machine) or [decision trees](https://en.wikipedia.org/wiki/Decision_tree_learning).

5.Complete the design. Run the learning algorithm on the gathered training set. Some supervised learning algorithms require the user to determine certain control parameters. These parameters may be adjusted by optimizing performance on a subset (called a validation set) of the training set, or via [cross-validation](https://en.wikipedia.org/wiki/Cross-validation_(statistics)).

6.Evaluate the accuracy of the learned function. After parameter adjustment and learning, the performance of the resulting function should be measured on a test set that is separate from the training set.

## **Algorithms**

- Model Building and Error Analysis
- Linear Regression
- Gradient Descent
- Logistic Regression
- Neural Nets
- Support Vector Machines
- k-Nearest Neighbors
- Decision/ Regression Trees
- Ensemble Learning

All of above will be discussed and presented in each folder.

![](RackMultipart20220507-1-yw095s_html_1dc0fc4220830ced.png)
![image](https://user-images.githubusercontent.com/101298565/167263511-23ad3034-a6d2-4519-91fa-b0ad03bfdd3d.png)

