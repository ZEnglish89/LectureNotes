
The means by which time-complexity(see previous courses) is analyzed.
If the time an algorithm takes to run can be represented as a function of n, where n is the number of inputs to the algorithm, then the time-complexity can be estimated as the term in the function with the highest-power of n.

This is similar to concepts in Calc II/Math022: With extremely high values of n, the highest-power term will "dominate" all others and control the way in which the function's outputs trend. As such, only the highest-power or fastest-growing term is considered in this analysis. Fastest-growing is important, because, for example, $n!$ will grow faster than $n^2$, even though the factorial isn't a higher power.

Differences in time-complexity will eventually be more significant than differences in computing power, with large enough n-values.
There exists a value of n such that a supercomputer running an inefficient algorithm will be outperformed by a human being running an efficient one, although it would have to be a ludicrously large value of n.

As implied, for smaller values of n, this is less useful. Algorithms which get excellent results on asymptotic analysis will often have constant or linear overheads which fade into insignificance with high n-values, but matter an awful lot at lower ones.

$O(n)$ is used for an upper bound: If, for some $c$ all $n$ greater than a certain value, $f(n)\leq c\cdot n$, then $f(n)$ is $O(n)$.

Note that you don't need to find "the right value" for c and n. You don't need to prove that the values you found are the lowest possible $n$ or $c$ in order for it to be valid, you just need to show that a value exists. You aren't trying to prove what $n$ or $c$ are, just that the equations grow at different rates.

$\Omega(n)$ is used for a lower bound

$\Theta(n)$ is used when the bound is both upper and lower. That is so say, if a function is both $O(n)$ and $\Omega(n)$, then it is $\Theta(n)$.

You can use algebra to discover whether or not an algorithm is or is not relative to a given function, and to solve for C: $$n^3+3n \leq c \cdot (n^3-n^2)$$
Solving the above equation for c will give you a value for which the inequality holds true, which will help you prove that $n^3 + 3n$ is $O(n^3-n^2)$.