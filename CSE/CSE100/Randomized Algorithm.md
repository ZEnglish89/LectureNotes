At some point during the access, some random decisions are made, and we hope they shake out such that the algorithm is both correct and fast.
We can guarantee that it is correct with clever construction, and we hope that it's fast when a value needs to be chosen but we cannot manually choose the best one.
A very good example is choosing the pivot for our solution to the [[K-Select]] problem, or [[Quick Sort]].

The classic example of a *bad* randomized algorithm is [[BogoSort]], which just scrambles the contents until it randomly permutates to a sorted position.

The runtime of a Randomized Algorithm can be more difficult to put through [[Asymptotic Analysis]] than a deterministic one.
You should look for Expected Runtime and Worst-case Runtime as the two measurements to be focused on.

You can find Expected by using the $E[]$ of all random terms within the algorithm(See Math032, unfortunately) and assuming that those expected values will all be achieved, then analyzing as if the algorithm were deterministic.

You can find Worst-case exactly how you would expect, by assuming the least beneficial outcomes from every source of randomness and then analyzing from there.