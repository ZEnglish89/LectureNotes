
For performing [[Asymptotic Analysis]] and calculating Time Complexity on recursive algorithms, and solving [[Recurrence Relation]]s.

If $a\geq 1$, $b>1$, and $d$ are constants independent of $n$, and $T(n) = a \cdot T(n/b) + O(n^d)$, then $$T(n) = O(n^dlog(n))$$ if $a=b^d$, $$T(n)=O(n^d)$$ if $a<b^d$, or $$T(n)=O(n^{log_b(a)})$$
if $a>b^d$

Explanation:
a is the number of subproblems, the rate at which recursion splits.
b is the factor by which the input size shrinks with each level of recursion.
d: you must do $n^d$ work in order to create all subproblems and combine their solutions(I'm assuming this means that there's $n^d$ operations needed per level of recursion).

When $a<b^d$, the amount of work done at the top of the tree, the first layer of recursion, dominates the rest of the work. This splits the problem into very few subproblems, resulting in a "tall and skinny" tree structure. The work at the top is $n^d$, so the entire problem results in $O(n^d)$.

When $a>b^d$, the amount of work done on the bottom layer of recursion dominates the rest of the work. The problem is split into large quantities of subproblems, representing in a wide or "bushy" tree structure. The work is equal to $a$<sup>depth of tree</sup> resulting in $O(n^{log_b(a)})$. [[Karatsuba]] is an example of this case, though we haven't covered that algorithm yet.

When $a=b^d$, the branching balances out the work at each layer, resulting in approximately the same work at every level of recursion. This results in a smoothly scaling tree structure. Total work is equal to layers $\times$ work per layer: $log(n) \cdot O(n) = O(nlog(n))$.

These can all be derived from scratch, but that would be extremely difficult, using the Master Theorem is massively easier.

Honestly I should look this up on youtube or something. Also, I need the slides from 09/24 and 09/26 to be posted, they aren't up yet.

For [[Merge Sort]]: $a=2,b=2,d=1$, that means that the algorithm is $O(n^1log(n))$, which I believe is true.

At recursion level 0, if there is 1 problem, of size n, then the amount of work done at that level is $c \cdot c^d$(Did I copy that down right? Slides aren't available to check).
At recursion level 1, if there are $a$ problems, of size $n/b$, then the amount of work done at that level is $ac \cdot (n/b)^d$
At recursion level $t$, there are $a^t$ problems of size 

Total work is at most $$c\cdot n^d \cdot \Sigma ^{log_b(n)}_{t=o}(a/b^d)^t$$

The Master Theory is limited by the fact that the subproblems must be of equal complexity. For a more general way to handle complexity, look to the [[Substitution Method]].