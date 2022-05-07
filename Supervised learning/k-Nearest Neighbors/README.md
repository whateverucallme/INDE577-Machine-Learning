
## **k-Nearest Neighbors**

The k-nearest neighbors (KNN) algorithm is a data classification method for estimating the likelihood that a data point will become a member of one group or another based on what group the data points nearest to it belong to.

The k-nearest neighbor algorithm is a type of [supervised machine learning](https://learn.g2.com/supervised-learning) algorithm used to solve classification and regression problems. However, it&#39;s mainly used for classification problems.

KNN is a _lazy learning_ and _non-parametric_ algorithm.

It&#39;s called a lazy learning algorithm or lazy learner because it doesn&#39;t perform any training when you supply the training data. Instead, it just stores the data during the training time and doesn&#39;t perform any calculations. It doesn&#39;t build a model until a query is performed on the dataset. This makes KNN ideal for [data mining](https://www.g2.com/articles/data-mining).

Did you know? The &quot;K&quot; in KNN is a parameter that determines the number of nearest neighbors to include in the voting process.

It&#39;s considered a non-parametric method because it doesn&#39;t make any assumptions about the underlying data distribution. Simply put, KNN tries to determine what group a data point belongs to by looking at the data points around it.

Consider there are two groups, A and B.

To determine whether a data point is in group A or group B, the algorithm looks at the states of the data points near it. If the majority of data points are in group A, it&#39;s very likely that the data point in question is in group A and vice versa.

In short, KNN involves classifying a data point by looking at the nearest annotated data point, also known as the _nearest neighbor_.

Don&#39;t confuse K-NN classification with K-means clustering. KNN is a supervised classification algorithm that classifies new data points based on the nearest data points. On the other hand, K-means clustering is an [unsupervised](https://learn.g2.com/unsupervised-learning) clustering algorithm that groups data into a K number of clusters.

##
# How does KNN work?

As mentioned above, the KNN algorithm is predominantly used as a classifier. Let&#39;s take a look at how KNN works to classify unseen input data points.

Unlike classification using artificial neural networks, k-nearest neighbors classification is easy to understand and simple to implement. It&#39;s ideal in situations where the data points are well defined or non-linear.

In essence, KNN performs a voting mechanism to determine the class of an unseen observation. This means that the class with the majority vote will become the class of the data point in question.

If the value of K is equal to one, then we&#39;ll use only the nearest neighbor to determine the class of a data point. If the value of K is equal to ten, then we&#39;ll use the ten nearest neighbors, and so on.

Tip: Automate tasks and make data-driven decisions using [machine learning software](https://www.g2.com/categories/machine-learning).

To put that into perspective, consider an unclassified data point X. There are several data points with known categories, A and B, in a scatter plot.

Suppose the data point X is placed near group A.

As you know, we classify a data point by looking at the nearest annotated points. If the value of K is equal to one, then we&#39;ll use only one nearest neighbor to determine the group of the data point.

In this case, the data point X belongs to group A as its nearest neighbor is in the same group. If group A has more than ten data points and the value of K is equal to 10, then the data point X will still belong to group A as all its nearest neighbors are in the same group.

Suppose another unclassified data point Y is placed between group A and group B. If K is equal to 10, we pick the group that gets the most votes, meaning that we classify Y to the group in which it has the most number of neighbors. For example, if Y has seven neighbors in group B and three neighbors in group A, it belongs to group B.

The fact that the classifier assigns the category with the highest number of votes is true regardless of the number of categories present.

You might be wondering how the distance metric is calculated to determine whether a data point is a neighbor or not.

There are four ways to calculate the distance measure between the data point and its nearest neighbor: Euclidean distance, Manhattan distance, Hamming distance, and Minkowski distance. Out of the three, Euclidean distance is the most commonly used distance function or metric.
![image](https://user-images.githubusercontent.com/101298565/167270054-ae8cc205-33b7-4c84-bfc0-ab55f55923f9.png)


###
## K-nearest neighbor algorithm pseudocode

Programming languages like Python and R are used to implement the KNN algorithm. The following is the pseudocode for KNN:

1. Load the data
2. Choose K value
3. For each data point in the data:
  - Find the Euclidean distance to all training data samples
  - Store the distances on an ordered list and sort it
  - Choose the top K entries from the sorted list
  - Label the test point based on the majority of classes present in the selected points
4. End

To validate the accuracy of the KNN classification, a [confusion matrix](https://www.analyticsvidhya.com/blog/2020/04/confusion-matrix-machine-learning/) is used. Other statistical methods such as the likelihood-ratio test are also used for validation.

In the case of KNN regression, the majority of steps are the same. Instead of assigning the class with the highest votes, the average of the neighbors&#39; values is calculated and assigned to the unknown data point.

![](RackMultipart20220507-1-delesv_html_9954833c416541d.png)

## **Data Characteristics**

:Number of Instances: 1797

:Number of Attributes: 64

:Attribute Information: 8x8 image of integer pixels in the range 0..16.

:Missing Attribute Values: None

:Creator: E. Alpaydin (alpaydin &#39;@&#39; boun.edu.tr)

:Date: July; 1998

Source:

This is a copy of the test set of the UCI ML hand-written digits datasets

https://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits

The data set contains images of hand-written digits: 10 classes where each class refers to a digit.

Data Set Information:

We used preprocessing programs made available by NIST to extract normalized bitmaps of handwritten digits from a preprinted form. From a total of 43 people, 30 contributed to the training set and different 13 to the test set. 32x32 bitmaps are divided into nonoverlapping blocks of 4x4 and the number of on pixels are counted in each block. This generates an input matrix of 8x8 where each element is an integer in the range 0..16. This reduces dimensionality and gives invariance to small distortions.

 For info on NIST preprocessing routines, see M. D. Garris, J. L. Blue, G. T. Candela, D. L. Dimmick, J. Geist, P. J. Grother, S. A. Janet, and C. L. Wilson, NIST Form-Based Handprint Recognition System, NISTIR 5469, 1994.

**Reference**

- C. Kaynak (1995) Methods of Combining Multiple Classifiers and Their

Applications to Handwritten Digit Recognition, MSc Thesis, Institute of

Graduate Studies in Science and Engineering, Bogazici University.

- E. Alpaydin, C. Kaynak (1998) Cascading Classifiers, Kybernetika.

- Ken Tang and Ponnuthurai N. Suganthan and Xi Yao and A. Kai Qin.

Linear dimensionalityreduction using relevance weighted LDA. School of

Electrical and Electronic Engineering Nanyang Technological University.

2005.

- Claudio Gentile. A New Approximate Maximal Margin Classification

Algorithm. NIPS. 2000.
