A method used to find all primes which do not exceed a specified positive integer.
For example, the integers between 1 and 100.

The procedure is quite simple: Remove all integers that are divisible by known primes, aside from themselves, in order until you reach the last prime that is <= 100<sup>1/2</sup>, because [[Root Theorem]] tells us that any further numbers are not required: Remove all numbers divisible by 2, then divisible by 3, then 5, then 7. Once you are done, all numbers which have *not* been removed are prime.
