
When given a sequence or chain of $n$ Matrices $A_n$, this algorithm seeks to properly parenthesize the chain so that the product of multiplying each [[Matrix]] together can be obtained as efficiently as possible.

This whole setup is covered in Chapter 15.2 of the textbook, but it's useful to take my own notes here.

Multiplying a $p\times q$ Matrix with a $q\times r$ Matrix requires $p\times q \times r$ multiplications, and produces a $p\times r$ Matrix as a result.
Because of this, choosing different sets of parentheses, for example $((A_1A_2)A_3)$ vs $(A_1(A_2A_3))$, can vastly affect the total number of operations required.

This algorithm does not actually multiply the Matrices in question. It simply decides the proper order in which they ought to be multiplied for peak efficiency.

We cannot brute force this, as for $n>1$ the number of parenthesizations $P(n)$ is:$$P(n)=\Sigma_{k=1}^{n-1}P(k)P(n-k)$$
Which, although I'm not interested in solving that in the scope of this problem, is too big to be considered worth the trouble. Indeed, using that algorithm to identify the optimal setup and then performing the multiplication may even be worse than performing a suboptimal multiplication.

In order to determine the optimal parenthesization of a list of matrices $A_i,...,A_n$, you must identify an index $k$ such that $i\leq k \leq n$ so that you can multiply $A_i,...,A_k$ and $A_{k+1},...,A_n$ before multiplying those results together. Each of those two sub-lists must then also be parenthesized in the same fashion.