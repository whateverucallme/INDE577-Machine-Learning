
## **Principal component analysis**

The principal components of a collection of points in a [real coordinate space](https://en.wikipedia.org/wiki/Real_coordinate_space) are a sequence of {\displaystyle p} ![Shape1](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  [unit vectors](https://en.wikipedia.org/wiki/Unit_vector), where the {\displaystyle i} ![Shape2](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif) -th vector is the direction of a line that best fits the data while being [orthogonal](https://en.wikipedia.org/wiki/Orthogonal) to the first {\displaystyle i-1} ![Shape3](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  vectors. Here, a best-fitting line is defined as one that minimizes the average squared [distance from the points to the line](https://en.wikipedia.org/wiki/Distance_from_a_point_to_a_line). These directions constitute an [orthonormal basis](https://en.wikipedia.org/wiki/Orthonormal_basis) in which different individual dimensions of the data are [linearly uncorrelated](https://en.wikipedia.org/wiki/Linear_correlation). Principal component analysis (PCA) is the process of computing the principal components and using them to perform a [change of basis](https://en.wikipedia.org/wiki/Change_of_basis) on the data, sometimes using only the first few principal components and ignoring the rest.

In data analysis, the first principal component of a set of {\displaystyle p} ![Shape4](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  variables, presumed to be normally distributed, is the derived variable formed as a linear combination of the original variables that explains the most variance. The second principal component explains the most variance in what is left once the effect of the first component is removed, and we may proceed through {\displaystyle p} ![Shape5](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  iterations until all the variance is explained. PCA is most commonly used when many of the variables are highly correlated with each other and it is desirable to reduce their number to an independent set.

PCA is used in [exploratory data analysis](https://en.wikipedia.org/wiki/Exploratory_data_analysis) and for making [predictive models](https://en.wikipedia.org/wiki/Predictive_modeling). It is commonly used for [dimensionality reduction](https://en.wikipedia.org/wiki/Dimensionality_reduction) by projecting each data point onto only the first few principal components to obtain lower-dimensional data while preserving as much of the data&#39;s variation as possible. The first principal component can equivalently be defined as a direction that maximizes the variance of the projected data. The {\displaystyle i} ![Shape6](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif) -th principal component can be taken as a direction orthogonal to the first {\displaystyle i-1} ![Shape7](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  principal components that maximizes the variance of the projected data.

For either objective, it can be shown that the principal components are [eigenvectors](https://en.wikipedia.org/wiki/Eigenvectors) of the data&#39;s [covariance matrix](https://en.wikipedia.org/wiki/Covariance_matrix). Thus, the principal components are often computed by eigendecomposition of the data covariance matrix or [singular value decomposition](https://en.wikipedia.org/wiki/Singular_value_decomposition) of the data matrix. PCA is the simplest of the true eigenvector-based multivariate analyses and is closely related to [factor analysis](https://en.wikipedia.org/wiki/Factor_analysis). Factor analysis typically incorporates more domain specific assumptions about the underlying structure and solves eigenvectors of a slightly different matrix. PCA is also related to [canonical correlation analysis (CCA)](https://en.wikipedia.org/wiki/Canonical_correlation). CCA defines coordinate systems that optimally describe the [cross-covariance](https://en.wikipedia.org/wiki/Cross-covariance) between two datasets while PCA defines a new [orthogonal coordinate system](https://en.wikipedia.org/wiki/Orthogonal_coordinate_system) that optimally describes variance in a single dataset.[[1]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-1)[[2]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-2)[[3]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-mark2017-3)[[4]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-l1tucker-4) [Robust](https://en.wikipedia.org/wiki/Robust_statistics) and [L1-norm](https://en.wikipedia.org/wiki/Lp_space)-based variants of standard PCA have also been proposed

![](RackMultipart20220507-1-rb2rol_html_ab7c9970da386243.jpg)
![image](https://user-images.githubusercontent.com/101298565/167271821-c5556863-b51a-4617-beab-f9264b0494e3.png)


## **Data Characteristics**

|
# **Wine Data Set**

_Download_: [Data Folder](http://archive.ics.uci.edu/ml/machine-learning-databases/wine/), [Data Set Description](http://archive.ics.uci.edu/ml/machine-learning-databases/wine/wine.names) **Abstract** : Using chemical analysis determine the origin of wines |
 |
| --- | --- |

| **Data Set Characteristics:  ** | Multivariate | **Number of Instances:** | 178 | **Area:** | Physical |
| --- | --- | --- | --- | --- | --- |
| **Attribute Characteristics:** | Integer, Real | **Number of Attributes:** | 13 | **Date Donated** | 1991-07-01 |
| **Associated Tasks:** | Classification | **Missing Values?** | No | **Number of Web Hits:** | 1913130 |

**Source:**

Original Owners:

 Forina, M. et al, PARVUS -
 An Extendible Package for Data Exploration, Classification and Correlation.
 Institute of Pharmaceutical and Food Analysis and Technologies, Via Brigata Salerno,
 16147 Genoa, Italy.

 Donor:

 Stefan Aeberhard, email: stefan  **&#39;@&#39;**  coral.cs.jcu.edu.au

**Data Set Information:**

These data are the results of a chemical analysis of wines grown in the same region in Italy but derived from three different cultivars. The analysis determined the quantities of 13 constituents found in each of the three types of wines.

 I think that the initial data set had around 30 variables, but for some reason I only have the 13 dimensional version. I had a list of what the 30 or so variables were, but a.) I lost it, and b.), I would not know which 13 variables are included in the set.

 The attributes are (dontated by Riccardo Leardi, riclea  **&#39;@&#39;**  anchem.unige.it )
 1) Alcohol
 2) Malic acid
 3) Ash
 4) Alcalinity of ash
 5) Magnesium
 6) Total phenols
 7) Flavanoids
 8) Nonflavanoid phenols
 9) Proanthocyanins
 10)Color intensity
 11)Hue
 12)OD280/OD315 of diluted wines
 13)Proline

 In a classification context, this is a well posed problem with &quot;well behaved&quot; class structures. A good data set for first testing of a new classifier, but not very challenging.

**Attribute Information:**

All attributes are continuous

 No statistics available, but suggest to standardise variables for certain uses (e.g. for us with classifiers which are NOT scale invariant)

 NOTE: 1st attribute is class identifier (1-3)

**Relevant Papers:**

(1)
 S. Aeberhard, D. Coomans and O. de Vel,
 Comparison of Classifiers in High Dimensional Settings,
 Tech. Rep. no. 92-02, (1992), Dept. of Computer Science and Dept. of
 Mathematics and Statistics, James Cook University of North Queensland.
 (Also submitted to Technometrics).

 The data was used with many others for comparing various
 classifiers. The classes are separable, though only RDA
 has achieved 100% correct classification.
 (RDA : 100%, QDA 99.4%, LDA 98.9%, 1NN 96.1% (z-transformed data))
 (All results using the leave-one-out technique)

 (2)
 S. Aeberhard, D. Coomans and O. de Vel,
 &quot;THE CLASSIFICATION PERFORMANCE OF RDA&quot;
 Tech. Rep. no. 92-01, (1992), Dept. of Computer Science and Dept. of
 Mathematics and Statistics, James Cook University of North Queensland.
 (Also submitted to Journal of Chemometrics).

 Here, the data was used to illustrate the superior performance of
 the use of a new appreciation function with RDA.
