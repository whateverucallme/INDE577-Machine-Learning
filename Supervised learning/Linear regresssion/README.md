![image](https://user-images.githubusercontent.com/101298565/167265777-17be19de-4292-479e-93bf-9dd9b9caf1c3.png)
## **Linear regression**

Before knowing what is linear regression, let us get ourselves accustomed to regression. Regression is a method of modelling a target value based on independent predictors. This method is mostly used for forecasting and finding out cause and effect relationship between variables. Regression techniques mostly differ based on the number of independent variables and the type of relationship between the independent and dependent variables.
![image](https://user-images.githubusercontent.com/101298565/167266081-ca31f526-8d85-4540-8abf-8b81065e25a6.png)


![](RackMultipart20220507-1-fmijql_html_dbd695a259e7c9e5.png)

Linear Regression

Simple linear regression is a type of regression analysis where the number of independent variables is one and there is a linear relationship between the independent(x) and dependent(y) variable. The red line in the above graph is referred to as the best fit straight line. Based on the given data points, we try to plot a line that models the points the best. The line can be modelled based on the linear equation shown below.

y = a\_0 + a\_1 \* x ## Linear Equation

The motive of the linear regression algorithm is to find the best values for a\_0 and a\_1. Before moving on to the algorithm, let&#39;s have a look at two important concepts you must know to better understand linear regression.

Cost Function

The cost function helps us to figure out the best possible values for a\_0 and a\_1 which would provide the best fit line for the data points. Since we want the best values for a\_0 and a\_1, we convert this search problem into a minimization problem where we would like to minimize the error between the predicted value and the actual value.
![image](https://user-images.githubusercontent.com/101298565/167266090-876a7869-328f-40a4-bf8e-fedb9b8978c6.png)

![](RackMultipart20220507-1-fmijql_html_83fd562798e88292.png)

Minimization and Cost Function

We choose the above function to minimize. The difference between the predicted values and ground truth measures the error difference. We square the error difference and sum over all data points and divide that value by the total number of data points. This provides the average squared error over all the data points. Therefore, this cost function is also known as the Mean Squared Error(MSE) function. Now, using this MSE function we are going to change the values of a\_0 and a\_1 such that the MSE value settles at the minima.

Gradient Descent

The next important concept needed to understand linear regression is gradient descent. Gradient descent is a method of updating a\_0 and a\_1 to reduce the cost function(MSE). The idea is that we start with some values for a\_0 and a\_1 and then we change these values iteratively to reduce the cost. Gradient descent helps us on how to change the values.
![image](https://user-images.githubusercontent.com/101298565/167266105-fcef5a15-49fa-483d-b789-bacd58cb842a.png)

![](RackMultipart20220507-1-fmijql_html_6a6c7557f13811e4.png)

Gradient Descent

To draw an analogy, imagine a pit in the shape of U and you are standing at the topmost point in the pit and your objective is to reach the bottom of the pit. There is a catch, you can only take a discrete number of steps to reach the bottom. If you decide to take one step at a time you would eventually reach the bottom of the pit but this would take a longer time. If you choose to take longer steps each time, you would reach sooner but, there is a chance that you could overshoot the bottom of the pit and not exactly at the bottom. In the gradient descent algorithm, the number of steps you take is the learning rate. This decides on how fast the algorithm converges to the minima.
![image](https://user-images.githubusercontent.com/101298565/167266113-060bcb48-b784-439b-91c4-a52eb9d78c8a.png)

![](RackMultipart20220507-1-fmijql_html_7adeab452d7ebfe2.png)

Convex vs Non-convex function

Sometimes the cost function can be a non-convex function where you could settle at a local minima but for linear regression, it is always a convex function.

You may be wondering how to use gradient descent to update a\_0 and a\_1. To update a\_0 and a\_1, we take gradients from the cost function. To find these gradients, we take partial derivatives with respect to a\_0 and a\_1. Now, to understand how the partial derivatives are found below you would require some calculus but if you don&#39;t, it is alright. You can take it as it is.

![image](https://user-images.githubusercontent.com/101298565/167266175-4b676d42-b672-43b6-a89f-44a115f6c3d9.png)

![](RackMultipart20220507-1-fmijql_html_438666d2eb3f21be.png)

![](RackMultipart20220507-1-fmijql_html_df83a0f0c9ed9d9c.png)

The partial derivates are the gradients and they are used to update the values of a\_0 and a\_1. Alpha is the learning rate which is a hyperparameter that you must specify. A smaller learning rate could get you closer to the minima but takes more time to reach the minima, a larger learning rate converges sooner but there is a chance that you could overshoot the minima.

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
