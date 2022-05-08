
## **logistic regression**

Logic Regression is an adaptive regression methodology that attempts to construct predictors as Boolean combinations of binary covariates.

In most regression problems a model is developed that only relates the main effects (the predictors or transformations thereof) to the response. Although interactions between predictors are considered sometimes as well, those interactions are usually kept very simple (two- to three-way interactions at most). But often, especially when all predictors are binary, the interaction between many predictors is what causes the differences in response. This issue often arises in the analysis of SNP microarray data or in data mining problems. Given a set of binary predictors X, we try to create new, better predictors for the response by considering combinations of those binary predictors. For example, if the response is binary as well (which is not required in general), we attempt to find decision rules such as ``if X1, X2, X3 and X4 are true&#39;&#39;, or ``X5 or X6 but not X7 are true&#39;&#39;, then the response is more likely to be in class 0. In other words, we try to find Boolean statements involving the binary predictors that enhance the prediction for the response. In more specific terms: Let X1,…,Xk be binary predictors, and let Y be a response variable. We try to fit regression models of the form g(E[Y]) = b0 + b1L1 + …+ bnLn, where Lj is a Boolean expression of the predictors X, such as Lj=[(X2 or X4c) and X7]. The above framework includes many forms of regression, such as linear regression (g(E[Y])=E[Y]) and logistic regression (g(E[Y])=log(E[Y]/(1-E[Y]))). For every model type, we define a score function that reflects the ``quality&#39;&#39; of the model under consideration. For example, for linear regression the score could be the residual sum of squares and for logistic regression the score could be the deviance. We try to find the Boolean expressions in the regression model that minimize the scoring function associated with this model type, estimating the parameters bj simultaneously with the Boolean expressions Lj. In general, any type of model can be considered, as long as a scoring function can be defined. For example, we also implemented the Cox proportional hazards model, using the partial likelihood as the score.

Since the number of possible Logic Models we can construct for a given set of predictors is huge, we have to rely on some search algorithms to help us find the best scoring models. We define the move set by a set of standard operations such as splitting and pruning the tree (similar to the terminology introduced by Breiman et al). We implemented two types of algorithms: a greedy and a simulated annealing algorithm. While the greedy algorithm is very fast, it does not always find a good scoring model. The simulated annealing algorithm usually does, but computationally it is more expensive. Since we have to be certain to find good scoring models, we usually carry out simulated annealing for our case studies. However, as usual, the best scoring model generally over-fits the data, and methods to separate signal and noise are needed. We implemented methods for candidate models found by either the greedy or simulated annealing algorithms. In the latter case, a definition of model size was needed, and a technique was implemented to find the best scoring model of a particular size. For the model selection itself we developed and implemented randomization tests and tests using cross-validation. If sufficient data is available, an analysis using a training and a test set can also be carried out. ![](RackMultipart20220507-1-nv10f5_html_f9ef8ba063db91f8.jpg)
![image](https://user-images.githubusercontent.com/101298565/167267094-9f854a53-40e2-45e3-98b1-953d846ae6e8.png)


## **Data Characteristics**

I am going to build two logistic models because I felt the first one is not so good. So I decided to make another one to make my grade higher if possible.



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
