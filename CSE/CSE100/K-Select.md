
$SELECT(A,k)$ means to return the k'th smallest element of A.
For $A = [7,4,3,8,1,5,9,14]$, $$SELECT(A,1)=1$$
$$SELECT(A,2)=3$$
$$SELECT(A,3)=4$$
$$SELECT(A,8)=14$$

As a general rule, $$SELECT(A,1)=MIN(A)$$$$SELECT(A,n/2)=MEDIAN(A)$$and $$SELECT(A,n)=MAX(A)$$
This problem can be trivialized by sorting the array first, because then the $k$'th smallest element will always be at position $A[k-1]$. However, it of course must be sorted, which takes time. Professor Lu uses [[Merge Sort]] as an example, so that solves the problem in $O(nlog(n))$.

Supposedly, $O(n)$ is possible.
For the case $SELECT(A,1)$ the trivial solution is $O(n)$, just scan the array once and return the minimum.
The same is true for $SELECT(A,n)$, just do the scan and return the maximum.

$SELECT(A,2)$ can be solved in $O(n)$ as well, by adding one additional variable to the algorithm that finds the minimum: It just tracks the *previous* minimum before the actual minimum is found.

You could technically expand this out, but as $k$ increases it ends up being more along the lines of [[Insertion Sort]] in complexity.

This problem can be solved in $O(n)$ using a [[Divide and Conquer]] framework:
The steps Professor Lu is describing appear to match [[Quick Sort]]:

1. Pick a pivot
2. Partition the array into "Bigger than the Pivot($R[]$)" and "Lesser than the Pivot($L[]$)." You don't need to sort the two halves.
3. If you're looking for the $k$'th smallest item and $k$ is one greater than $length(L)$, then your Pivot is the item you're looking for.
4. If $k\leq length(L)$ then you can use recursion to do this again with $SELECT(L,k)$
5. If $k>length(L)+1$ then you can use recursion and do this again with $SELECT(R,k-(length(L)+1))$
Note that if you find that your value is on the left, you can ignore the right from that point forward, and vice versa. That allows this method to be a more efficient solution than sorting the entire array, cutting down the number of subproblems you have to handle.


The running time of this whole thing can be described with a [[Recurrence Relation]]: $$T(n) = O(n)$$
if $Len(L) = k-1$,$$T(n) = T(Len(L))+O(n)$$
if $Len(L)>k-1$, or $$T(n) = T(Len(R))+O(n)$$
if $Len(L) < k-1$

$Len(L)$ and $Len(R)$ are dependent on the Pivot we select. Ergo, the quality of this algorithm is highly dependent on how effectively we select our Pivot.
The ideal pivot arises when $Len(L) = k-1$, i.e. when we split our input precisely in half. That maximizes our odds of getting the $O(n)$ scenario. If we assume that we split the input in half consistently, then we can treat this whole thing as: $$T(n) \leq T(n/2) +O(n)$$
Which can then have the [[Master Theorem]] used on it!
However, that is a strong assumption, so we should avoid doing that, and therefore avoid using Master's.

The reason why we can't just choose a pivot that will always split the input perfectly in half is because we don't have the array sorted in advance, so finding that pivot represents its own problem to be solved.

As a replacement, we can recursively find the median of different subgroups of the input, and therefore get something approximating the overall median. It doesn't give us our ideal pivot every time, but it does give us something approximating that pivot with *vastly* fewer resources consumed than any technique that would give us greater precision.
Finding the median is effectively $SELECT(A,n/2)$, so we can't just solve that. If we could do that easily, we wouldn't need to do any of this nonsense at all, we'd just solve it.
However, it's not impractical to split $A$ into multiple subgroups $B$ and solve $SELECT(B,m/2)$ where $m=Len(B)$. Once all subgroups have had their medians found, we can arrange those medians into an array and find the median of them, which will then approximate our ideal pivot.

As such, the whole Algorithm combines to give this pseudocode:
```
SELECT(A,p=k):
	if len(A)<=50
		A=MergeSort(A)
		Return A[k]
	p=CHOOSEPIVOT(A)
	L,A[p],R=PARTITION(A,p)
	if len(L) = k-1
		return A[p]
	else if len(L)>k-1
		return SELECT(L,k)
	else if len(L)<k-1
		return SELECT(R,k-len(L)-1)

Partition(A,p):
	L = new array
	R = new array
	for i=1,...,n:
		if i==p:
			continue
		else if A[i] <=A[p]:
			L.append(A[i])
		else if A[i]>A[p]:
			R.append(A[i])
	return L,A[p],R

CHOOSEPIVOT(A):
	Split A into m=n/5 groups, of size <=5 each
	for i=1...m:
		find median of m[i]
		call it p[i]
	p=SELECT(p[1],p[2],etc, m/2)
	return p
```
The ChoosePivot is a bit of a mess. I'll have to find a better way to write that. But still, it could be worse.
Note that this does have a lot in common with [[Quick Sort]].