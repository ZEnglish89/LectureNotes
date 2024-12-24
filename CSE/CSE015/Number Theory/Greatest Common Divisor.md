The largest integer d such that two integers a and b are both divisible by d, is referred to as their Greatest Common Divisor, and denoted as gcd(a,b).

For small numbers, these can be found via brute force.

Two numbers are "relatively prime" if their gcd=1


For larger numbers, gcd can be found using [[Prime]] Factorization, using the same method as [[Least Common Multiple]], but swapping the max for a min:

Prime Factorize both numbers into p<sub>1</sub><sup>a1</sup> * p<sub>2</sub><sup>a2</sup> etc and p<sub>1</sub><sup>b1</sup> * p<sub>2</sub><sup>b2</sup> etc.

The gcd(a,b) = p<sub>1</sub><sup>min(a1,b1)</sup> * p<sub>2</sub><sup>min(a2,b2)</sup> etc.
a = 95256 b = 432
a = 2<sup>3</sup> * 3<sup>5</sup> * 7<sup>2</sup>   b = 2<sup>4</sup> * 3<sup>3</sup>
gcd(a,b) = 2<sup>min(3,4)</sup> * 3<sup>min(5,3)</sup> * 7<sup>min(2,0)</sup> = 2<sup>4</sup> * 3<sup>5</sup> * 7<sup>2</sup> = 190512