
The process of reducing a collection of data to a single line, in order to make sense of it more clearly and easily. This loses you information in exchange for giving an easier to understand conclusion.
The goal for Linear Regression is to find the best possible line to represent your data.

This is not useful for ALL data collections, some are better suited to linear regression than others.
Also see [[Quadratic Regression]], because some datasets map nicely onto parabolas.

In order to fit a linear model to data, we need to include: $$y_i = \alpha + \beta x_i + r_r$$
where $\alpha$ is the intercept, $\beta$ is the slope, and $r_i$ is the noise or error for a specific data point, also called the Residual.

There are MANY types of regression and many methods for determining a regression's effectiveness. Regression is an entire field in its own right. Anything contained in my notes here is just a small chunk of what exists in the field.

**Least Squares Regression:**
This is one possible method of linear regression. It is NOT the only one.
Achieved by picking a line which minimizes the sum of the squares of the residuals, i.e. minimizing the following equation: $$E(\alpha,\beta) = \Sigma^n_{i=1}(y_i-\alpha - \beta x_i)^2$$
Therefore we need the partial derivatives $\partial E/\partial \alpha = 0$ and $\partial E /\partial \beta = 0$ and we get a linear system in two variables.

Take the sum of the $\alpha$ derivatives and that of the $\beta$ derivatives, then set those two sums equal to 0 and solve for $\alpha$ and $\beta$ using substitution.
Sometime before the exam, I should go through and practice using this method. The below equations are awesome but I need to know how they're derived.

To do this more simply, without as much calculus: $$\beta = (E[XY] - E[X]E[Y])/(E[X^2]-E[X]^2)$$
or, using [[Covariance]] and [[Variance]]: $$\beta = Cov(X,Y)/Var(x)$$ and $$\alpha = E[Y]-\beta E[X]$$
or, with Sigma notation: $$\alpha = (1/n \cdot \Sigma y_i) - (\beta \cdot 1/n \cdot \Sigma x_i)$$
Also if my brain isn't working right, remember that $E[X] = \bar{X}$ and so on, that makes it slightly more understandable.

The final equation is of the form: $y=\beta x + \alpha$

When determining the quality of a linear fit:
See if the residuals are biased in one direction or another; that would signify a bias within your line. The sum of the residuals(not the squares, not the absolute values, just the sum of the residuals) should be 0 in order to signify no bias.

$R^2 = 1 - (\Sigma_i(y_i - f_i(x_i))^2)/(\Sigma_i(y_i-E[Y])^2)$, which is the same as
1 - ((The deviation from the model) / (The natural variation of the data)).
This $R^2$ value varies between 0 and 1, with 1 representing a perfect fit and 0 representing a completely worthless fit.