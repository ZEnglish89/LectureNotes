The smallest positive integer that is divisible by both integers a and b.
Denoted by lcm(a,b)
Finding multiples can be brute forced by taking ab, but this will not always be the lcm, it will simply be one multiple.

This can be found using [[Prime]] factorization, via the same technique as [[Greatest Common Divisor]] but swapping the min for a max:

Prime Factorize both numbers into p<sub>1</sub><sup>a1</sup> * p<sub>2</sub><sup>a2</sup> etc and p<sub>1</sub><sup>b1</sup> * p<sub>2</sub><sup>b2</sup> etc.

The lcm(a,b) = p<sub>1</sub><sup>max(a1,b1)</sup> * p<sub>2</sub><sup>max(a2,b2)</sup> etc.
a = 95256 b = 432
a = 2<sup>3</sup> * 3<sup>5</sup> * 7<sup>2</sup>   b = 2<sup>4</sup> * 3<sup>3</sup>
lcm(a,b) = 2<sup>max(3,4)</sup> * 3<sup>max(5,3)</sup> * 7<sup>max(2,0)</sup> = 2<sup>4</sup> * 3<sup>5</sup> * 7<sup>2</sup> = 190512

