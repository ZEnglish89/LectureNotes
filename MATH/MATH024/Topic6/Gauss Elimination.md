
A strategy with which you can help understand the definitions regarding [[System]]s, as well as potentially solving them.

The example below is for a system of three tri-variable equations, but it will work as long as you have at least as many equations as you have variables.

Stage One: Pick one equation "the first" and add multiples of it to the other equations, attempting to eliminate one variable from both of them. The coefficient of the one remaining instance of the variable is called the "first pivot."

Stage Two: Pick a different equation and a different variable, add multiples of that equation to attempt to remove it from the third.

Stage Three: The third equation should now be in terms of a single variable. Solve it, then substitute into the second equation, which will be in terms of two variables, and then substitute into the first, which is still in all three. Work back up the chain, so to speak.
Hey this is kinda recursive lol

This produces an Upper Triangular [[Matrix]]. A Matrix which is obtained when Gauss Elimination is completed is referred to as being in Row Echelon Form.
The process can be streamlined using an Augmented [[Matrix]], see Lecture Notes 3.2.
The coefficients of the equations are written out in the Matrix, with each equation getting a row. One column for each variable, with an additional column for whatever constants are on the other side of the equality.

Then Row Operations can be used: 
Operation One: $\lambda R_i + R_j -> R_j$ denotes adding the contents of Row$_i$ with a multiplier $\lambda$ into the contents of Row$_j$. This is used in the actual elimination process.
Operation Two: $R_i <--> R_j$ simply swaps the two rows. This is used to reorganize the Matrix, so that the equations with fewer variables end up on the bottom, making the Matrix triangular more rapidly.
Operation Three: $\lambda R_i -> R_i$ simply multiplies a row by a constant multiplier.


If you can continue Elimination further, you can put the Matrix in Reduced Row Echelon Form. This is when:
1: Any rows made up entirely of zeroes are at the bottom
2: There is at most one nonzero entry in each row, and it is 1. This is called the pivot.
3: Each pivot is further to the right than the one above it.

If you successfully put a [[Matrix]] in this form, then the rightmost column will contain the solution to the [[System]] of equations: Top row is x, second row is y, etc.

I need to study Rank, Pivot Columns, the process of using an RREF Matrix to solve a System once I've got it, and just generally practice the process of elimination itself. I keep backing myself into corners.