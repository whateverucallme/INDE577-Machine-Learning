## **k-Means clustering**

**Clustering**  is one of the most common exploratory data analysis technique used to get an intuition about the structure of the data. It can be defined as the task of identifying subgroups in the data such that data points in the same subgroup (cluster) are very similar while data points in different clusters are very different. In other words, we try to find homogeneous subgroups within the data such that data points in each cluster are as similar as possible according to a similarity measure such as euclidean-based distance or correlation-based distance. The decision of which similarity measure to use is application-specific.

Clustering analysis can be done on the basis of features where we try to find subgroups of samples based on features or on the basis of samples where we try to find subgroups of features based on samples. We&#39;ll cover here clustering based on features. Clustering is used in market segmentation; where we try to find customers that are similar to each other whether in terms of behaviors or attributes, image segmentation/compression; where we try to group similar regions together, document clustering based on topics, etc.

Unlike supervised learning, clustering is considered an unsupervised learning method since we don&#39;t have the ground truth to compare the output of the clustering algorithm to the true labels to evaluate its performance. We only want to try to investigate the structure of the data by grouping the data points into distinct subgroups.

In this post, we will cover only  **Kmeans**  which is considered as one of the most used clustering algorithms due to its simplicity.

# Kmeans Algorithm

**Kmeans**  algorithm is an iterative algorithm that tries to partition the dataset into _K_pre-defined distinct non-overlapping subgroups (clusters) where each data point belongs to  **only one group**. It tries to make the intra-cluster data points as similar as possible while also keeping the clusters as different (far) as possible. It assigns data points to a cluster such that the sum of the squared distance between the data points and the cluster&#39;s centroid (arithmetic mean of all the data points that belong to that cluster) is at the minimum. The less variation we have within clusters, the more homogeneous (similar) the data points are within the same cluster.

The way kmeans algorithm works is as follows:

1. Specify number of clusters _K_.
2. Initialize centroids by first shuffling the dataset and then randomly selecting _K _data points for the centroids without replacement.
3. Keep iterating until there is no change to the centroids. i.e assignment of data points to clusters isn&#39;t changing.

- Compute the sum of the squared distance between data points and all centroids.
- Assign each data point to the closest cluster (centroid).
- Compute the centroids for the clusters by taking the average of the all data points that belong to each cluster.

The approach kmeans follows to solve the problem is called  **Expectation-Maximization**. The E-step is assigning the data points to the closest cluster. The M-step is computing the centroid of each cluster. Below is a break down of how we can solve it mathematically (feel free to skip it).

