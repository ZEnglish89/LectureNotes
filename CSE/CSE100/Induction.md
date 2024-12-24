
Look back at CSE015 for a complete explanation of Mathematical Induction.

A logical process for proving something to be true:
First, prove that it is true in a specific situation.
Then, prove that if it is true for one situation, it is true for the situation that will immediately follow.
Once that is done, you have proved that it is true for all situations beyond the first.

For example, you can prove that [[Insertion Sort]] works via induction:
Insertion Sort starts with a 1-item list, and adds one item into it with each loop.
1: All 1-item lists are inherently sorted, because they can only be in one possible order.
2: [[Insertion Sort]] adds 1 item at a time into its proper place in a sorted list so that the list remains sorted.

We now know that the algorithm will start with a sorted list, and it will cause a sorted list to remain sorted as it adds each item. Therefore, we know by induction that Insertion Sort will always return a properly sorted list!