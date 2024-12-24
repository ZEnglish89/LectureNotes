An unordered arrangement of a [[Set]] of objects or elements.
Opposed to [[Permutation]]s by their unordered nature.

An r-combination is a subset of the set with r elements.

The number of r-combinations of a set with n elements is denoted by C(n,r).
(<sup>n</sup><sub>r</sub>) is sometimes used to mean the above, and is called a "binomial coefficient." The n and r should be directly above/below each other, subscripts and superscripts just don't work that way.

S={a,b,c,d}
{a,c,d} is a 3-combination of S.
{a,c,d} = {d,c,a} because combinations are all the same regardless of order. Much like how sets are equivalent if they contain the same elements regardless of order or repeated elements.
Do repeated elements matter for combinations?

C(n,r) = n!/((n-r)!r!)
I believe this means that there will be r! potential combinations that are redundant, i.e. are the same as other combinations but reordered.
By [[Product Rule]]: P(n,r) = C(n,r) * P(r,r)

So C(n,r) = P(n,r)/P(r,r)
By looking at the formulas on the [[Permutation]] page and doing some algebra, the above original equation can be derived relatively simply.

Additionally, C(n,r) = C(n,n-r)
This, again, can be found out with algebra.

On tests, Combination and Permutation problems will just have to be written out in their expanded multiplication form. They should not be left as factorial, but they do not necessarily need to be simplified all the way down, simply because some problems will be too large for that to work, even with calculators.
For example, if you get 52!/(5! * 47!) then multiply it out to 
(52 * 51 * 50 * 49 * 48)/(5 * 4 * 3 * 2 * 1), cancelling the factorials appropriately, but you do not have to multiply that final expression out.