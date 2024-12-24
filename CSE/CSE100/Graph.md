
An Undirected Graph has Vertices and Edges.
$V$ is the set of vertices, $E$ is the set of edges, and formally, a graph is $G=(V,E)$
Unfortunately, graphs are much easier to represent graphically(haha) than they are textually. Fortunately, there are plenty of examples on Lecture 17, and also Obsidian's graph view is EXACTLY what's being talked about here.

The Degree of a vertex is the number of edges which connect to it, and a vertex's Neighbors are the other vertices which those edges connect it to.

A Directed Graph still has vertices and edges, where $V$ is  the vertices and $E$ is the set of edges, but those edges are directed: They don't just connect two vertices, they have a defined origin and destination.
Directed Graphs are still formally $G=(V,E)$

Vertices in directed graphs now have an in-degree, the number of edges which have that vertex as a destination, and an out-degree, the number of edges which have that vertex as an origin.
Vertices also have incoming and outgoing neighbors, which follow the same rules as in-and-out-degrees.

Vertices are nodes, which may hold information, and edges show connections or relationships between them.

Graphs may be represented by an adjacency matrix, see the below screenshot, it's pretty self-explanatory:![[Pasted image 20241104193454.png]]

With directed graphs, rows can represent origins and columns can represent destinations.

Another option is adjacency lists, where each element is a linked list and the elements of that linked list are all of its neighbors.

On a given Graph, we want to be able to do two operations:
1. Edge Membership: Tell if edge $e\in E$
2. Neighbor Query: Retrieve all of the neighbors of vertex $v$.

For a Graph with $n$ vertices and $m$ edges:
A [[Matrix]] will give Edge Membership in $O(1)$, Neighbor Query in $O(n)$, and require $O(n^2)$ space.

A List will give Edge Membership for edge $e=[v,w]$ in $O(deg(v))$ or $O(deg(w))$, Neighbor Query on vertex $v$ in $O(deg(v))$, and require $O(n+m)$ space.

When searching through a graph, you have a couple different options:
1. Depth First Search or DFS

A Depth First Search will start at a certain vertex, and move to one of its neighbors which has not been visited yet. If all of its neighbors have been visited, the search will instead move to one of the neighbors which itself has unvisited neighbors. If all of that vertex's neighbors have already been visited, the search will take a step back and go to the next one. The search is completed when the current vertex has no neighbors which have unvisited neighbors.
The pseudocode honestly is easier to understand than a verbal explanation for this one.

Pseudocode of Depth First Search:
```
DFS(w,currentTime):
	w.startTimes = currentTime
	currentTime++
	Mark w as InProgress
	for v in w.neighbors:
		if v is UnVisited:
			currentTime=DFS(v,currentTime)
			currentTime++
	w.finishTime=currentTime
	mark w as AllDone
	return currentTime
```
Because we're just looking at each edge here, this has running time $O(m)$.
This will build a DFS tree, with the first vertex as the root and its neighbors as its children.

DFS is called on a vertex $x$'s descendants(call one of them $y$) during the process of performing the search on $x$, the time it will take to perform DFS on $y$ will be necessarily quicker than the time it will take on $x$. The start time for $y$ will also be later, because the process is started on $x$ and only then is the call made to $y$.
As such, you can prove that $y$ is a descendant of $x$ if you know that `x.startTime<y.startTime && x.finishTime>y.finishTime`.
This is proven and discussed more thoroughly during lecture 18.

DFS is very useful for solving the Topological Sorting Problem:

2. Breadth First Search or BFS

A Graph can be Weighted if there are Weights attached to its edges. Those weights represent something about the relationship between the two vertices that the edge connects, most commonly how closely related they are.
On a map, the weight of an edge would be the distance between the two locations it connects, for example.
For finding optimal paths between nodes on a Weighted Graph, look to [[Dijkstra's Algorithm]] and its less-efficient but more-resilient brother the [[Bellman-Ford Algorithm]].
Note that in some applications negative edge weights are possible, and if a loop can be formed within the Graph that has a net-negative weight to all of its edges, then the optimal path becomes just following that loop infinitely, which is no good.

Below is a full `c++` implementation of a Directed, Unweighted Graph that I wrote myself:
It includes things such as Depth-First-Search and just generally is ready to be used.
There are doubtless more efficient ways to implement this though, for example several of the class variables within `Vertex` are almost certainly unnecessary or their functionality can be created elsewhere. This is probably not optimal, but it does work for most applications.

This implementation assumes that you are `using namespace std;` and that you have `#include<vector>`.

```
struct Graph{

  

    vector<vector<int>> adj_matrix;

    Vertex* Verteces;

    int n;

    Graph(int numVerteces){//Sets up a blank matrix of the appropriate dimensions, and creates the appropriate number of verteces.

        n=numVerteces;

        adj_matrix = vector<vector<int>>(n,vector<int>(n,0));

        Verteces = new Vertex[n];

        for(int i=0;i<n;i++){

            Verteces[i].ID=i;//Numbers each vertex.

        }

    }

  

    void AddEdge(int u,int v){//Adds the edge both in the matrix representation and in each vertex's information.

        adj_matrix[u][v]=1;

        Verteces[u].OutDegree++;

        Verteces[u].Neighbors.push_back(&Verteces[v]);

        Verteces[v].InDegree++;

    }

  

    void ResetEdges(){//Resets all of the edge data within the verteces to match the information contained within the matrix.

        for(int i=0;i<n;i++){

            Verteces[i].Reset();

        }

        for(int i=0;i<n;i++){

            for(int j=0;j<n;j++){

                if(adj_matrix[i][j]==1){

                    AddEdge(i,j);

                }

            }

        }

    }

  

    int DFSHelper(Vertex* w,int currentTime){//Allows each vertex to be unmarked when the search is completed.

        int val = DFS(w,currentTime);

        for(int i=0;i<n;i++){

            Verteces[i].DoneWithSearch();

        }

        return val;

    }

  

    int DFS(Vertex* w,int currentTime){//Depth-first-search babyyy

        w->StartTime=currentTime;

        currentTime++;

        w->visited=true;

        int n = w->Neighbors.size();

        Vertex* v;

        for(int i=0;i<n;i++){

            v=w->Neighbors[i];

            if(!v->visited){

                currentTime=DFS(v,currentTime);

                currentTime++;

            }

        }

        w->FinishTime=currentTime;

        w->complete=true;

        return currentTime;

    }
  

struct Vertex{

    int StartTime;

    int FinishTime;

    bool visited = false;

    bool complete = false;

    int ID=0;

    int InDegree=0;

    int OutDegree=0;

  

    vector<Vertex*> Neighbors;

    void Reset(){

        StartTime=0;

        FinishTime=0;

        visited=false;

        complete=false;

        InDegree=0;

        OutDegree=0;

        Neighbors.clear();

    }

  

    void DoneWithSearch(){

        visited=false;

        complete=false;

    }

  

};
```