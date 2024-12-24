
Move through the list left-to-right, starting with the second item. With each item, search through the part of the list you've already covered right-to-left, moving each item one space to the right, until you find an item which is less than the item you're currently inserting. Then insert your item at the appropriate spot and move on.

Pseudocode:
```
for i =2 -> Length do
key <- A[i]
j<-i-1
	while j>0 and A{j}>key do
	A{j+1}<-A{j}
	j<-j-1
A{j+1}<-key
```
This runs in worst-case and average-case $O(n^2)$ time-complexity.
$O(n)$ space complexity, it just takes up the original list/array.

When implementing this yourself, it can be easy to default to iterating left-to-right all the time. This does work, but it requires a few additional variables, is potentially(I'm not sure) slower, and takes up twice the space.
Basically, doing it that way is possible, and not *that much* worse, but there's no benefits over doing it the way above.