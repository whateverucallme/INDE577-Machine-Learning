## **Ensemble Learning**

![image](https://user-images.githubusercontent.com/101298565/167265332-82266ccc-d82a-4e96-8d82-17eccfddea40.png)

Ensemble learning is a general meta approach to machine learning that seeks better predictive performance by combining the predictions from multiple models.

Although there are a seemingly unlimited number of ensembles that we can develop for our predictive modeling problem, there are three methods that dominate the field of ensemble learning. So much so, that rather than algorithms per se, each is a field of study that has spawned many more specialized methods.

The three main classes of ensemble learning methods are bagging, stacking, and boosting, and it is important to both have a detailed understanding of each method and to consider them on our predictive modeling project.

![](RackMultipart20220507-1-o0a9tb_html_887c8f9b152705f8.png)

## **Data Characteristics**

:Number of Instances: 1797

:Number of Attributes: 64

:Attribute Information: 8x8 image of integer pixels in the range 0..16.

:Missing Attribute Values: None

:Creator: E. Alpaydin (alpaydin &#39;@&#39; boun.edu.tr)

:Date: July; 1998

**Source:**

This is a copy of the test set of the UCI ML hand-written digits datasets

https://archive.ics.uci.edu/ml/datasets/Optical+Recognition+of+Handwritten+Digits

The data set contains images of hand-written digits: 10 classes where each class refers to a digit.

**Data Set Information:**

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
