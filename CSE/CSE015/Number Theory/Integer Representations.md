Integers can be represented in any base, we generally use decimal, or base 10
For any base b, an integer has a base b expansion
Binary is base b=2
Octal is base b=8
Hexadecimal is base b=16
Any b value >1 can be used, b=20 and b=60 have been used in the past, but 10, 2, 8, and 16 are the four most commonly used both in daily life and in computations

A base representation is denoted by surrounding the value with parentheses and subscripting the b-value of the base afterwards.
(a<sub>k</sub>a<sub>k-1</sub>a<sub>k-2</sub>)<sub>b</sub> = a<sub>k</sub>b<sup>k</sup> + a<sub>k-1</sub>b<sup>k-1</sup>+a<sub>k-2</sub>b<sup>k-2</sup> = n

To expand an integer n to base b, take n mod b and then subtract b from n. The result of the mod is the rightmost undecided digit in the expansion, and you repeat the process with your now-subtracted n until n<b. K is equal to the number of times you take the mod function.

For conversions between specific base expansions to other bases(without first converting into decimal, which would be time-consuming) refer to the lecture 15 slideshow.

Because binary works on powers of 2 and octal and hexadecimal both work on values which *are* powers of 2, converting from binary to either of those is very streamlined.

Converting the other way is not as easy, but not massively more difficult.

Decimal does not fit into this nice pretty "powers of 2" model.