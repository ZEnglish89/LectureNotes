
If S is an oriented piecewise smooth [[Parametric Surface]] with unit normal vector $\hat n$, and C is the simple, closed, piecewise smooth, bounding curve of S with positive orientation with respect to $\hat n$, and $\overrightarrow{F}$ is a [[Vector Field]] having components with continuous [[Partial Derivative]]s on an open region containing S, then $$\int\int_S (\nabla \times \overrightarrow{F}) \cdot d\overrightarrow{S} = \oint_C \overrightarrow{F} \cdot d\overrightarrow{r}$$
The component on the left is a Flux Integral(see [[Surface Integral]]) and the component on the right is a [[Scalar]] [[Line Integral]].
This is effectively a 3D version of [[Green's Theorem]]. Specifically, if $\overrightarrow{F}$ has a z=component which is equal to 0, it just reduces down to Green's.

[[Green's Theorem]] is for [[Line Integral]]s, Stokes' is for [[Surface Integral]]s.

Used for computing work on a "complicated closed curve."
Can compute Flux Integrals of $\nabla \times \overrightarrow{F}$
If $\partial S_1 = C = \partial S_2$, then $$\int\int_{S_1}(\nabla \times \overrightarrow{F})\cdot d\overrightarrow{S} = \oint_C \overrightarrow{F} \cdot d\overrightarrow{r} = \int\int_{S_1} (\nabla \times \overrightarrow{F})\cdot d\overrightarrow{S}$$