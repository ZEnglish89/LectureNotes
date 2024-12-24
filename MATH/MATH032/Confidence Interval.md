
Formula for a confidence interval of a given percent: $$(z \times \sigma)/\sqrt{n}$$where $z$ is the z-score that corresponds to the percentage which the confidence interval is meant to be for.
The confidence interval will then be $\bar{x}_n +-$ the result of the above equation. 

If you know the variance/standard deviation and the distribution is normal, use a z-score. If you only have a sample variance/standard deviation, use a t-score(below). If the distribution is not known to be normal, you can't make a Confidence Interval at all.

Z-Score table is on page 434 of the textbook.

![[Pasted image 20240320124910.png]]


If the standard deviation is known: Use the above equation, and relate it to the $N(0,1)$ distribution
Z-Score, the above table.

If the standard deviation is NOT known, and we only have the sample standard deviation, use the above equation with the sample standard deviation in place of the real one, and relate it to the $t(n-1)$ distribution where n is the number of samples(The value $n-1$ is referred to as the number of "degrees of freedom").
T-Score, the below table.

A t-score will be roughly 10% larger to account for additional error caused by not knowing an ideal $\sigma$.
![[Pasted image 20240322125531.png]]

For a one-sided confidence interval: Use the same equation as above, but instead of +-, use only + or only -, and replace the other part of the interval with $+-\infty$. Also, for the z/t-score, remember that the probability isn't shared between two tails, but instead is concentrated within a single tail; meaning that you're using a z/t-score for double the normal probability.


This is all assuming that the situation is based on the Normal distribution. Not many things in actuality are like that, but thanks to the [[Central Limit Theorem]] we can assume that things with enough samples will end up being *roughly* based on Normal. The note about the CLT also contains the equation for finding a z-score.