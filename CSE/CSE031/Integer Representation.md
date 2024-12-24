
If the result of an operation returns a value which is too great to be represented by the number of bits available, overflow has occurred.

"Signed" numbers are capable of being negative, "unsigned" ones are not. The word refers to a negative sign, naturally.

An int is, by default, a "signed integer variable" with 32-bits assigned to it. The first bit is reserved for the sign, the other 31 are the representation of the number itself. The largest value possible for an integer, as a result, is $2^{31}-1$. The smallest value possible is the same magnitude with the opposite sign, that is to say $-(2^{31}-1)$.
If the sign bit is 0, the number is positive, if it is 1, the number is negative.

The most obvious way to sign a number is, as implied above, to have the first bit in the representation handle it, and then the remaining bits to the right represent the number itself.
This is referred to as ***"Sign-Magnitude Representation***," because there's a sign followed by the magnitude.
As a side note, this representation can produce a $-0$.

Sign-Magnitude has its issues: arithmetic becomes more complicated when using this representation. Adding two negative numbers can result in an overflow in the leftmost bit, resulting in a positive sum. Similarly, adding two large positive numbers can result in an overflow into the leftmost bit, turning the sum negative. Additionally, incrementing the binary has the opposite effect based on which sign is applied; increments increase the absolute value rather than the magnitude.

Because of these issues, sign-magnitude is no-longer widely used.

***"One's Complement:"*** all bits are complemented, meaning all 1s become 0s and vice-verse.
So, for example, $7=00111$, and $-7=11000$.
Then, numbers beginning with 1 are read as negative, so a negative sign is used, the bits are complemented, and the magnitude is read as a normal positive number.
Under a One's Complement system, incrementing the binary always increases the value; that's one flaw in Sign-Magnitude that's fixed.
A negative zero is still possible, it's all-ones.

In One's Complement addition, if there is an overflow bit, it is taken and added back into the right-most bit. This, apparently, is sufficient to make addition always accurate under this representation.
The amount of numbers possible to represent within One's Complement is  $2^{n-1}$ positive numbers, counting $0$, and $2^{n-1}$ negative numbers, counting $-0$.

Problems with One's Complement: The arithmetic is imperfect, and there are still two zeros. One's Complement is not completely extinct, but is not standard by any means.

The problem with both of these representations is that there is overlap between the negative values and the positive ones; the existence of that $-0$. As such, we would have a much better representation if we could shift all the negative values "left" by one.

***"Two's Complement:"*** The same as One's Complement, but between complementing and reading the negative values, they are incremented by one. That means that what was formerly -7 becomes -8 and the former -0 becomes a -1, erasing it and increasing the range of the values by one. This achieves that "shift" leftwards we desired.
Two's Complement arithmetic does not require the adding of the overflowed bit, instead it can just be discarded and the result will work.
There are the same number of possible numbers in Two's Complement as there are in One's Complement, but this time $-0$ is not counted because it does not exist.
This one is actually used!!!

***"Bias Encoding:"*** A system devised to have all 0s represent the smallest number(the negative with the largest magnitude). That way you could just increment without worrying about negatives or positives, everything would just be offset so that 0 would be the minimum.
This works off of setting a bias. $$value=unsigned-bias$$
Where the bias for N bits is $2^{n-1}-1$.
For 5 bits, the bias is 15, so $00000=0-15=-15$
$00010=2-15=-13$ and so on and so forth.