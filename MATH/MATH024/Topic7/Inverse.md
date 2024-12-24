
The inverse of an invertible [[Matrix]] $A$ is another Matrix $A^{-1}$ such that $$A^{-1}A=AA^{-1}=I$$
where $I$ is the identity [[Matrix]]. For the purpose of this class, both Matrices must be square.
Think of this the same way that $5^{-1}\cdot 5 = 1$.
Theorem 1: $(A^{-1})^{-1} = A$
Theorem 2: $(AB)^{-1} = B^{-1}A^{-1}$
Theorem 3: If $A$ is invertible, then so is $A^T$(The [[Transpose]] of $A$), and $(A^T)^{-1} = (A^{-1})^T$

Proof of 1: if $B$ is invertible, then $B^{-1}B = I$. Replacing $B$ with $A^{-1}$ gives: $$(A^{-1})^{-1}(A^{-1})=I$$
Algebraically this can then be turned into Theorem 1: $(A^{-1})^{-1}(A^{-1})=AA^{-1}$ -> $(A^{-1})^{-1}A^{-1}A=A$ -> $(A^{-1})^{-1}=A$

Proof of 2: Note that $$(AB)^{-1}(AB)=I$$This can be multiplied from the right first by $B^{-1}$, then by $A^{-1}$ and cancelling the pairs that form an identity for:$$(AB)^{-1}A=B^{-1}$$
$$(AB)^{-1} = B^{-1}A^{-1}$$

Proof of 3: If $$(A^T)^{-1}(A^T) = I$$
and you take the [[Transpose]] of both sides, then $I^T=I$, so:$$A((A^T)^{-1})^T = I$$
and you can multiply this from the left by $A^{-1}$:$$((A^T)^{-1})^T = A^{-1}$$
and take another transpose to solve for:$$(A^T)^{-1}=(A^{-1})^T$$

Theorem: The [[Matrix]] Inverse, if it exists, is unique. This can be proven by assuming that a Matrix $A$ has two inverses, $B$ and $C$. By $$AC=I=AB$$ you can solve to find that $B=C$, so those two inverses are actually the same unique inverse.

If you have a [[System]] $Ax=b$ and $A$ is Invertible, you can multiply by $A^{-1}$ to get $x=A^{-1}b$.
This is useful if you have the inverse handy.

The inverse can be computed via [[Gauss Elimination]] by remembering that $AA^{-1}=I$ and solving for the inverse is the same as turning $(A|I)$ into $(I|A^{-1})$.
See Lecture Notes 3.3 and 3.4 for examples on performing this process.

Special case: For $2\times 2$ Matrix $A=(a,b,c,d)$, $A^{-1}=1/(ad-bd)\cdot (d,-b,-c,a)$
The condition for a $2\times 2$ [[Matrix]] to be Invertible is that $ad-bc\neq 0$, because otherwise there would be a divide-by-zero violation in the above special case.

A Matrix is Singular if it is not Invertible.
A Matrix is Nonsingular if it is invertible.

For Nonsingular homogeneous [[System]]s $Ax=0$, the only [[Solution]] is the trivial solution $x=0$.