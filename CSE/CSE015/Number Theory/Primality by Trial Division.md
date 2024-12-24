

The simplest, but inefficient method of determining if n is [[Prime]] is to see if it is divisible by each of the primes which are <= n<sup>1/2</sup>. You do not need to worry about primes greater than n<sup>1/2</sup> because all composite numbers must have at least one factor which is lesser than its square root.

This is very straightforward, but requires an attempted division for each and every prime under the root, effectively brute-forcing the problem. It would be O(n) for a computer(I assume).

This process is known as Trial Division; you would say you are "Determining Primarily by Trial Division."