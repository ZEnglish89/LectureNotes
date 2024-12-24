
This is a sorting algorithm which sorts values digit-by-digit.

If we want to sort $n$ integers with maximum size $M$ in base $r$, then the number of iterations of RadixSort is the same as the number of digits, base $r$, of an integer $x$ of max size $M$. That is $$d=(log_r(M))+1$$
Each iteration requires you to initialize $r$ buckets and place $n$ items into them, so $O(r+n)$.
So the total time is $$O(d\cdot(n+r))=O((log_r(M)+1)\cdot(n+r))$$
With small enough $M$ and $r$ this can simplify down to $O(n)$, which is pretty sweet. But of course, that requires small values, so it's only situationally helpful.