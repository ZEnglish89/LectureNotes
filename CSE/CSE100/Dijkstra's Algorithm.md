
This is an algorithm to find the minimum distances of all nodes from a given node within a Directed and Weighted [[Graph]]. It starts at a given node and makes distance estimates to all of its direct neighbors. It then travels to the closest neighbor and updates the distance estimates for all of that node's neighbors, repeating the process until every node has been travelled to.

It is similar in concept to Depth-First-Search, but it decides which neighbor to travel to based on the distance estimates, and all estimates are made relative to the original root node, not the current node.

Its effectiveness is data-structure dependent.
With an array: $O(n^2)$
With a [[Red-Black Tree]]: $O(n+m)log(n))$ which is better if the [[Graph]] is "sparse," if $m$ is much smaller than $n^2$.
Using a Fibonacci Heap, whatever that is, you get $O(nlog(n)+m)$ as an "Amortized Time" estimate, which means that not all of the components within it will require the same time complexity in each call.

This algorithm is used in practice, but it has some limitations:
1. The edge weights must be non-negative.
2. If the weights change, the entire algorithm must be re-run from the beginning.

Pseudocode:
```
	Dijkstra(G,s):
	Set all vertices to not-sure //or unknown or whatever. Give them a bool.
	d[v] = \infty for all v in V //d is the Distance, v is a vertex,
	//V is the list of all Verteces.
	d[s] = 0 //Distance to yourself is 0.
	While there are not-sure nodes: //Maybe create a numnotsure?
		Pick the not-sure node u with the smallest d[u]
		for v in neighbors:
			d[v] = min(d[v],d[u]+edgeWeight(u,v)) //The distance for v either
			//remains the same, or is equal to the distance for u plus the 
			//distance between u and v.
		Mark u as sure.
// now d(s,v) = d[v] //Once the process is complete, d[v] will contain the correct
//distance between v and s.
```