
Another option for dealing with Weighted [[Graph]]s.

This is developed as an alternative for [[Dijkstra's Algorithm]], so when analyzing it it's useful to first understand that algorithm and how it functions.

Bellman-Ford is slower than [[Dijkstra's Algorithm]], but unlike that algorithm it can handle [[Graph]]s with negative weights and is more flexible if the weights are changed.

The basic idea is to update all of the distance estimates simultaneously, rather than choosing the neighbor with the smallest estimate and proceeding from there.

It works with negative weights, but it breaks with negative cycles, although it can detect their presence. By extending one iteration past the original loop, if the values change then a negative cycle must be present.

It runs in $O(mn)$.

Bellman-Ford is the first example of [[Dynamic Programming]] covered in this class.
Pseudocode:
```
Bellman-Ford(G,s):
	d[v] = \infty for all v in V //All distance estimates start at infinity and
	//are reduced from there.
	d[s] = 0 //The starting node is 0 distance from itself.
	for int i=0; i<n; i++: //Calculates the cost of a path with at most i edges.
		for u in V: //loop through each vertex
			for v in u.neighbors:
				d[v] = d[v] = min(d[v],d[u]+edgeWeight(u,v))
	if d_{n-1} != d_n:
		A negative cycle is present, scrap everything.
```

The lecture also gives this more complicated pseudocode which is less space-efficient but may be easier to implement in a real programming language:
```
Bellman-Ford(G,s):
	Initialize arrays d_0,...,d_{n-1} of length n to all be \infty
	d_0[s]=0
	for int i=0;i<n-1;i++:
		for u in V:
			for v in u.outNeighbors:
				d_{i+1} = min(d_i[v],d_{i+1}[v],d_i[u]+w(u,v))
	if d_{n-1} != d_{n-2}:
		A negative cycle is present, scrap everything.
	//now dist(s,v) = d_{n-1}[v] for all v in V
```

Lecture 21 messes around with this pseudocode a bit further, but I don't think anything else is particularly relevant or helpful to understanding the algorithm.