
Q1. Think Stats Chapter 2 Exercise 4 (effect size of Cohen's d)

Cohen's D is an example of effect size. Other examples of effect size are: correlation between two variables, mean difference, regression coefficients and standardized test statistics such as: t, Z, F, etc. In this example, you will compute Cohen's D to quantify (or measure) the difference between two groups of data.

You will see effect size again and again in results of algorithms that are run in data science. For instance, in the bootcamp, when you run a regression analysis, you will recognize the t-statistic as an example of effect size.

***

Exercise 2.4 Using the variable totalwgt_lb, investigate whether first ba-
bies are lighter or heavier than others. Compute Cohen’s d to quantify the
difference between the groups. How does it compare to the difference in
pregnancy length?

***

```python
import numpy as np

import nsfg
import first
import thinkstats2

preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]

firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

print('firsts mean: ', firsts.totalwgt_lb.mean())
print('others mean: ', others.totalwgt_lb.mean())

print("Cohen's d weight: ", thinkstats2.CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb))
print("Cohen's d preg length: ", thinkstats2.CohenEffectSize(firsts.prglngth, others.prglngth))
```

    firsts mean:  7.201094430437772
    others mean:  7.325855614973262
    Cohen's d weight:  -0.088672927072602
    Cohen's d preg length:  0.028879044654449883



```python

```
