A collection of elements.
Trees are called "rooted" if they have a root, a single element which serves as the beginning of the whole structure. In rooted trees, there is only one possible path between any two elements.
These are the same structures that we're using in Data Structures.

The "level" of a tree is how many degrees it's separated from the root. The root exists on level 0, its children are on level 1, etc. The "size" or "height" of a tree is how many levels it has.

Binary Trees are trees where every node has either 0 or 2 children.
Tertiary Trees: 0 or 3 children.
And so on for all possible numbers, they're defined in that sense.

Full Binary Trees:
Height h(t) is defined by:
Basis Step: The height of a root-only full binary tree T is h(T) = 0

Recursive Step: If T<sub>1</sub> and T<sub>2</sub> are full binary trees, then the full binary tree T<sub>1</sub> * T<sub>2</sub> has height 
h(T) = 1 + max(T<sub>1</sub>,T<sub>2</sub>).
The new tree, created by the concatenation, will have a root where the root's two children are the roots of T<sub>1</sub> and T<sub>2</sub>. This means that the minimum height is 1(the root and its children), and the actual height will be that 1 + whichever of the two concatenated trees is taller.

Number of Vertices n(T):
Basis Step: The number of vertices of a root-only full binary tree is n(T)=1

Recursive Step: If T<sub>1</sub> and T<sub>2</sub> are full binary trees, then the full binary tree T = T<sub>1</sub> * T<sub>2</sub> has the number of vertices n(T) = 1 + n(T<sub>1</sub>) + n(T<sub>2</sub>)
The new tree's root is the 1, then simply the two trees added together.

n(T) <= 2<sup>h(T)+1</sup>-1

Basis Step: for a root-only full binary tree, this holds: n(T) = 1 and h(T) = 0
1 = 2<sup>0+1</sup>-1

Recursive Step: Assume n(T<sub>1</sub>) <= 2<sup>h(T<sub>1</sub>)+1</sup>-1 and also n(T<sub>2</sub>) <= 2<sup>h(T<sub>2</sub>)+1</sup>-1
whenever T<sub>1</sub> and T<sub>2</sub> are full binary trees.
![[Pasted image 20231115172444.png]]
Just copying that because no way am I typing it out.
It's a big opaque but just scroll up and look back over the recursive definitions of h(T) and n(T) above.