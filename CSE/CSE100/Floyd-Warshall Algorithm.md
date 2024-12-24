
An example of the [[Dynamic Programming]] paradigm, used to solve the "All-Pairs Shortest Paths" problem, or APSP.
The problem calls for finding the shortest path from $u$ to $v$ for ALL pairs $(u,v)$ within a Directed and Weighted [[Graph]].

The naive solution for this problem is to use either [[Dijkstra's Algorithm]] or the [[Bellman-Ford Algorithm]] $n$ times, using each vertex as the root.

For Bellman-Ford, this naive solution is $O(n^2m)$, and the value of $m$ could potentially bring it as high as $O(n^4)$ so really undesirable and we want to do better.

Floyd-Warshall works by treating every node as an intermediate node along a path, and constantly updating a list of known path lengths.
It's not quite making sense in my head, but I'll get some pseudocode down and it'll be fine.

This algorithm runs in $O(n^3)$ time, which may be easily seen via the three nested loops, making it more efficient than Bellman-Ford.

Floyd-Warshall does not work if the graph contains negative cycles, but it is also capable of detecting them. If there exists some node $u$ where $D_n[u][u]<0$, then a negative cycle must exist.

Pseudocode:
```
Floyd-Warshall():
	Initialize nxn arrays D_k for k=0 to k=n
		D_k[u][u]=0 for all u and all k
		D_k[u][v] = \infty for all u!=v and all k
		D_0[u][v] = weight(u,v) for all (u,v) with an edge between them
	for int k=1;k<=n;k++:
		for all u:
			for all v:
				D^k[u][v] = min(D_{k-1}[u][v], D_{k-1}[u][k]+D_{k-1}[k][v])
	return D_n
	//D_n[u][v] will be the shortest distance between u and v for all pairs.
```
The path containing at most $k$ nodes will either be equal to the shortest path containing at most $k-1$ nodes or it will be the sum of the shortest path from $u$ to $k$ and the shortest path from $k$ to $v$.