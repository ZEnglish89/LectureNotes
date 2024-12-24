
If you take n IID samples from a distribution with mean $\mu$ and variance $\sigma^2$, and $\bar{x}_n$ is the average of n sample, then is will have mean $\mu$ and variance $\sigma^2/n$.

The distribution of $\bar{x_n}$ converges to a Normal distribution, specifically N(0,1) as $n → \infty$.

This means that the normal distribution can then be used as an approximation.
Make an assumption about the type of distribution being witnessed, and collect data to compare against it.
The number of standard deviations that your measurements are away from the theoretical data is equal to:$$Z = (\bar{x_n}-\mu)/(\sigma / \sqrt{n})$$
You can then qualitatively and contextually decide if that number of standard deviations of difference is acceptable. The more standard deviations, the less likely that the assumption was accurate.

The above value is a z-score, used in calculating [[Confidence Interval]]s.