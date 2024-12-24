
In single-variable calc, functions map from real numbers back onto real numbers

Vector-valued functions, or vector functions, are functions whose range is vectors, i.e. the output of the function is a [[Vector]], not a single value.

To begin, we are studying single-variable vector functions, which have one variable in their domain:
IR → IR<sup>n</sup>

Later in the course, we will expand to multiple variables.

Parametric formulas of [[Line]]s are considered Vector Functions in IR<sup>3</sup>

[[Space Curve]]s are common examples of Vector Functions in IR<sup>3</sup>

$\overrightarrow{r}$ = IR → IR<sup>3</sup>
t → $\overrightarrow{r}$(t) = <f(t), g(t), h(t)> = f(t)$\hat{i}$ + g(t)$\hat{j}$ + h(t)$\hat{k}$
This space curve represents the position of a particle at a time t, where it is moving in all three dimensions.

Vector Functions can have a Domain defined via set notation: $\overrightarrow{r}$ : D c IR → IR<sup>3</sup>

This domain is defined by taking a limit of each component function.
When taking the limit of a vector function, you take the limits of f(t), g(t), and h(t) individually.
If any of the three component limits do not exist, then the limit of the function as a whole does not exist.

A Vector Function is continuous on the domain D if all three component functions are individually continuous on D.
A function is considered to be continuous on a point if: it if defined at that point, the limit of it at that point exists, and the limit is equal to the actual value.

$\overrightarrow{r}$(t) = < t<sup>2</sup> +5, $\sqrt{t+2}$ , (1-e<sup>t</sup>/t) >
f(t) has a domain of all real numbers
g(t) has a domain of all real numbers >=-2
h(t) has a domain of all real numbers besides 0.
Therefore, for $\overrightarrow{r}$(t), D = (inclusive)-2,0) U (0,$\infty$)
The Vector Function is continuous along its entire domain. This will not always be true, discontinuities within the domain will happen.

The Curvature of a Vector Function r(t) can be solved for as follows:$$\kappa = (||r'(t) \times r''(t)||)/||r'(t)||^3$$
