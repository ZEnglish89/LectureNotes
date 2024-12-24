

9 Questions, 20 minutes per question(ish)
1 T/F and 8 written questions
50% will be on the rest of the class, 50% on the end units

The grading scheme will be the best of: The regular one, and a version where the final is worth 46%

Look back through Midterm reviews to check the old material, he's just giving us the end stuff here.

[[Vector Field]]s: Sketching them in 2D, checking if they're conservative/irrotational($\nabla \times \overrightarrow{F} = 0$, can be the gradient of a Vector Potential) and incompressible($\nabla \cdot \overrightarrow{F} = 0$, can be the curl of a vector potential).

[[Line Integral]]s: parametric curves/[[Space Curve]]s $\overrightarrow{r}(t)$; checking if they're smooth $\overrightarrow{r}'(t)\neq0$ and checking orientation direction of $\overrightarrow{r}(t)$

Scalar [[Line Integral]] $\int_C f dS = \int_a^b f(\overrightarrow{r}(t)\cdot ||\overrightarrow{r}'(t)||dt$
Conceptualized as: Integrand of 1 gives arc length, integrand of $f$ gives mass when density function is equal to $f$
[[Vector Field]] [[Line Integral]]: Dependent on Orientation
$\int_C \overrightarrow{F}\cdot d\overrightarrow{r} = \int_a^b \overrightarrow{F}(\overrightarrow{r}(t)) \cdot \overrightarrow{r}'(t)dt$
Integrand of $\overrightarrow{F}$ gives the work required to move a particle against force field $\overrightarrow{F}$ along C

Relationships between Conservative [[Vector Field]]s and [[Line Integral]]s:
When $\overrightarrow{F}$ is conservative and the region D is simply connected, in 2D that implies that $Q_x = P_y$ and in 3D it implies that $\nabla \times \overrightarrow{F} = 0$. This is because cross [[Partial Derivative]]s are equal; $f_xy = f_yx$. This is "Clairaut's Theorem," a name I haven't heard before this very moment.

This shows path independence, so $\int_C$ is the same regardless of C, so long as the endpoints/boundary points are the same. This is the Fundamental Theorem of Line Integrals, see the [[Line Integral]] note for the exact theorem.

Checking if $\overrightarrow{F} = \nabla f$ for some f, in other words checking for conservatism:
In 2D; check if $Q_x-P_y=0$
In 3D; check if $\nabla \times \overrightarrow{F} = 0$
If either of those two things are false, then you can immediately conclude that no it is not conservative.
If they are true, then check if the region is simply connected, if yes, then it is conservative, and a [[Vector]] Potential $f$ can be found. If the region is not simply connected, then you cannot conclude conservatism or lack thereof with the information you have.

Checking if $\overrightarrow{F} = \nabla \times \overrightarrow{G}$ for some $G$:
if the divergence $\nabla \cdot \overrightarrow{F} = 0$ and domain D is "star-shaped" then you can conclude yes. If the divergence $!=0$ then you can conclude no, if the domain is wrong then you cannot conclude anything.

[[Surface Integral]]s:
[[Parametric Surface]]s $\overrightarrow{r}(u,v)$ are smooth if $\overrightarrow{r}_u \times \overrightarrow{r}_v \neq 0$ on the domain, and orientable if it "has two sides." All surfaces on the exam will be orientable.
The normal vector $\hat{n}=\overrightarrow{r}_u \times \overrightarrow{r}_v$
$(u,v)$ can be any coordinate system

[[Surface Integral]]s of [[Scalar]] Functions:
$\int\int_S fdS = \int\int_D f(\overrightarrow{r}(u,v)) \cdot ||\overrightarrow{r}_u \times \overrightarrow{r}_v||dA$
Defined for smooth surfaces and independent of parameterization.
When the integrand is 1, this finds the surface area. When the integrand is equal to a density, this finds the mass.

[[Surface Integral]]s of [[Vector Field]]s:
Also called Flux Integrals; the exam will probably call them that.
$\int\int_S \overrightarrow{F}\cdot d\overrightarrow{S} = \int\int_D \overrightarrow{F}(\overrightarrow{r}(u,v))\cdot (\overrightarrow{r}_u \times \overrightarrow{r}_v)dA$
Defined for smooth, orientable surfaces.
Sign is orientation-dependent, aka the direction of the normal [[Vector]]. This is determined by the right-hand rule.
"Mass flow rate" across surface S. Flux Integrals will probably be presented out of context, literally just called "flux" because this contextualization is too weird.

Provided:
Fundamental Theorem of [[Line Integral]]s
[[Green's Theorem]]
[[Stokes' Theorem]]
[[Divergence Theorem]]