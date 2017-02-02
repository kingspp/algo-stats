#Kullback–Leibler divergence


**What is Probability Distribution?**<br>
A mathematical function that can be thought of as providing the probability of occurance of different possible outcomes.<br>
**Example:** Toss of a coin twice<br>

| Number of Heads  | Probability |
| ------------- | ------------- |
| 0  | 0.25  |
| 1  | 0.5   |
| 2  | 0.25  |


**What is KL Divergence?**<br>
It is a non-symmetric measure of difference between two probability distributions p(x) and q(x) over a same variable x. It is used to quantify 
the information lost when q(x) is used to approximate p(x)

```
KLD = ∑ p(x) * ( ln p(x)/ q(x) )
```
**Example**:<br>

| Age  | Propensity to buy a Motorcycle | Segment |
| ------------- | ------------- | ------------- |
| 23 | 1 | 1 |
| 42 | 1 | 4 |
| 54 | 0 | 3 |
| 32 | 1 | 2 |
| 63 | 0 | 5 |
| 56 | 0 | 1 |
| 24 | 1 | 2 |
| 65 | 0 | 3 |
| 54 | 0 | 2 |
| 63 | 0 | 1 |
| 53 | 1 | 4 |
| 57 | 0 | 3 |
| 61 | 1 | 5 |
| 54 | 1 | 2 |
| 64 | 1 | 3 |
| 24 | 0 | 4 |
| 33 | 0 | 2 |
| 45 | 0 | 1 |
| 34 | 1 | 1 |
| 43 | 0 | 2 |
| 63 | 1 | 2 |
| 23 | 1 | 3 |
| 34 | 1 | 3 |
| 42 | 0 | 3 |
| 33 | 1 | 4 |
| 45 | 1 | 4 |
| 62 | 0 | 4 |
| 23 | 1 | 5 |
| 37 | 0 | 5 |
| 46 | 0 | 5 |
| 58 | 1 | 5 |

**KLD Matrix:**<br>

| Row Labels (Clusters)/Column Labels (Count) | 20-29 |	30-39 |	40-49	 | 50-59 | 60-69 | Grand Total |
| -------------------------|-------|--------|--------| -------| -------| -------| 
| **1** |	1 |	1 |	1 | 1 |	1 | **5** |
| **2** |	1 |	2 |	1 |	2 |	1 |	**7** |
| **3** |	1 |	1 |	1 |	2 |	2 |	**7** |
| **4** |	1 |	1 |	2 |	1 |	1 |	**6** |
| **5**	| 1	| 1 |	1 |	1 |	2 |	**6** |
| **Grand Total** |	**5** |	**6** |	**6** |	**7** |	**7** |	**31** |

**References**:<br>
1. [Probability Distribution](http://stattrek.com/probability-distributions/probability-distribution.aspx)<br>
2. [Probability Distribution Wiki](https://en.wikipedia.org/wiki/Probability_distribution)<br>
3. [KLD Layman's Explanation](https://www.quora.com/What-is-a-good-laymans-explanation-for-the-Kullback-Leibler-Divergence)<br>
4. [Kullback-Leibler Divergence](http://web.engr.illinois.edu/~hanj/cs412/bk3/KL-divergence.pdf)<br>
5. [KL Divergence Wiki](https://en.wikipedia.org/wiki/Kullback%E2%80%93Leibler_divergence)<br>
