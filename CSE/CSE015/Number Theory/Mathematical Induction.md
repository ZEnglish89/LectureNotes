A proof method, widely used.

To prove that a given expression, P(n), is true for all positive integers n, there are steps to follow:

Basis step: Show that P(1) is true. This gives you a starting point.
You do not necessarily have to use 1, some proofs will begin at a different integer b, depending on their situation. Mathematical induction proves that P(n) is true for n>=b.

Inductive Step: Show that P(k)->P(k+1) is true for all k
To complete the inductive step, assume that P(k) is true and show that
the truth value of P(k+1) = the truth value of P(k)
Assuming that P(k) holds for k is called the inductive hypothesis.

The inductive hypothesis is proven by the inductive step, so long as the basis step is true. This is because the inductive step proves that if P(1) is true, then P(2) is true, and if P(2) is true, then P(3) is true, and so forth, and the basis step proves that P(1) is true.

The conjecture: 1 + 3 +5 + ... + (2n-1) = n<sup>2</sup> was proven via mathematical induction.
(the sum of the first n odd numbers will be equal to n<sup>2</sup>, written in English)
1 + 3 +5 + ... + (2k-1) = k<sup>2</sup> is the inductive hypothesis, so
1 + 3 +5 + ... + (2k-1)+(2(k+1)-1) = (k)<sup>2</sup> + (2(k+1)-1) must be true, as it is just the result of adding the same value to each side. Then, simply use algebra to simplify the right side of that equation to (k+1)<sup>2</sup>
