
Q4. Think Stats Chapter 5 Exercise 1 (normal distribution of blue men)
This is a classic example of hypothesis testing using the normal distribution. The effect size used here is the Z-statistic.

****

Exercise 5.1 In the BRFSS (see Section 5.4), the distribution of heights is
roughly normal with parameters μ = 178 cm and σ = 7.7 cm for men, and
μ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and
6’1” (see http://bluemancasting.com). What percentage of the U.S. male
population is in this range? Hint: use scipy.stats.norm.cdf.

****


```python
import scipy.stats

dist = scipy.stats.norm(loc=178, scale=7.7)

low = dist.cdf(177.8)
high = dist.cdf(185.4)

high-low
```




    0.3420946829459531



34.2% of the U.S. male population is in this range
