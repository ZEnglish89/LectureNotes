
If E is a compact volume with a piecewise smooth boundary curve S with an outward normal [[Vector]], and $\overrightarrow{F}$ is a continuously differentiable [[Vector Field]] defined on E, then: 
$$\int\int\int_E (\nabla \cdot \overrightarrow{F})dV = \oint\oint_S(\overrightarrow{F} \cdot \hat{n}) dS$$

The [[Surface Integral]] of a [[Vector Field]] over a closed Surface(the "Flux" through the surface) is equal to the Volume Integral of the Divergence over the region enclosed by the surface.

Used for computing Flux Integrals on a complicated closed surface.
Can compute Volume of E with $\overrightarrow{F} = 1/3<x,y,z>$ because then the [[Partial Derivative]]s of F will reduce to $<1,1,1>$

Can be used to compute Flux on "open" surfaces: $$\int\int\int_E \nabla \cdot \overrightarrow{F} dv = \oint\oint_S \overrightarrow{F} \cdot d\overrightarrow{S} = \int\int_{S_1} \overrightarrow{F} \cdot d\overrightarrow{S} + \int\int_{S_2} \overrightarrow{F} \cdot d\overrightarrow{S}$$
