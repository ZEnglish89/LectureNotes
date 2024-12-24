
Used in compression, this is a [[Greedy Algorithm]] that assigns each item in a list a code based on how frequently that item appears.
For a better explanation of the usefulness of this algorithm and a proof that it works, See chapter 16.3 of the textbook.

The codes are assigned by building a tree of the items, and then traversing the tree, appending a '0' to the code for each time a left-branch is stepped down, and appending a '1' for each time a right-branch is stepped down.

Below is psuedocode for building the tree, followed by a complete `c++` implementation that assigns codes to ABCDEF.

Pseudocode:
```
Huffman(C)
n = |C|
Q=C
for i=1 to n-1:
	allocate a new node z
	z.left = x = Q.top()
	Q.pop()
	z.right = y = Q.top()
	Q.pop()
	z.freq = x.freq + y.freq
	Q.push(z)
return Q.top()
```
Where C is the list of characters, each of which have their frequency, and Q is a min-priority queue, that is a queue which sorts itself such that the smallest item will be on the top.
Q in this case is sorted based on the freq attibute.

`c++` implementation:
```
#include<iostream>

#include<queue>

#include<string>

#include<vector>

  

using namespace std;

  

struct Node{

    int freq;

    char key;

    Node* left;

    Node* right;

};

  

struct node_cmp{ //I found this from StackOverflow, it allows a priority queue to work on my Nodes by looking at the values inside them.

    bool operator()(const Node* a, const Node* b) const{

        return a->freq > b->freq;

    }

};

  

void InOrderTraverse(Node* root){

    if(root==nullptr){

        return;

    }

    else{

        InOrderTraverse(root->left);

//        cout<<"Key: "<<root->key<<"Freq: "<<root->freq<<";";

        cout<<root->key<<":";

        InOrderTraverse(root->right);

    }

}

  

Node* Huffman(Node* C, int n);

void Codes(Node* root, string* list, string curr);

  

int main(){

    int n=6;

    Node* C = new Node[n];

    char array[]= "ABCDEF";

    char* list = &array[0];

  

    for(int i=0;i<n;i++){

        C[i].key=list[i];

        cin>>C[i].freq;

        C[i].left=nullptr;

        C[i].right=nullptr;

    }

    delete list;

    Node* Huff = Huffman(C,n);//Create the tree, grab the root.

//    InOrderTraverse(Huff);

    string* CodeList = new string[n];//This will hold the codes of the letters.

//    cout<<"Root: "<<Huff->key<<","<<Huff->freq<<endl;

//    cout<<"Left: "<<Huff->left->key<<","<<Huff->left->freq<<endl;

//    cout<<"Right: "<<Huff->right->key<<","<<Huff->right->freq<<endl;

    Codes(Huff,CodeList,"");

    char letter = 'A';

    for(int i=0;i<n;i++){

        cout<<(char)(letter+i)<<":"<<CodeList[i]<<endl;

    }

    return 1;

}

  

Node* Huffman(Node* C, int n){//This function constructs a tree which is used to create the codes.

//    cout<<"In Huffman"<<endl;

    priority_queue<Node*, vector<Node*>, node_cmp> Q;

    for(int i=0;i<n;i++){

        Q.push(C+i);

    }

/*    cout<<"Q is set up, printing it now."<<endl;

    for(int i=0;i<n;i++){

        cout<<Q.top()->key<<":";

        Q.pop();

    }*/

//    cout<<"Queue compiled"<<endl;

    for(int i=0;i<n-1;i++){

//        cout<<"Looping"<<endl;

        Node* z = new Node;

        Node* x = Q.top();

        Q.pop();

        Node* y = Q.top();

        Q.pop();

        z->key='0';

        z->left=x;

        z->right=y;

        z->freq = (x->freq + y->freq);

        Q.push(z);

    }

    Node* val = Q.top();

    Q.pop();

//    cout<<"returning"<<endl;

//    cout<<"val = "<<val<<" key = "<<val->key<<endl;

    return val;

}

  

void Codes(Node* root, string* list, string curr){//This function is little more than a traverse, but it creates and saves the codes based on the tree.

    if(root->left!=nullptr){

//        cout<<"Moving left"<<endl;

//        cout<<"When we move left, we hit Key: "<<root->left->key<<" With freq: "<<root->left->freq<<endl;

        string temp=curr;

        temp.append("0");

        Codes(root->left,list,temp);

    }

    if(root->key!='0'){

//        cout<<"Current key is: "<<root->key<<endl;

//        cout<<"Curr is: "<<curr<<endl;

        list[(int)((root->key)-'A')] = curr;

    }

    if(root->right!=nullptr){

//        cout<<"Moving right"<<endl;

//        cout<<"When we move right, we hit Key: "<<root->right->key<<" With freq: "<<root->right->freq<<endl;

        string temp = curr;

        temp.append("1");

        Codes(root->right,list,temp);

    }

    return;

}
```