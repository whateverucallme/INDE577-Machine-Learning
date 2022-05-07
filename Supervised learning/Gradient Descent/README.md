
## **Ensemble Learning**

Gradient descent (GD) is an iterative first-order optimisation algorithm used to find a local minimum/maximum of a given function. This method is commonly used in machine learning (ML) and deep learning(DL) to minimise a cost/loss function (e.g. in a linear regression). Due to its importance and ease of implementation, this algorithm is usually taught at the beginning of almost all machine learning courses.

However, its use is not limited to ML/DL only, it&#39;s being widely used also in areas like: control engineering (robotics, chemical, etc.), computer games, mechanical engineering.

That&#39;s why today we will get a deep dive into the math, implementation and behaviour of first-order gradient descent algorithm. We will navigate the custom (cost) function directly to find its minimum, so there will be no underlying data like in typical ML tutorials — we will be more flexible in terms of a function&#39;s shape.

This method was proposed before the era of modern computers and there was an intensive development meantime which led to numerous improved versions of it but in this article, we&#39;re going to use a basic/vanilla gradient descent implemented in Python.

![](RackMultipart20220507-1-xez98c_html_dc115ca7a9e5ebc1.png)
![image](https://user-images.githubusercontent.com/101298565/167265554-a030a7d9-084a-49ac-8f1d-ea0dfc3d72e1.png)


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
