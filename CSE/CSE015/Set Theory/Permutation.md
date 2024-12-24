An ordered arrangement of a set of distinct objects or elements.
Opposed to [[Combination]]s due to their ordered nature.
A permutation of r elements of a set is an "r-permutation."

S = {1,2,3}
3,1,2 is a permutation of S
3,2 is a 2-permutation of S
The number of possible r-permutations of a set with n elements is denoted by P(n,r).
S has 3 elements and 6 possible 2-permutations, so P(3,2) = 6
P is not the name of the set, it denotes "number of permutations" instead.

To find the number of permutations of a set with n elements, simply use n!
To find the number of r-permutations: P(n,r) = n! but you stop at (n-r)+1 instead of 1.
This formula is found using the [[Product Rule]].
n * (n-1) * (n-2) ... * (n-r+1)
P(3,2) = 3 * 2 = 6
P(4,2) = 4 * 3 = 12

Can also be written as P(n,r) = n!/(n-r)!
This is the more intuitive way to do it, as the whole (n-r+1) business is personally confusing.
3! = 6 (3-2)! = 1 6/1 = 6
4! = 24 (4-2)! = 2 24/2 = 12

How many permutations of the letters ABCDEFGH contain the string ABC?
Treat ABC as one element, and count the permutations of a set with 6 objects: ABC,D,E,F,G,H
instead of 8 objects: A,B,C,D,E,F,G,H.
All permutations of the set of 6 will be permutations of the set of 8 where that string appears.

On tests, Combination and Permutation problems will just have to be written out in their expanded multiplication form. They should not be left as factorial, but they do not necessarily need to be simplified all the way down, simply because some problems will be too large for that to work, even with calculators.
For example, if you get 52!/(5! * 47!) then multiply it out to 
(52 * 51 * 50 * 49 * 48)/(5 * 4 * 3 * 2 * 1), cancelling the factorials appropriately, but you do not have to multiply that final expression out.