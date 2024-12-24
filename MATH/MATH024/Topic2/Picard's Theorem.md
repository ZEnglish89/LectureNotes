
"Picard's Existence & Uniqueness Theorem"

Existence Theorems give us *at least one* of some property. In the case of [[Differential Equation]]s, that property is a [[Solution]].
This is not the same as the colloquial usage of "Exists" because this is referring to there being at least one of a type of something, not that a concrete thing is present.

Uniqueness Theorems give us *at most one* of some property: Just zero or one.
Again, not the same as colloquial "Unique" because this allows for there being zero as well.

These overlap at exactly one [[Solution]]: If both theorems are true, then you've found the one solution that is present, which is the ideal case.

The full Theorem:
GIven $y' = f(t,y)$, $y(t_0)=y_0$, which is an [[Initial Value Problem]]:

Existence: Suppose the function $f(t,y)$ is continuous on the region $$R={(t,y) | a<t<b , c<y<d}$$ then $\exists$ a number h>0 such that the IVP above has *at least* one [[Solution]] for $$t \in (t_0-h,t_0+h)$$
Existence is required before Uniqueness can be proven.

Uniqueness: If furthermore $\partial f/\partial y$ is also continuous on R, then there is *at most* one solution.