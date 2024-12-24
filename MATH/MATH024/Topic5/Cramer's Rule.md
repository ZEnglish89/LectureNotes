
With a [[System]] $Ax=b$, you can consider $A$ to be a collection of columns $A_i$
As such, $Ax=b$ is $$x_1A_1 + x_2A_2 +...+x_nA_n =b$$
If one column, the $ith$ column, is replaced by $b$, then the [[Determinant]] of that new [[Matrix]] will have all columns aside from that $ith$ column vanish, giving that $det(A^{(i)}) = x_i|A|$ or $x_i = |A^{(i)}|/|A|$ where superscript $i$ denotes the version of the Matrix with the column replaced.

You can use this to solve for the terms of $x$, as shown in the examples in Lecture Notes 3.3 and 3.4

Replacing the x-column of the matrix with the solution matrix will give you $A_x$, and $x=|A_x|/|A|$. Those bars signify [[Determinant]]s.
This same rule holds true for all of the variables.

You can then check your answer by plugging in the values you get for the variables into the appropriate matrix and performing the multiplication.