Big-O notation is used to evaluate/estimate the complexity of [[Algorithm]]s and functions; estimating how much their complexity grows relative to the complexity of their input.

Used in Programming, O(1) O(n) O(n<sup>2</sup>) and so on.

For any given function f(x), there is another function g(x) where f(x) is O(g(x)). This means that f(x) has time complexity which can be approximated by g(x), if you neglect constants and things of that nature.

f(x) is O(g(x)) if there is some constant k and some constant C where f(x)<=Cg(x) when x>k.

This generally just means that g(x) is of a higher degree than f(x), or, to use a calculus term, g(x) dominates f(x) as x approaches infinity.
Important note^ g(x) does not have to dominate f(x). g(x) simply has to be not dominated by f(x), meaning that g(x) simply has to be *of the same degree or higher* than f(x). 
For example, f(x)=x<sup>2</sup>+x+2 is O(g(x)) when g(x)=x<sup>2</sup> even though g(x) does not dominate f(x).
Because of this, g(x) is also O(f(x)) in this situation. Any two functions that are both O(each other) are referred to as being of the "same order."

If there exists some pair of k and C where f(x) is O(g(x)), then there must be infinitely many pairs(because all k<sup>'</sup>>k and all C<sup>'</sup>>C will also satisfy the same conditions).

O(g(x)) really represents a set of functions, that being the set of all functions which are of its complexity or lesser. Thus, "f(x) is O(g(x))" really means that f(x) is a member of the set O(g(x)).

