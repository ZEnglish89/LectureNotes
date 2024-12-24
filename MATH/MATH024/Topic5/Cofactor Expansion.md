
Consider a $3\times 3$ [[Matrix]] $A$.

The [[Determinant]] of this Matrix is$$det(A) = a_{11}a_{22}a_{33} + a_{31}a_{12}a_{23}+a_{21}a_{32}a_{13} - a_{21}a_{12}a_{33}-a_{31}a_{22}a_{13}-a_{11}a_{32}a_{23}$$
Consider the first row of $A$, $a_{11}, a_{12}, a_{13}$. If we factor all terms with these three in them from the Determinant, we get: $$a_{11}(a_{22}a_{33}-a_{32}a_{23})+a_{12}(a_{31}a_{23}-a_{21}a_{33})+a_{13}(a_{21}a_{32}-a_{31}a_{22})$$
This can be rearranged to be as if we found three smaller [[Determinant]]s(see diagram in Lecture notes 3.3 and 3.4), making it much easier to compute.
This is done by looking at each of those three entries one at a time, and removing the rest of their row and column as you do so.

The smaller [[Matrix]] found by removing that row and column is called the "Minor of [[Order]] $n-1$."
The number $M_{ij}$ is the Determinant of the Minor.$$A_{ij}=(-1)^{i+j}M_{ij}$$
is called the *cofactor* of the entry $a_{ij}$.

The factor $(-1)^{i+j}$ comes from moving $a_{ij}$ up $i-1$ rows and left $j-1$ columns. Each time you swap a row or column, you acquire another factor of $(-1)$ in the [[Determinant]].

See the lecture notes for examples of how this is used to compute difficult Determinants.

Definition: A Minor of [[Order]] $r$ of a $m\times n$ [[Matrix]] is the [[Determinant]] of [[Order]] $r$ obtained after deleting all entries of a Matrix except for those simultaneously in $r$ rows and $r$ columns.

Definition: The *rank* of a [[Matrix]] is the smallest number $r$ such that all the Minors of [[Order]] $>r$ are zero or there are no such minors; $r=min(m,n)$.
Corollary: The rank of a [[Matrix]] is unaffected under [[Transpose]]s.

Theorem: ugh see page 18 of Lecture Notes 3.3 and 3.4 it's too much nonsense to type.