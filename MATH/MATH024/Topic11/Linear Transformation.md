
A Linear Transformation or Linear Transform $T$ on a [[Vector Space]] $\mathbb{V}$ to a vector space $\mathbb{W}$ is a function $T:\mathbb{V}->\mathbb{W}$ that preserves scalar multiplication and vector addition.
That is to say, for all $\vec{u},\vec{v}\in\mathbb{V}$ and $\lambda\in\mathbb{R}$, $$T(\lambda\vec{u})=\lambda T(\vec{u})$$ and$$T(\vec{u}+\vec{v})=T(\vec{u})+T(\vec{v})$$
$\mathbb{V}$ is referred to as the Domain, and $\mathbb{W}$ is the Codomain or Target.

A linear transformation associates the zero vector of the domain with the zero vector of the codomain, for example:$$T(\vec{0}\cdot\vec{u}) = 0\cdot T(\vec{u})$$
The "image" or "range" of a linear transformation is the set of vectors in $\mathbb{W}$ to which vectors in $\mathbb{V}$ are mapped:$$Im(T) = [\vec{w}\in\mathbb{W}|\vec{w} = T(\vec{v})|\vec{v}\in\mathbb{V}]$$
The most basic and obvious linear transformation is the Identity Transform, which literally just maps every item to itself, so $id_n(\vec{v})=\vec{v}$.

Differentiation is actually a linear transformation, as separate additive terms in a derivative have their derivatives taken separately, and you can pull constants out before differentiating.

An $m\times n$ [[Matrix]] $A$ when combined with a vector with $n$ elements $\vec{x}$ into $A\vec{x}$ can be considered a transformation, mapping the elements of $\vec{x}$ from $\mathbb{R}^n -> \mathbb{R}^m$.
Multiplying by $A$ transforms a vector $\vec{x}\in\mathbb{R}^n$ into another vector $\vec{b}\in\mathbb{R}^m$.

The simpler way to understand this is that a Transformation $T(\vec{u})$ can be represented as a Matrix, so $T(\vec{u}) = A\times\vec{u}$.
In effect, a transformation is just Matrix Multiplication, and each Transformation has its own Matrix.