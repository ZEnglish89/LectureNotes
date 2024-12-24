A type of Binary Search Tree(CSE 030) which uses a proxy to balance itself, allowing it to remain balanced and binary.

It obeys the following:
1. Every node is colored red or black
2. The root node is black.
3. NIL/null Children count as black.
4. Children of red nodes are black nodes.
5. For all nodes x: All paths from X to NILs have the same number of black nodes on them.

These five properties guarantee that the black nodes will be balanced, and property 4 ensures that the red nodes will be "spread out" so to speak, so that they cannot have a significant effect on the overall balance of the tree.

If you define $bh(x)$ to be the number of black nodes in any path from x to NIL, not counting $x$ or the NIL space:

If $bh(x)=b$, and $y$ is a child of $x$, then:
1. $bh(y)=b$ if $y$ is red.
2. $bh(y)=b-1$ if $y$ is black.

The number of internal nodes at $x$ can be derived to be$\geq 2^{bh(x)}-1$. Proof of that is on the lecture slides from 10/31-2024.

The height $h$ of a Red-Black tree with $n$ non-NIL nodes is at most $2log(n+1)$. Proof below, based on the above statement regarding $bh(x)$.
1. $n \geq 2^b-1$
2. $n\geq 2^{h/2}-1$
3. $h\leq 2log(n+1)$

Because the height is strictly capped by the number of nodes like this, the tree literally cannot become too unbalanced: A tree is at its most unbalanced when its height is equal to $n$ and it's at its most balanced when the height is $log(n)$. I believe $log(n)$ is correct there, but regardless I think the conceptual understanding is there.

Insert and Delete operation on a RB tree can be completed in $O(log(n))$ time.
First you must search to find the correct location to insert or delete a node, and then you must complete rotations of the tree and recolorings of nodes in order to preserve the five properties.

These processes are beyond the scope of the course for the most part, but they are covered within the slides for 10/31-2024 and it's pretty interesting stuff.