
A common algorithm for finding the [[Strongly Connected Components]] of a given Directed [[Graph]].
This is the algorithm that the textbook bases its pseudocode for this problem off of.

It works by performing Depth-First-Search on the Graph, then taking the transpose of the graph(reversing the direction of every edge) and performing DFS a second time, but this time conducting the search in the order of the vertices' finishing times on the first DFS run.

It's a little bit confusing, but not the worst in the world.

Pseudocode:
```
StronglyConnectedComponents(G):
	run DFS(G) to find finishing times u.f for each vertex u
	take G^T the Transpose of the Graph
	Call DFS(G^T), but choose the vertex with the latest finishing time
	Each run of DFS(G^T) will give a tree, that tree is a SCC
```

Below is a `c++` implementation of the algorithm that did end up working. It has some comments and such, but is still pretty confusing.

The current implementation is printing out each vertex's SCC ID, which is the number of the first vertex in that vertex's SCC. However, it can be very easily modified in order to instead print out the SCCs, by removing some of the commented print statements.

```
#include<iostream>

#include<vector>

#include<stack>

  

#define MAX_N 20001//This was recommended to me online, when I had the issues with dynamic allocation(see line 81). It's an arbitrary value.

  

using namespace std;

  

struct Node {

    vector<int> Adjacent;

    vector<int> ReverseAdjacent;

};

  

/*

Node* g;

stack<int> S;

bool* visited;

int* component;

vector<int>* components;

int numComponents;

*/

  

Node g[MAX_N];

stack <int> S;

bool visited[MAX_N];

vector <int> components[MAX_N];

int numComponents;

  

void DFS(int x){

    visited[x]=true;

    for(int i=0;i<g[x].Adjacent.size();i++){

        if(!visited[g[x].Adjacent[i]]){

            DFS(g[x].Adjacent[i]);

        }

    }

    S.push(x);//Stack it in order of endtime.

}

  

void SpecialDFS(int x){
	cout<<x<<" ";

    components[numComponents].push_back(x);

    visited[x]=true;

    for(int i=0;i<g[x].ReverseAdjacent.size();i++){

        if(!visited[g[x].ReverseAdjacent[i]]){

            SpecialDFS(g[x].ReverseAdjacent[i]);

        }

    }

}

  

void Kosaraju(int n){

    for(int i=0;i<n;i++){

        if(!visited[i]){

            DFS(i);

        }

    }//First round of searches, stacking up the elements.

    for(int i=0;i<n;i++){

        visited[i]=false;

    }//resetting the bools to search again.

    while(!S.empty()){

        int v = S.top();

        S.pop();

        if(!visited[v]){
//	        cout<<"Component "<<numComponents<<": ";

            SpecialDFS(v);

            numComponents++;//holding onto this because it's used in the second search.
//            cout<<endl;

        }

    }//Second round of searches, in the order the elements were stacked.

}

  

int main(){

    int n;

    int m;

  

    cin>>n;

    cin>>m;

  

/*

    g = new Node[n+1];

    visited = new bool[n+1];

    component = new int[n];

    components = new vector<int>[n];

*/

//I really wanted to avoid having to use pre-allocated global variables, but seemingly no matter what I did it just wouldn't work.

//The most interesting problem is that my dynamically-allocated version wasn't deterministic. It would sometimes be correct and

//sometimes be incorrect, even if run back-to-back with the same inputs.

  

    int u;

    int v;

    for(int i=0;i<m;i++){

        cin>>u;

        cin>>v;

        g[u].Adjacent.push_back(v);

        g[v].ReverseAdjacent.push_back(u);

    }//Setting up the graph based on inputs.

  

    Kosaraju(n);

  

    int ID[n];

  

    for(int i=0;i<numComponents;i++){//I'm assigning the IDs via something hashing-esque to avoid having to search components n times.

        int min=components[i][0];

        for(int j=0;j<components[i].size();j++){

            if(components[i][j]<min){

                min=components[i][j];//Finding the minimum within each SCC, because they aren't automatically sorted.

            }

        }

        for(int j=0;j<components[i].size();j++){

            ID[components[i][j]]=min;//Assigning the ID for each element.

        }

    }

    for(int i=0;i<n;i++){

        cout<<ID[i]<<endl;

    }//And print!

  

    return 1;

}
```