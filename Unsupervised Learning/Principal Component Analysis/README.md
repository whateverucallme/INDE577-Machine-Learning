
## **Principal component analysis**

The principal components of a collection of points in a [real coordinate space](https://en.wikipedia.org/wiki/Real_coordinate_space) are a sequence of {\displaystyle p} ![Shape1](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  [unit vectors](https://en.wikipedia.org/wiki/Unit_vector), where the {\displaystyle i} ![Shape2](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif) -th vector is the direction of a line that best fits the data while being [orthogonal](https://en.wikipedia.org/wiki/Orthogonal) to the first {\displaystyle i-1} ![Shape3](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  vectors. Here, a best-fitting line is defined as one that minimizes the average squared [distance from the points to the line](https://en.wikipedia.org/wiki/Distance_from_a_point_to_a_line). These directions constitute an [orthonormal basis](https://en.wikipedia.org/wiki/Orthonormal_basis) in which different individual dimensions of the data are [linearly uncorrelated](https://en.wikipedia.org/wiki/Linear_correlation). Principal component analysis (PCA) is the process of computing the principal components and using them to perform a [change of basis](https://en.wikipedia.org/wiki/Change_of_basis) on the data, sometimes using only the first few principal components and ignoring the rest.

In data analysis, the first principal component of a set of {\displaystyle p} ![Shape4](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  variables, presumed to be normally distributed, is the derived variable formed as a linear combination of the original variables that explains the most variance. The second principal component explains the most variance in what is left once the effect of the first component is removed, and we may proceed through {\displaystyle p} ![Shape5](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  iterations until all the variance is explained. PCA is most commonly used when many of the variables are highly correlated with each other and it is desirable to reduce their number to an independent set.

PCA is used in [exploratory data analysis](https://en.wikipedia.org/wiki/Exploratory_data_analysis) and for making [predictive models](https://en.wikipedia.org/wiki/Predictive_modeling). It is commonly used for [dimensionality reduction](https://en.wikipedia.org/wiki/Dimensionality_reduction) by projecting each data point onto only the first few principal components to obtain lower-dimensional data while preserving as much of the data&#39;s variation as possible. The first principal component can equivalently be defined as a direction that maximizes the variance of the projected data. The {\displaystyle i} ![Shape6](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif) -th principal component can be taken as a direction orthogonal to the first {\displaystyle i-1} ![Shape7](RackMultipart20220507-1-rb2rol_html_49ac0cb03196381.gif)  principal components that maximizes the variance of the projected data.

For either objective, it can be shown that the principal components are [eigenvectors](https://en.wikipedia.org/wiki/Eigenvectors) of the data&#39;s [covariance matrix](https://en.wikipedia.org/wiki/Covariance_matrix). Thus, the principal components are often computed by eigendecomposition of the data covariance matrix or [singular value decomposition](https://en.wikipedia.org/wiki/Singular_value_decomposition) of the data matrix. PCA is the simplest of the true eigenvector-based multivariate analyses and is closely related to [factor analysis](https://en.wikipedia.org/wiki/Factor_analysis). Factor analysis typically incorporates more domain specific assumptions about the underlying structure and solves eigenvectors of a slightly different matrix. PCA is also related to [canonical correlation analysis (CCA)](https://en.wikipedia.org/wiki/Canonical_correlation). CCA defines coordinate systems that optimally describe the [cross-covariance](https://en.wikipedia.org/wiki/Cross-covariance) between two datasets while PCA defines a new [orthogonal coordinate system](https://en.wikipedia.org/wiki/Orthogonal_coordinate_system) that optimally describes variance in a single dataset.[[1]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-1)[[2]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-2)[[3]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-mark2017-3)[[4]](https://en.wikipedia.org/wiki/Principal_component_analysis#cite_note-l1tucker-4) [Robust](https://en.wikipedia.org/wiki/Robust_statistics) and [L1-norm](https://en.wikipedia.org/wiki/Lp_space)-based variants of standard PCA have also been proposed

![](RackMultipart20220507-1-rb2rol_html_ab7c9970da386243.jpg)
![image](https://user-images.githubusercontent.com/101298565/167271821-c5556863-b51a-4617-beab-f9264b0494e3.png)


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
