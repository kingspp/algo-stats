#Cohen's Kappa

**What is it?**<br>
Cohen's kappa coefficient is a statistic which measures inter-rater agreement for qualitative (categorical) items. It is generally thought to be a more robust measure than simple percent agreement calculation, since κ takes into account the possibility of the agreement occurring by chance.

**What is inter-rater aggreement?**<br>
In statistics, inter-rater reliability, inter-rater agreement, or concordance is the degree of agreement among raters. It gives a score of how much homogeneity, or consensus, there is in the ratings

**Example:**<br>

| Actual Value  | Predicted Value |
| ------------- | ------------- |
| 0 | 0 |
| 0 | 0 |
| 1 | 0 |
| 0 | 1 |
| 1 | 1 |
| 1 | 0 |
| 1 | 1 |
| 1 | 1 |
| 1 | 1 |
| 0 | 0 |

**Cohen's Matrix**<br>

| Actual / Predicted | 0 (A) | 1 (A) | Total
| ------------- | ------------- | ------------- | ------------- |
| 0 (P) | 3  | 2  | **5**
| 1 (P) | 1  | 4  | **5**
| Total | **4**  | **6**  | <i>10</i>
<br>
```
P(a) [ Observed Proportionate Agreement ] = Sum of Cohen's Matrix Diagonals / Total(Predicted + Actual) = (3+4) / 10 = 0.7<br>
p(b) [ Probability of Random Agreement ] = ( (Total of Actual 0's * Total of Predicted 0's) + (Total of Actual 1's Total of Predicted 0's * Total of Predicted 1's ) ) / Total = ((4*5) + (6*5)) / 10 = 0.5 <br>
```
**Cohen's Kappa** = ( P(a) - P(b) ) / ( 1 - P(b) ) = ( 0.7 - 0.5 ) / ( 1 - 0.5 ) = 0.2/0.5 = 0.4

**Kappa Coefficients Results**<br>
k >= 0.5 : Moderate Aggrement <br>
k >= 0.7 : Good Aggrement<br>
k >= 0.8 : Excellent Aggement<br>

**Kappa Sensitivity :** True Positives<br>
**Kappa Specificity :** False Negetives<br>
