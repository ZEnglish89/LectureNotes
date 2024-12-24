
An algorithm design paradigm, like [[Divide and Conquer]] is.

It has a few core elements:
1. Optimal Sub-Structure:
	The solution to a problem can be expressed in terms of solutions to smaller sub-problems.
2. Overlapping Sub-Problems:
	 More than one larger problem can be expressed in terms of solutions to the same smaller sub-problems, so solving those sub-problems once and storing their solutions for multiple uses saves processing time.

The basics are really that simple. Dynamic Programming is just splitting your problem into smaller problems, and then holding on to the solutions to the smaller problems so you can use them later.

Dynamic Programming algorithms can be designed either Top-Down or Bottom-Up:
1. Top-Down:
	 Like a recursive algorithm, look at the larger problem, split it, and use recursion from there. The difference between this and [[Divide and Conquer]] is that the solutions to sub-problems are stored in some way, referred to as Memoization.
2. Bottom-Up:
	 Solve the smallest problems first, then the larger ones, and continually step up from there until you reach the main problem.

