Also called [[Linear]] Space.
A nonempty collection $\mathbb{V}$ of Vectors defined over a field $\mathbb{R}$.
Note that we aren't using the normal definition of Vector here; anything that satisfies the below properties is considered a vector.

Closure Properties:
1. Given any two $\vec{x},\vec{y} \in \mathbb{V}$ there is a rule called $+$ (addition) that gives a unique element $(\vec{x}+\vec{y})\in \mathbb{V}$ called the sum of $\vec{x}$ and $\vec{y}$.
2. Given any element $\vec{x}\in V$ and a scalar(Defined as an element of a field) $\lambda \in \mathbb{R}$ there is a rule called *scalar multiplication* that gives a unique element $\lambda \vec{x}\in \mathbb{V}$.

Addition has the following rules:
3. Commutivity: $\vec{x}+\vec{y}=\vec{y}+\vec{x}$, for all $\vec{x},\vec{y} \in V$
4. Associativity: $(\vec{x}+\vec{y})+\vec{z} = \vec{x}+(\vec{y}+\vec{z})$ for all $\vec{x},\vec{y},\vec{z} \in \mathbb{V}$
5. Zero Vector: There exists $\vec{0} \in \mathbb{V}$ such that $\vec{x}+\vec{0}=\vec{x}$
6. Inverse: For all $\vec{x}$ there exists $\vec{y}\in \mathbb{V}$ such that $\vec{x}+\vec{y}=0$

Scalar Multiplication has the following rules:
7. $1\cdot \vec{x} = \vec{x}$ for all $\vec{x}\in \mathbb{V}$
8. $\alpha(\beta\vec{x})=(\alpha\beta)\vec{x}$ for all $\vec{x}\in V$ and $\alpha,\beta \in R$
9. $(\alpha+\beta)\vec{x} = \alpha\vec{x} + \beta\vec{x}$ for all $\vec{x}\in V$ and $\alpha,\beta\in R$
10. $\alpha(\vec{x}+\vec{y}) = \alpha\vec{x} + \alpha\vec{y}$ for all $\vec{x},\vec{y}\in V$ and $\alpha\in R$


Theorem: The Zero Vector is Unique.

Theorem: Every element in a vector space has a unique additive inverse.
Proof: If you assume that $\vec{x}+\vec{y}_1=0$ and $\vec{x}+\vec{y}_2=0$, you find that $\vec{y}_1=\vec{y}_2$

Theorem: $0\vec{x}=\vec{0}$ is always true in a Vector Space.
Proof: $0\vec{x}+1\vec{x} = (0+1)\vec{x}=1\vec{x}$. Then say $\vec{x}+\vec{y}=\vec{0}$(because every element has an additive inverse).
$0\vec{x}+1\vec{x}+\vec{y}=1\vec{x}+\vec{y}=\vec{0}->0\vec{x}=\vec{0}$

Theorem: $\vec{y}=-1\vec{x}$ acts as the additive inverse to $\vec{x}$.
Proof: Suppose that $\vec{x}+\vec{y} = 0$, then $(-1)\vec{x}=(-1)\vec{x}+\vec{x}+\vec{y}=(-1+1)\vec{x}+\vec{y}=0\vec{x}+\vec{y}=\vec{0}+\vec{y}=\vec{y}$
What a mess.

Elements 1. and 2. can be combined for simplicity, this gives Closure Property 0:
$\alpha\vec{x}+\beta\vec{y}\in V$ whenever $\vec{x},\vec{y}\in V$ and $\alpha,\beta\in R$

A nonempty subset $\mathbb{W}$ of a vector space $\mathbb{V}$ is a Vector Subspace so long as it is closed under addition and scalar multiplication.
It must be true that $\vec{0}\in \mathbb{W}$
If $\vec{u},\vec{v}\in\mathbb{W}$ then $\vec{u}+\vec{v}\in\mathbb{W}$
If $\vec{u}\in\mathbb{W}$ and $\lambda\in\mathbb{R}$ then $\lambda\vec{u}\in\mathbb{W}$

The solutions to $A\vec{x}=\vec{0}$ is a very important subspace called the Nullspace, or Kernel.

If $A\vec{x}=\vec{0}$ and $A\vec{y}=\vec{0}$ then $$A(\alpha\vec{v}+\beta\vec{y}) = \alpha A\vec{x}+\beta A \vec{y}=\alpha\vec{0}+\beta\vec{0}=\vec{0}$$
