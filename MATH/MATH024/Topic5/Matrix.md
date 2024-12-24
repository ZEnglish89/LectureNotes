
The plural is Matrices but I need my links to work so I'll be getting it wrong.

A Matrix is a rectangular array of elements/entries arranged in rows and columns.
$a_{(row,column)}$ is the notation for pointing out a specific element in a Matrix. Note that this is of the form $(y,x)$ instead of $(x,y)$, don't get mixed up by that.

The size of a Matrix is denoted as $m \times n$, where there are $m$ rows and $n$ columns. This is, again, $(y,x)$.

$A = [a_{ij}]$ to indicate the components of a matrix of known size.

If $m=n$, then $A$ is a *square matrix*, because, of course, it's a square.
If the only non-zero entries of a square matrix are the ones where $i=j$(i.e. on the center-line from the top left to bottom right corners), then the matrix is diagonal.

If all the diagonal entries of a diagonal matrix are 1, that is called the *$n \times n$ identity matrix.*
The book refers to it as $I_n$, it can also be $1_n$, $Id(n)$, or several other things.

A $m \times 1$ matrix is a *column vector*.
A $1 \times n$ matrix is a *row vector*.

A matrix can be viewed as a collection of $n$ column vectors and/or $m$ row vectors, if you so desire.

If a matrix has all zeros for entries, it is called *the zero matrix*. $0_{mn}$ or just $0$? I zoned out for a minute, I'll need to look back at the notes for the notation.

() and $[]$ are interchangeable, but you cannot use $||$

Addition and subtraction of matrices is performed component-wise:
$$A\pm B = [a_{ij}] \pm [b_{ij}] = [a_{ij} \pm b_{ij}]$$

If the dimensions of two vectors do not match, then the addition and subtraction of them is not defined. Treat matrices as objects, which must remain constant in dimension and cannot be manipulated to fit normal arithmetic.
$$[2,0,9] + [8,1,8] = [10,1,17]$$
Matrices can be multiplied by a constant or scalar by simply scaling, distributing the scalar to all entries: $$kA = k[a_{ij}]$$
$$3\cdot [2,0,9] = [6,0,27]$$
Matrix Division does not exist.
Matrix Multiplication is a pain in the ass. This bad boy is $O(x^3)$ by the normal method.

The matrix product of a $m \times r$ matrix A and a $r \times n$ matrix B is a $m \times n$ matrix C given by: $$C_{ij} = [a_{i1},a_{i2}, ..., a_{ir}] \times [b_{1j}, b_{2j}, ..., b_{rj}]$$
$$C_{ij} = \Sigma^r_{k=1} = a_{ik}b_{kj}$$
Where each item is the [[Scalar Product]] of the relevant row and the relevant column.

Multiplying another Matrix by an Identity Matrix of matching dimensions will not change it. $A \times I = A$
This is also commutative as a result: $A \times I = I \times A$
This is why it's called the identity matrix, it's the multiplicative identity for matrices.

A Matrix is considered Symmetric if it is equal to its own [[Transpose]].
It is called Anti-Symmetric or Skew-Symmetric if its negative is equal to its own [[Transpose]].

Matrices of functions behave as you'd expect under differentiation:
$$[A(t) + B(t)]' = A'(t) + B'(t)$$
$$[cA(t)]' = cA'(t)$$
$$[A(t)B(t)]' = A'(t)B(t) + A(t)B'(t)$$
The Square Root of a matrix A is a matrix R such that $R^2=A$. As in $R\times R$, matrix multiplication.
Not every matrix has a square root.

Upper Triangular Matrices are used in [[Gauss Elimination]] to help solve [[System]]s. Such Matrices are considered to be in Row Echelon Form. When Elimination is finished, the Matrix will be in Reduced Row Echelon Form.
Similarly, this is made easier via an Augmented Matrix(See Lecture Notes 3.2 for diagram, I'm not dealing with actually writing out matrices here).
Also see the [[Gauss Elimination]] note for information on Row Operations.

When being used in [[Gauss Elimination]] to solve [[System]]s: If the rank of the matrix is equal to the number of variables, then there is a unique [[Solution]]; the System is definite.
If the rank is less, then the solution is not unique, the system is indefinite.

[[Superposition]] and the [[Nonhomogeneous Principle]] also exist for Matrices.