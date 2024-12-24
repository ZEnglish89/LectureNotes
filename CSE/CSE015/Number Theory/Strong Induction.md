To prove that P(n) is true for all positive integers n, use this strategy:
Complete the basis step: Verify that P(1) is true.
Then the Inductive Step: Show that if P(k) is true for all 0<k<=n, then P(n+1) is also true.

Example: prove that every value $0.12 and greater can be formed using $0.04 and $0.05 components.

Basis step: P(12, 13, 14, 15) are all possible(3x4,2x4+5,4+2x5,3x5)
Inductive step: The basis shows that P(k) is true for 12<=k<=15. P(k-3) holds for k=15, 
because k-3=12. To achieve k+1, add an additional 4-cent value to the setup for k-3.
Effectively, because four consecutive situations are possible, and we can iterate by fours, then every higher situation is also possible because it can be reached by adding a multiple of four to one of the existing situations.

I could definitely use some more examples.