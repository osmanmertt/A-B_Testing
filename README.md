# AB_Testing
# General Information About A/B Test  
In this study, a project about A/B Testing was carried out. First, brief information about the subject will be given.

"A hypothesis, in a scientific context, is a testable statement about the relationship between two or more variables or a proposed explanation for some observed phenomenon." A/B testing is a form of hypothesis testing. In this study, the focus was on using the A/B test, to determine whether the differences between the groups occurred randomly, whether there was a significant difference. A and B here represent the control group and test group.

There are 3 steps that can be followed for testing.
> **1. Writing Hypotheses**  
> **2. Assumption control**  
>  &emsp;  **-Assumption of Normality**  
>  &emsp;  **-Variance Homogeneity**  
> **3. Testing the Hypothesis and Interpreting the Results**    

**1.** The hypotheses need to be written. The hypotheses can be written as follows.
> **H0:  M1 = M2**   &emsp; &emsp;  **H0: M1 <= M2**  &emsp; &emsp;  **H0: M1 >= M2**  
 **H1:  M1 != M2**  &emsp; &emsp;  **H1: M1 > M2**  &emsp; &emsp;   **H1: M1 < M2**
 
H0 and H1 represent hypotheses. H0 is called null hypothesis, and H1 is called alternative hypothesis. For example, we can say M1=M2 as there is no difference between the mean of the two groups.

**2.** In the second step, assumption controls should be made. T-test was used in this study. In this regard, our Assumptions can be summarized as follows:
> **Assumption of Normality :** The data for each group should be approximately normally distributed.  
> **Variance Homogeneity :** The variance of the outcome variable should be equal in each group.

**3.** If all the assumptions are met, the parametric test, the T-Test, can be used. If the assumption of normality is not met, the Mann-Whitney U test, which is a non-parametric test, is used directly. If the assumption of normality is met, but the assumption of homogeneity of variance is not met, the T-Test is used, but it is indicated by entering the relevant argument that the assumption of homogeneity of variance is not met.


Hypotheses can be evaluated through test statistics. There are various formulas according to sample numbers and variance homogeneity. Here, after using the relevant formula and calculating the values, it can be examined whether the H0 hypothesis will be rejected or not. However, we will use the p-value in this study. If the p-value<0.05, the H0 hypothesis is rejected. There is also an important point, we can reject H0 or not. There is no form of evaluation such as accepting H1. The p-value can be obtained by using the function of the relevant test (T-Test, Mann-Whitney U Test) and an interpretation can be made accordingly.

# Business Problem and Dataset

The business problem to be discussed in this study is as follows. A company has introduced a new bidding type, 'average bidding', as an alternative to the current bidding type, 'maximum bidding'. In this study, it will be tested whether average bidding brings more conversions than maximum bidding. While performing statistical tests, the purchase metric in the dataset will be focused on.

Information about the columns is given below.

* **Impression :** Number of Ad Views
* **Click :** Number of Clicks on the Viewed Ad
* **Purchase :** Number of Products Purchased After Ads Clicked
* **Earning :** Earnings After Purchased Products