The objective function is:
![image](https://user-images.githubusercontent.com/101298565/167272059-2434b9be-2b3a-45bd-b1a6-c49b132220b4.png)


![](RackMultipart20220507-1-t8me6l_html_465cf78fa18b7264.png)

where wik=1 for data point xi if it belongs to cluster _k_; otherwise, wik=0. Also, μk is the centroid of xi&#39;s cluster.

It&#39;s a minimization problem of two parts. We first minimize J w.r.t. wik and treat μk fixed. Then we minimize J w.r.t. μk and treat wik fixed. Technically speaking, we differentiate J w.r.t. wik first and update cluster assignments (_E-step_). Then we differentiate J w.r.t. μk and recompute the centroids after the cluster assignments from previous step (_M-step_). Therefore, E-step is:

![](RackMultipart20220507-1-t8me6l_html_3743be6ae1d9ba56.png)
![image](https://user-images.githubusercontent.com/101298565/167272063-cb22f00d-48cb-4b45-b932-c6f3e5a9a347.png)


In other words, assign the data point xi to the closest cluster judged by its sum of squared distance from cluster&#39;s centroid.

And M-step is:

![](RackMultipart20220507-1-t8me6l_html_af1045c9c22e917d.png)
![image](https://user-images.githubusercontent.com/101298565/167272069-ad89f61a-4595-417d-a41c-f76741aa7e06.png)


Which translates to recomputing the centroid of each cluster to reflect the new assignments.

Few things to note here:

- Since clustering algorithms including kmeans use distance-based measurements to determine the similarity between data points, it&#39;s recommended to standardize the data to have a mean of zero and a standard deviation of one since almost always the features in any dataset would have different units of measurements such as age vs income.
- Given kmeans iterative nature and the random initialization of centroids at the start of the algorithm, different initializations may lead to different clusters since kmeans algorithm may _stuck in a local optimum and may not converge to global optimum_. Therefore, it&#39;s recommended to run the algorithm using different initializations of centroids and pick the results of the run that that yielded the lower sum of squared distance.
- Assignment of examples isn&#39;t changing is the same thing as no change in within-cluster variation:

![](RackMultipart20220507-1-t8me6l_html_fb7f4d9bd1d5a498.png)
![image](https://user-images.githubusercontent.com/101298565/167272074-eb3d8750-b7d1-448a-ac94-600dce2e3984.png)


![](RackMultipart20220507-1-t8me6l_html_4507fc6d44eb506d.jpg)
![image](https://user-images.githubusercontent.com/101298565/167272044-0a80ae6e-67b1-4b6d-9ec7-ea98e6bb60cf.png)


## **Data Characteristics**

:Number of Instances: 150 (50 in each of three classes)

:Number of Attributes: 4 numeric, predictive attributes and the class

:Attribute Information:

- sepal length in cm

- sepal width in cm

- petal length in cm

- petal width in cm

- class:

- Iris-Setosa

- Iris-Versicolour

- Iris-Virginica

:Summary Statistics:

============== ==== ==== ======= ===== ====================

Min Max Mean SD Class Correlation

============== ==== ==== ======= ===== ====================

sepal length: 4.3 7.9 5.84 0.83 0.7826

sepal width: 2.0 4.4 3.05 0.43 -0.4194

petal length: 1.0 6.9 3.76 1.76 0.9490 (high!)

petal width: 0.1 2.5 1.20 0.76 0.9565 (high!)

============== ==== ==== ======= ===== ====================

:Missing Attribute Values: None

:Class Distribution: 33.3% for each of 3 classes.

:Creator: R.A. Fisher

:Donor: Michael Marshall (MARSHALL%PLU@io.arc.nasa.gov)

:Date: July, 1988

The famous Iris database, first used by Sir R.A. Fisher. The dataset is taken

from Fisher&#39;s paper. Note that it&#39;s the same as in R, but not as in the UCI

Machine Learning Repository, which has two wrong data points.

This is perhaps the best known database to be found in the

pattern recognition literature. Fisher&#39;s paper is a classic in the field and

is referenced frequently to this day. (See Duda &amp; Hart, for example.) The

data set contains 3 classes of 50 instances each, where each class refers to a

type of iris plant. One class is linearly separable from the other 2; the

latter are NOT linearly separable from each other.

References

- Fisher, R.A. &quot;The use of multiple measurements in taxonomic problems&quot;

Annual Eugenics, 7, Part II, 179-188 (1936); also in &quot;Contributions to

Mathematical Statistics&quot; (John Wiley, NY, 1950).

- Duda, R.O., &amp; Hart, P.E. (1973) Pattern Classification and Scene Analysis.

(Q327.D83) John Wiley &amp; Sons. ISBN 0-471-22361-1. See page 218.

- Dasarathy, B.V. (1980) &quot;Nosing Around the Neighborhood: A New System

Structure and Classification Rule for Recognition in Partially Exposed

Environments&quot;. IEEE Transactions on Pattern Analysis and Machine

Intelligence, Vol. PAMI-2, No. 1, 67-71.

- Gates, G.W. (1972) &quot;The Reduced Nearest Neighbor Rule&quot;. IEEE Transactions

on Information Theory, May 1972, 431-433.

- See also: 1988 MLC Proceedings, 54-64. Cheeseman et al&quot;s AUTOCLASS II

conceptual clustering system finds 3 classes in the data.
