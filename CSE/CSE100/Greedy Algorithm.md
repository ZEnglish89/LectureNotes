
This is a design paradigm(like [[Dynamic Programming]] and [[Divide and Conquer]]) that involves making the most optimal decision at each individual step without considering the consequences of that on future steps.

Sometimes this works! When trying to make change in US currency with as few coins as possible, the greedy option of choosing the largest denomination coin that does not take you over the price will always work.

Oftentimes this doesn't work. Trying to solve the [[Knapsack Problem]] with a Greedy approach will often trap you with a useless amount of budget left, missing out on potential value.

Activity Selection can be achieved greedily, if your priority is simply to complete as many activities as possible within the day. If you just greedily schedule the activity with the earliest finish time that does not have any existing time conflicts, you will achieve your goal.
This works in $O(n)$ time if the activities are sorted by finishing time, and $O(nlog(n))$ otherwise.

Greedy algorithms are really intuitive and are often the first thing the human brain will turn to, but proving their correctness is often difficult.

Proof of the Activity Selection problem is in Lecture 24. The short version is that the selection of earliest finish time ensures that an optimal next choice will never be ruled out by a time conflict. That's how proofs of Greedy Algorithms are structured: Prove that the greedy choice won't ever remove an optimal option when the next choice needs to be made.