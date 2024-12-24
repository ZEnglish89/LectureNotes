
An algorithm which calls itself using an input which has been changed and modified by itself.
It must have a stopping condition to ensure it does not create an infinite loop.
In this class, it will typically reduce the input with each recursion, and stop when the input reaches 0.
Binary Search Trees use recursive algorithms, anything that Traverses the tree will recur by calling itself with the node to its left or right, then *that* node's left or right, and so on. The stopping condition is when you reach the bottom of the tree, i.e. when the current node does not have a child.

Recursive algorithm for factorial:

	if n=0 then return 1
	else return n * factorial(n-1)


Recursive Merge Sort:
(I'll have to pour over this on my own time, it's very conceptually cool though)
Note that it should just be returning L at the end. Small omission.
![[Pasted image 20231115173412.png]]
![[Pasted image 20231115173440.png]]

Merge Sort works very similarly from the Binary Search Tree copy constructor, I just can't quite make sense of it to the degree that would allow me to explain it concisely.

The `merge` function called is presumably similar to insertion sort; it takes two lists and combines them in such a way that all of their elements are in order.