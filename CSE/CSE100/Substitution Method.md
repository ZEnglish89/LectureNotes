
Covered in Lecture #7, on 10/01. May be useful to revisit those notes, the entire induction process is laid out there(Though I'm not quite getting it yet).

1. Repeatedly expand and simplify the [[Recurrence Relation]] to identify a pattern. Once you believe you have identified a pattern, guess that that is your solution. Plug in your solution and simplify to get a guess at the Time Complexity. (You can guess via patterns you've noticed in the [[Master Theorem]], but it won't always be applicable.)
2. Prove that your solution works, using Induction(See CSE015).
If step 2 works, then you're done! Otherwise, just start again.


Example: $$T(n) = 2 \cdot T(n/2) +n$$
with $T(1) = 1$.
**Step One:**
Lecture notes moved on before I could write it, not accessible until they're posted.

**Step Two:**
Inductive Hypothesis: $$T(j) = j(log(j)+1$$
for all $1\leq j \leq n$.
Base Case $(n=1)$:$$T(1)=1=1\cdot(log(1)+1)$$
Inductive Step: Assume the Inductive Hypothesis for $n=k-1$: Suppose that $T(j)=j(log(j)+1)$ for all $1\leq j\leq k-1$.
By definition, $$T(k)=2\cdot T(k/2)+k$$
then by induction $$T(k)=2\cdot(k/2(log(k/2)+1))+k$$
then by simplifying $$T(k)=k(log(k)+1)$$
Therefore the Hypothesis holds for $n=k$.

Example:$$T(n) = 2\cdot T(n/2)+32\cdot n$$
with $T(2)=2$
The [[Master Theorem]] tells us that this is $O(nlog(n))$, so that's something to go off of/check my work.

**Step One:**
Expand to $$T(n) = 2\cdot(2\cdot T(n/4)+32\cdot n/2)+32\cdot n$$
then simplify to $$T(n) = 4\cdot T(n/4)+64\cdot n$$
and expand again to $$T(n)=4\cdot(2\cdot T(n/8)+32\cdot n/4)+64\cdot n$$
and simplify to $$T(n)=8\cdot T(n/8)+96\cdot n$$
I'm clearly not seeing the patterns I'm supposed to be seeing...

**Step Two:**
Inductive Hypothesis: $$T(j)\leq C\cdot jlog(j)$$
for $2\leq j\leq n$.
Base Case: $(n=2)$:$$T(2)=2 \leq C \cdot 2log(2)$$
Inductive Step: This works as long as $C\geq 32$ so choose $C \geq 32$
The rest of this is in the slides, I fell behind on the typing trying to perform step one on my own.