
A directed [[Graph]] is considered to be Strongly Connected if for every pair of vertices `w` and `v` there is a pathway between them. That is to say, every single vertex can access every single other vertex.
A set of vertices make up a Strongly Connected Component if a [[Graph]] made up exclusively of those vertices would be Strongly Connected.
There's a simpler way to say that, but it makes enough sense.

It is possible to find all of the Strongly Connected Components within a [[Graph]] via an algorithm which runs in $O(n+m)$ time, if there are $n$ vertices and $m$ edges. This is the content of Lecture 19.

1. Perform DFS to create a "DFS Forest." Choose the starting vertices in any order, and keep track of all the finishing times.
2. Reverse all the edges in the graph.
3. Perform DFS a second time to create a second Forest. This time, begin your search with the vertices which had the largest finishing time.

A SCC Graph is a Graph which makes each Strongly Connected Component into a vertex, and then connects those vertices. An SCC Graph is directed and acyclic, meaning that any edge which you follow in the graph will not provide you with a way to return to your starting position.
This is because if you could return to your starting position, then the two components would actually be strongly connected together, and therefore they would need to merge into a single vertex.

Definitely look back to the images on Lecture 19's slides, it's not nearly as confusing as I'm making it sound.

Having access to finishing times makes Topological Sorting possible. Because finding SCCs involves finding all finishing times, SCC graphs are useful if you want to perform a topological sort.

For finding Strongly Connected Components, multiple different algorithms exist. The one focused on, and used for Lab10, is [[Kosaraju's Algorithm]].