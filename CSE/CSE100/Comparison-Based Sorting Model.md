
This includes [[Merge Sort]], [[Quick Sort]], [[Insertion Sort]], and other similar sorting algorithms.
It has been proven that no sorting algorithm which uses this model can beat the time complexity of $O(nlog(n))$. It's a hard floor on the time it must take.

The structure of this model is exactly what it sounds like: It's based on comparing two items within a set in order to determine which of them should come before the other in a sorted list. The difference between algorithms comes in how you group items into subsets and how you pair them up to be compared, all algorithms under this model perform comparisons.

Other sorting models can exist, but they are more difficult to put in computing terms, as they are better suited for the human mind's ability to think creatively and handle physical objects in 3D space.

Proof of the $O(nlog(n))$ comment:
Establish that all sorting algorithms in this model give rise to a *decision tree* and analyze the behavior of those trees.