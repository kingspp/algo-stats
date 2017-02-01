#Information Value and Weight of Evidence

**What is Mutual Information?**<br>
It is a way of summarizing much knowing the value of one random variable tells you about another random variable. 
If X and Y are independent, the mutual information is zero. Any correlations (positive, negative, or nonlinear) will result in positive mutual information.<br>
It is the difference in predictability that you get from knowing the joint distribution p(X,Y) compared to knowing only the two marginal distributions p(X) and p(Y).<br>

Mutual information of X and Y is expressed in terms of entropy (H):
```
MI(X,Y)=H(X)+H(Y)−H(X,Y)
```
**What is Weight of Evidence?**<br>
It is a measure of the predictive power of an independent variable in relation to the dependent variable. It is a widely used measure of the "strength” of a grouping for separating events and non-events (default)

```
WOE = ln (Distribution of Events / Distribution of Non Events)
```
**Example:**

| Age  | Propensity to buy a Motorcycle |
| ------------- | ------------- |
| 23 | 1 |
| 42 | 1 |
| 54 | 0 |
| 32 | 1 |
| 63 | 0 |
| 56 | 0 |
| 24 | 1 |
| 65 | 0 |
| 54 | 0 |
| 63 | 0 |
| 53 | 1 |
| 57 | 0 |
| 61 | 1 |
| 54 | 1 |
| 64 | 1 |
| 24 | 0 |
| 33 | 0 |
| 45 | 0 |

**Note: If the variable is not categorical, create bins for the variable**<br><br>
**Rules for WOE**<br>
1. Each category (bin) should have at least 5% of the observations.<br>
2. Each category (bin) should be non-zero for both non-events and events.<br>
3. The WOE should be distinct for each category. Similar groups should be aggregated. <br>
4. The WOE should be monotonic, i.e. either growing or decreasing with the groupings.<br>
5. Missing values are binned separately.<br><br>

**Rules for Binning Algorithm**<br>
1. The WOE should be monotonic i.e. either growing or decreasing with the bins.<br>
2. The slope of the Logistic regression with an independent variable having WOE values is not 1 or the intercept is not ln(% of non-events / % of events) then the binning algorithm is wrong.

| Age bins  | Count | Events (1's) | Non-Events ( count - events) | Distribution of Events | Distribution of Non Events | **Weight of Evidence** |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 20-29 | 3 | 2 | 1 | 0.25  | 0.1 | 0.91 |
| 30-39 | 2 | 1 | 1 | 0.125 | 0.1 | 0.22 |
| 40-49 | 2 | 1 | 1 | 0.125 | 0.1 | 0.22 |
| 50-59 | 6 | 2 | 4 | 0.25  | 0.4 | -0.47 |
| 60-69 | 5 | 2 | 3 | 0.25  | 0.3 | -0.18 |
| **Total** | **18** | **8** | **10** | - | - | - |<br>


**What is Information Value (IV)?**<br>
The Information Value (IV) of a predictor is related to the sum of the (absolute) values for WoE over all groups. It helps to rank variables on the basis of their importance

```
IV = ∑ (% of non-events - % of events) * WOE
```
**Example:**

| Age bins  | Count | Events (1's) | Non-Events ( count - events) | Distribution of Events | Distribution of Non Events | WOE | **IV** |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |          ------------- |
| 20-29 | 3 | 2 | 1 | 0.25  | 0.1 | 0.91  | -0.137 |
| 30-39 | 2 | 1 | 1 | 0.125 | 0.1 | 0.22  | -0.005 |
| 40-49 | 2 | 1 | 1 | 0.125 | 0.1 | 0.22  | -0.005 |
| 50-59 | 6 | 2 | 4 | 0.25  | 0.4 | -0.47 | -0.070 |
| 60-69 | 5 | 2 | 3 | 0.25  | 0.3 | -0.18 | -0.009 |
| **Total** | **18** | **8** | **8** | **10** | - | - | -0.228 |

**Information Value Measure:**

| Information Value |	Variable Predictiveness |
| ----------------- | ----------------------- |
| < 0.02 | Not useful for prediction |
| 0.02 to 0.1 |	Weak predictive Power |
| 0.1 to 0.3 | Medium predictive Power |
| 0.3 to 0.5 | Strong predictive Power |
| >0.5	     | Suspicious Predictive Power |<br>


**References:**<br>
1. [Data Exploration with Weight of Evidence and Information Value ](http://multithreaded.stitchfix.com/blog/2015/08/13/weight-of-evidence/)<br>
2. [WOE and IV](http://www.listendata.com/2015/03/weight-of-evidence-woe-and-information.html)<br>
3. [Introduction to WOE and IV](http://documentation.statsoft.com/STATISTICAHelp.aspx?path=WeightofEvidence/WeightofEvidenceWoEIntroductoryOverview)<br>
