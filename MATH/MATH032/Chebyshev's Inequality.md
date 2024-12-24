Relevant to [[Model]]s and [[Sampling]].
If X is a random variable with mean $\mu$ and variance $\sigma^2$, then: 
$$P(|X-\mu|>=k \cdot \sigma) <= 1/k^2$$
In plain English: The chance that X takes a value more than k standard deviations from its mean is less than or equal to $1/k^2$.

Alternative way of writing the equation: $$P(|X-\mu|>= a) <= \sigma^2/a^2$$
This is true for ALL distributions, it does not change based on which distribution X comes from.

However, even though this rule holds, the specifics can vary. For certain distributions, the value is equal to $1/k^2$, for others it is less than, and the specific value for the less than distributions varies.

Use this when you're given mean and variance, and asked how "weird" or "unusual" a certain occurrence is.
When dealing with averages, make use of the [[Central Limit Theorem]] to modify the variance. When dealing with exceptionally large sample sizes, take CLT all the way and use a Z-score.