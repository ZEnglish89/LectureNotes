
Another example of the [[Dynamic Programming]] paradigm.

If you have a list of items "for sale," each with an associated cost and value, and you have a budget for maximum cost, how do you maximize the value?

In the context presented in Lecture 23, each item has a "weight" and you have a backpack or knapsack with finite capacity, and you want to fill it with maximum value.

I don't completely understand how this one works, I get the concept but honestly I'm taking these notes while very tired and multitasking a little so the specifics are not clicking. I copied down the pseudocode as usual.

There are two versions of the problem: The "unbounded" version, where you can have infinite copies of each individual item, and the "bounded" version, where there are a limited number of each one, most commonly just one.

It can be solved dynamically by solving the problem for smaller budgets, then expanding to larger ones.

The algorithms for each version of the problem are different.

Unbounded can be solved in $O(nW)$ for $n$ items and a budget of $W$.
Pseudocode:
```
UnboundedKnapsack(W,n,weights,values):
	K[0]=0 //K[x] represents the optimal value with budget x.
	Items[0]=0;
		for(int x=1;x<=W;x++):
			K[x]=0;
			for(int i=1;i<=n;i++):
				if w_1<=x:
					K[x] = max(K[x],K[x-w_1]+v_i)
					if K[x] was updated:
						Items[x] = Items[x-w_i] U item i//Not really sure what's  //up with the set notation there.
	Return Items[W]
```

The bounded version(we focus on the one where each item must be unique) is more complicated. This is because each sub-problem must keep track of which items have already been used to avoid repeats, while the unbounded version just doesn't care.
For the purpose of this problem, `K[x][j]` represents the optimal solution with a budget of `x` and using the first `j` items.
The optimal solution for `j` items of course either will or won't use the `j`th item. If it does not, then the solution for `j-1` items is the same.
If it does, then the solution for `j-1` items will be the same but missing that `j`th item. I think.

This apparently also runs in $O(nW)$.

Pseudocode:
```
Zero-One-Knapsack(W,n,w,v):
	K[x][0] = 0 for all x=0,...,W
	K[0][i] = 0 for all i=0,...,n
	for(int x=1;x<=W;x++):
		for(int j=1;j<=n;j++):
			K[x][j] = K[x][j-1] //the term being assigned is the value for Case 1
			if(w_j<=x):
				K[x][j] = max(K[x][j],K[x-w_j][j-1]+v_j) //the right term is Case 2
	return K[W][n]
```
