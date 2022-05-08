## **Regression Tree**

![](RackMultipart20220507-1-hbg9c4_html_b0732fb190e0846e.png)
![image](https://user-images.githubusercontent.com/101298565/167264996-577826d0-9e2a-4655-a1bc-465b4e9d61b2.png)

A regression tree is built through a process known as binary recursive partitioning, which is an iterative process that splits the data into partitions or branches, and then continues splitting each partition into smaller groups as the method moves up each branch.

Initially, all records in the Training Set (pre-classified records that are used to determine the structure of the tree) are grouped into the same partition. The algorithm then begins allocating the data into the first two partitions or branches, using every possible binary split on every field. The algorithm selects the split that minimizes the sum of the squared deviations from the mean in the two separate partitions.

This splitting rule is then applied to each of the new branches. This process continues until each node reaches a user-specified minimum node size and becomes a terminal node. (If the sum of squared deviations from the mean in a node is zero, then that node is considered a terminal node even if it has not reached the minimum size.

## **Data Characteristics**


Cardata.csv is the dataset of the decision tree and I combine the svm and decision tree model in SVM folder.

[SAS code](https://www4.stat.ncsu.edu/~boos/var.select/diabetes.read.tab.txt) to access the data using [the original data set](https://www4.stat.ncsu.edu/~boos/var.select/diabetes.tab.txt) from [Trevor Hastie&#39;s LARS software page.](http://www-stat.stanford.edu/~hastie/Papers/LARS)

[Proc Means and Proc Print Output](https://www4.stat.ncsu.edu/~boos/var.select/diabetes.read.tab.out.txt) when using the above data.

[The data](https://www4.stat.ncsu.edu/~boos/var.select/diabetes.rwrite1.txt) from the R package lars. [SAS code](https://www4.stat.ncsu.edu/~boos/var.select/diabetes.read.rdata.txt) to access these data. [Proc Means and Proc Print Output](https://www4.stat.ncsu.edu/~boos/var.select/diabetes.read.rdata.out.txt) when using the above data from R. Note that the 10 x variables have been standardized to have mean 0 and squared length = 1 (sum(x^2)=1).

[SAS Data](https://www4.stat.ncsu.edu/~boos/var.select/diabetes2.sas7bdat) set of Hastie&#39;s &quot;quadratic model&quot; data64.txt with Y added at the end.

Brief Description

From Bradley Efron, Trevor Hastie, Iain Johnstone and Robert Tibshirani (2004) &quot;Least Angle Regression,&quot; Annals of Statistics (with discussion), 407-499, we have

&quot;Ten baseline variables, age, sex, body mass index, average blood pressure, and six blood serum measurements were obtained for each of n = 442 diabetes patients, as well as the response of interest, a quantitative measure of disease progression one year after baseline.&quot;

Characteristics

Number of Instances: 442

Number of Attributes: First 10 columns are numeric predictive values

Target: Column 11 is a quantitative measure of disease progression one year after baseline

Attribute Information:

- age age in years

- sex male and female

- bmi body mass index

- bp average blood pressure

- s1 tc, T-Cells (a type of white blood cells)

- s2 ldl, low-density lipoproteins

- s3 hdl, high-density lipoproteins

- s4 tch, thyroid stimulating hormone

- s5 ltg, lamotrigine

- s6 glu, blood sugar level

Note: Each of these 10 feature variables have been mean centered and scaled by the standard deviation times `n_samples` (i.e. the sum of squares of each column totals 1).

Source URL:

https://www4.stat.ncsu.edu/~boos/var.select/diabetes.html
