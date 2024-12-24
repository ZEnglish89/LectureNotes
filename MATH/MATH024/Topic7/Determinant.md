
Consider a function $area(\vec{u},\vec{v})$ that satisfies:
1. It is [[Linear]] in the first and second arguments.
2. $area(\vec{u},\vec{v})=-area(\vec{v},\vec{u})$, or it is Skew-Symmetric(See [[Transpose]])(NOTE: The lecture notes directly say that $area(\vec{u},\vec{v}) = -area(\vec{u},\vec{v})$, however looking at the definition of the Transpose and the later work done in the notes, this doesn't appear to make *any* sense unless you assume a mistake and switch the variables as I have above)
3. If $\hat{e}_1$ and $\hat{e}_2$ are unit vectors with $\hat{e}_1 \cdot \hat{e}_2=0$, then $area(\hat{e}_1,\hat{e}_2)=1$

These properties apply to all determinants, with "all arguments" swapped for the two arguments mentioned.

Note that property 2 means that repeated entries give 0 area, as they must be equal to their own negatives and that is only true for things with magnitude 0.

Example: $\vec{u} = a_{11}\hat{x} + a_{12}\hat{y}$, $\vec{v} = a_{21}\hat{x} + a_{22}\hat{y}$
Then $$area(\vec{u},\vec{v}) = area(a_{11}\hat{x} + a_{12}\hat{y}, a_{21}\hat{x} + a_{22}\hat{y})$$
By Linearity, you can split these up to have matching terms as each, with the coefficients pulled out:$$a_{11}a_{21}area(\hat{x},\hat{x}) + a_{11}a_{22}area(\hat{x},\hat{y}) + a_{12}a_{21}area(\hat{y},\hat{x}) + a_{12}a_{22}area(\hat{y},\hat{y})$$
By property 2, the two terms with repeated arguments vanish, and the flipped arguments can be simplified(again via property 2) so that we get: $$area(
\vec{u},\vec{v}) = a_{11}a_{22}area(\hat{x},\hat{y}) - a_{12}a_{21}(\hat{x},\hat{y})$$
By property 3, $area(\hat{x},\hat{y})=1$, so the above comes all the way down to: $$area(\vec{u},\vec{v}) = a_{11}a_{22}-a_{12}a_{21}$$

This will then equal the area formed by the two vectors $\vec{u},\vec{v}$ if they are used to form a parallelogram with each vector making up its own pair of parallel sides.

We can then drop the orthogonal unit vectors and consider this to be a function on the rows of a [[Matrix]], see lecture notes 3.3 and 3.4 for a diagram.

Look at [[Permutation]] for how to find the Sign of a sequence of integers.

Haik for some reason solve the above equation as written, but from that point onward he began writing it as $a_{11}a_{22} - a_{21}a_{12}$, reversing the order of the second set of terms.

This is significant because he uses the order he places them in to justify the minus sign, using the row numbers to comprise the lists of integers: $$Sign(1, 2)a_{11}a_{22} + Sign(2,1)a_{21}a_{12} = (+1)a_{11}a_{22} + (-1)a_{21}a_{12}$$
This appears to be a convention: Terms are organized so that their column numbers are in ascending order.
When performing this operation on a [[Matrix]], each term is as follows: One coefficient from each column, with the rows each coefficient comes from being comprised of every possible [[Permutation]] of the list of rows; all those coefficients are multiplied together to make a term. The Sign of that Permutation of the list of rows is then used to decide the sign of the term.

For a $3\times 3$ [[Matrix]] the terms would shake out to be as follows: $$a_{11}a_{22}a_{33} + a_{31}a_{12}a_{23}+a_{21}a_{32}a_{13} - a_{21}a_{12}a_{33}-a_{31}a_{22}a_{13}-a_{11}a_{32}a_{23}$$
For a Square [[Matrix]] with side length $n$ there will always be $n!$ terms.

Finally, Definition: The Determinant of a [[Matrix]] is the sum of all products of the entries of that Matrix such that each term has exactly one entry from a row and column, and has the Sign given by its [[Permutation]] of row values.

Determinants give the volume of an $n$-dimensional parallelopiped spanned by the $n$ vectors that form the rows of a Matrix. Obviously higher-dimensions are a mindfuck but that's the application here.

Notation: $det(A) = |A|$, or surround the terms of the Matrix with $||$ instead of parentheses.

As a potential shortcut for finding Sign, draw a web connecting each entry in the given term of the Matrix. Each upward line in that web is considered to have "negative slope" and each downward line has "positive slope"(remember that Matrix rows grow downward instead of upward). If there are an even number of negative slopes, the sign is positive, if there are an odd number the sign is negative.

Theorem: $det(A) = det(A^T)$, the [[Transpose]] does not affect the Determinant.

Properties:
1. The Determinant is [[Linear]](it is a [[Linear Operator]]) in its rows or columns, so coefficients and sums can be pulled out.
2. The Determinant changes sign when its rows or columns are swapped
3. The Determinant of the Identity Matrix($I$) is 1

Theorem: If two rows or columns are equal, the Determinant vanishes. This technically follows from Property 2.

Theorem: Elementary Row Operation 1(See [[Gauss Elimination]]) does not change the Determinant.

Theorem: If a [[Matrix]] has a zero row, $det(A)=0$

Theorem: If $A$ is upper-triangular with no zeros in the diagonal, then the Determinant is exactly the product of the diagonal entries.
Corollary: The Determinant of a diagonal Matrix is the product of the diagonals.
Corollary: If a [[System]] $Ax=b$ is singular, then $det(A)=0$
Corollary: If $det(A)\neq 0$, the matrix $A$ is invertible(has an [[Inverse]])
Corollary: If $A$ is invertible, then $A^T$ is invertible.
Corollary: The Determinant of an invertible Matrix is equal to $\pm$ the product of all its pivots. The $\pm$ is determined by whether a row swap was used.

Theorem: $det(AB) = det(A)det(B)$
Corollary: $det(A^{-1}) = 1/det(A)$

Before you attempt [[Cofactor Expansion]], attempt row reduction: find a column with all zeroes except for one element, remove the entire row and column which corresponds to that element, and then you can calculate the determinant of the rest of the [[Matrix]] and multiply the result by $(val)(-1)^{a+b}$ where you removed row $a$ and column $b$.
You can create the column that you need via [[Gauss Elimination]].

If you can find multiple rows or columns which don't have [[Linear Independence]] from each other, then the whole determinant is zero.
This is because of the conceptualization of a Determinant as giving volume, and linearly dependent rows/columns imply that the conceptual "shape" that we're giving volume of is contained within a single plane, so it must have volume 0.

If you have a Matrix where every column is the same, the Rows lack [[Linear Independence]] and therefore by the [[Invertible Matrix Theorem]] the determinant is 0.

If there is a row or column of all zeroes, then your determinant is 0.

If you have a Matrix in Upper Triangular form, then the determinant is equal to the product of all of the elements along the diagonal.