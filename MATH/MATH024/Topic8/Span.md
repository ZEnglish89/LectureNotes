
If a [[Vector Space]] $\mathbb{V}$ consists of all [[Linear]] combinations of the particular vectors $u_1,u_2,...,u_n$ then the vectors Span the Space.

The span of $\hat{x},\hat{y}$ is the entire $x-y$ plane, any point on the plane can be reached by combining those vectors. A point that requires some $z$-traversal is not within the span, as it cannot be reached with only $x$ and $y$ values.

Redefinition: Every vector $\vec{v}\in \mathbb{V}$ can be represented as some combination of the $\vec{u}_i$s:$$\vec{v}=c_1\vec{u}_1+c_2\vec{u}_2+...+c_k\vec{u}_k$$
Alternate Definition: A Span is the collection of all [[Linear]] combinations of vectors in a given [[Vector Space]]. We write span $$[\vec{u}_1,\vec{u}_2,...,\vec{u}_l]$$
For $\vec{u}_1=(1,0,0),\vec{u}_2=(0,1,0),\vec{u}_3=(2,0,0)$:
$\vec{u}_1+\vec{u}_2$ span a 2D space
$\vec{u}_2+\vec{u}_3$ span a 3D space
$\vec{u}_1+\vec{u}_3$ span only a 1D space, the $x$-axis.

Theorem:
For a set of vectors in a [[Vector Space]] $\mathbb{V}$, the Span of that set of vectors is a subspace of $\mathbb{V}$.
Proof: Let $v_1$ and $v_2$ be two vectors in the span. $$v_1=a_1u_1+a_2u_2+...+a_lu_l$$$$v_2=b_1u_1+b_2u_2+...+b_lu_l$$
Therefore:$$\alpha v_1+\beta v_2=\alpha(a_1u_1+...+a_lu_l)+\beta(b_1u_1+...+b_lu_l)$$
This can be rearranged such that each term is in the form of $(\alpha c_l +\beta b_l)u_l$ which means that we still have a [[Linear]] representation: each term is a vector of first degree multiplied by scalar constants.

For a [[Matrix]] $B$, $Col(B)$ is the [[Column Space]] of $B$. The specific [[Matrix]] being referred to is in the lecture notes, this lecture was on 10/21-2024, I'm not going through the mess of recreating a Matrix in Obsidian.
If there are some columns within the Matrix which can be used to form all of the other columns within the Matrix, then those columns provide the entire [[Column Space]] and Span on their own, and the others are redundant information for this purpose. The Span of those columns is the same as the span of the entire matrix.

You can use the Pivot Columns(See [[Gauss Elimination]] and all of its associated nonsense) for the above focus.