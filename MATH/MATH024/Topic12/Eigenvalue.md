
$\frac{du}{dt} = au+bv$ and $\frac{dv}{dt} = cu+dv$ this can be written as a [[Matrix]] but I'm not typing that out. This is the equivalent of $y'=Ay$. $a,b,c,d$ are all just constants.

Like with [[Simple Harmonic Motion]], assume a solution of the form $u=e^{\lambda t}$ and $v=e^{\lambda t}$ I think, Haik moved on from that in less than five seconds.
$$A\vec{x} = \lambda\vec{x}$$
$T(\hat{v}) = \lambda\vec{v}, \lambda\in C$. He's talking about transformations here and it's just a complete disaster.

Definition: Let $T=\mathbb{V}->\mathbb{V}$ be a [[Linear Transformation]] from [[Vector Space]] $\mathbb{V}$ into vector space $\mathbb{V}$. A scalar $\lambda$ is an Eigenvalue(German for "proper value") of $T$ is there is a **nonzero** vector $\vec{v}\in\mathbb{V}$ such that$$T(\vec{v}) = \lambda\vec{v}$$ Such a nonzero vector is called an Eigenvector of $T$ corresponding to $\lambda$.

If the [[Linear]] Transformation $T$ is represented by a $n\times n$ [[Matrix]] $A$ where $\mathbb{V}=\mathbb{R}^n$ and $T(\vec{v})=A\vec{v}$, then $\lambda$ and $\vec{v}$ are characterized by the equation$$A\vec{v}=\lambda\vec{v}$$
From this:$$A\vec{v} = \lambda\vec{v}=\lambda I\vec{v}$$
Because multiplying by the Identity [[Matrix]] doesn't change anything. From this you can now get:$$(A-\lambda I)\vec{v} = \vec{0}$$
That equation gives a few things to you:
1. An Eigenvalue is a scalar $\lambda$ such that the operator $(A-\lambda I)$ is *singular* or *non-invertible*.
2. An Eigenvector is a nonzero vector that lies in the nullspace of $(A-\lambda I)$.

According to the [[Invertible Matrix Theorem]]:$$p(x) = |A-\lambda I| = 0$$$p(\lambda)$ is a polynomial of $n$th degree, called the Characteristic Polynomial.
The fundamental theorem of algebra states that a polynomial has a number of roots equal to its degree.

By setting up the Matrix addition between $A$ and $\lambda I$ you can just take the [[Determinant]] which will be equal to a polynomial thanks to the terms of $\lambda$. This is very easy with a $2\times 2$ Matrix, but with anything larger you'll need to mess around with some Row Reduction.

Once you have found an Eigenvalue, you can move on to find an Eigenvector using the above equations.

Haik worked the whole thing out during the lecture on 12/02-2024. It's very confusing to me but hopefully with some paper and a lot more time it can make sense.