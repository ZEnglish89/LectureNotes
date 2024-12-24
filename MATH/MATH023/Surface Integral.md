
For [[Scalar]] Surface Integrals:
$$\int\int_S fdS = \int\int_D f(r(u,v)) \cdot ||r_u \times r_v ||dudv$$
Above, $r(u,v)$ is the parameterization for a [[Parametric Surface]]

The function f is surface density for the surface S; the total mass is equal to the surface integral. To find surface area, simply assume a density of 1, so the surface area of the portion of a [[Parametric Surface]] over a rectangular region with parameterization $r(u,v)$ is: $$\int\int_D ||\overrightarrow{r}_u \times \overrightarrow{r}_v || dA$$

For [[Vector Field]] Surface Integrals:
S must be an oriented smooth surface(see the [[Parametric Surface]] note for details) with a unit normal vector $\hat n$. The Surface Integral of [[Vector Field]] F over S is: $$\int\int_S \overrightarrow{F} \cdot d\overrightarrow{S} = \int\int_S \overrightarrow{F} \cdot \hat{n} dS$$
Hopefully I can make more sense of this as time passes.
This is also called the "Flux Integral" of $\overrightarrow{F}$ over S.
This can be thought of as a "mass flow rate" across S.

It's unclear when to use Scalar vs when to use Vector Field. HOWEVER, questions which require Vector Field Surface Integrals will often ask for the Flux instead, to make it clear. I just have to hope that happens on the exam.

The Flux Integral can be further "simplified": $$\int\int_S \overrightarrow{F} \cdot \hat{n} dS = \int\int_D \overrightarrow{F}(\overrightarrow{r}(u,v)) \cdot (\overrightarrow{r}_u \times \overrightarrow{r}_v) dA$$

