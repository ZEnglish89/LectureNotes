
A hashed data structure allows for fast insertion, deletion, and searching.

Self-Balancing trees such as the [[Red-Black Tree]] have $O(log(n))$ deterministic performance, meaning that you can guarantee that there will always be consistent moderate speed.

However, hash tables have $O(1)$ expected performance: There is a worst-case that is much worse to deal with, but the average case is absolutely wonderful.

Place things in "buckets"(usually linked lists) based on a **hash function**: your input is run through the function, and the output shows which bucket the input belongs in.

The naive method is to use a modulus function, so the buckets are just dependent on the last digit of the input, or whether the input is even or odd, etc.
This allows for a worst-case where not all of the buckets get used/inputs get disproportionately sorted into a limited number of buckets(referred to as having a lot of "collisions"), resulting in complexity approximating $O(n)$, no good.

In order to have a good hash table, you need to manage two factors:
1. The more buckets there are($n$ buckets), the more space your table will require
2. The less evenly spread between the buckets your inputs are, the more time your operations will require.

For the purpose of these notes, the set of all possible inputs is $U$ and $|U|=M$.
So the goal is to define a hashing function $h:U->[1,...,n]$ such that no matter what input(fewer than $n$ items for $n$ buckets) the buckets will be balanced($O(1)$ entries per bucket).
If this hashing function is achieved, than Insert/Delete/Search will be $O(1)$ on this hash table.

Unfortunately, this is entirely impossible. For any deterministic hashing function, there exists some worst-case input that will result in unbalanced buckets. That worst-case input is just different from function to function.

Because of this, outside of niche applications, you will want to use a hash function with some degree of randomness. However, a hash function that just assigns keys into a random bucket is not practical, both for storage reasons and because retrieving the item afterwards is very difficult. Hash families are used instead.

A hash family is a collection of hash functions. The largest one possible is of course "all of the hash functions" but that's just there for an example.
When using a hash family, each input is hashed using a random function from the family, and then additional data is stored to remember which of the functions was used to hash that input so it may be retrieved later.

The goal is to choose a family of $H$ hash functions such that you can expect $O(1)$ buckets, but the $log(|H|)$ bits required to store which function was used is not prohibitively large.

A hash family is Universal if for all $u_i,u_j\in U$ with $u_i\neq u_j$,$$P_{h\in H}[h(u_i)=h(u_j)]\leq\frac{1}{n}$$
In other words, if you pick a random $h$ from $H$, the odds of a collision are no greater than with a uniform distribution.

Using this method, a hash table will require $O(nlog(M))$ bits of space: 
1. $O(n)$ buckets.
2. $O(n)$ items with $log(M)$ bits per item.
3. $O(log(M))$ bits to store the hash family.