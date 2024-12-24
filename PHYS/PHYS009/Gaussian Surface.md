Imaginary surfaces which enclose [[Charge]]s to make [[Gauss's Law]] easier to calculate.

Type Z: The [[Electric Field]] and [[Flux]] are 0 for every section.
Type P: The [[Electric Field]] is perpendicular for every section, so there is no [[Flux]].
Type CC: The [[Electric Field]] is in the same/opposite direction as the surface for each section and has no magnitude everywhere, this maximizes [[Flux]] at $+-|\overrightarrow{E}||d\overrightarrow{A}|$

Common types:
Plane: Causes planar [[Charge Distribution]] for a Unidirectional [[Electric Field]]
Gaussian Rectangle: Four Faces parallel, two perpendicular. The parallel ones are type P, the perpendicular ones are type CC.
Cylindrical: Causes axial [[Electric Field]]s with a curved surface providing type CC and end caps providing type P.
Spherical: Causes radial [[Electric Field]]s. A Gaussian Sphere has a single panel of type CC.

For spherical shells of [[Charge]], the Charge is located on the outer surface. As such, the Gaussian surface will either have a smaller radius than the shell, enclosing no charge and having no [[Electric Field]] and no [[Flux]], or it will have a larger radius than the shell, enclosing all of the charge, having the full field and full flux.

For the case of an infinitely long rod with uniform [[Charge]]  density $\lambda$ projecting $\vec{E}$ radially outward, you can take a cylindrical Gaussian Shell so that $|\vec{E}|$ is constant over the surface of the shell.

As per [[Gauss's Law]] $$\Phi_E = \pi r^2E_1cos\theta _1+(2\pi rL)E_2cos\theta _2 + \pi r^2 E_3 cos\theta_3$$
This equation simplifies down to $$(2\pi rL)E_2$$
Which can be set equal: $$(2\pi rL)E_2 = \frac{\lambda L}{\epsilon_0}$$
and solved for E: $$E = \frac{\lambda }{ 2\pi \epsilon_0 r}$$

For an infinite plane of charge, you can use a Gaussian Pillbox, and eventually $$\Phi_E = 2EA = \frac{\sigma A}{\epsilon_0}$$
Solved for E $$E = \frac{\sigma}{2\epsilon_0}$$
Positive if $x>0$, negative otherwise.

For a non-conducting Solid Sphere where the Gaussian Surface doesn't cover the entire sphere, i.e. $r<=R$:
$$\Phi_E = \frac{4\rho \pi r^3}{3\epsilon_0}$$
$$E=\frac{\rho r}{3\epsilon_0}$$
I no longer have it in me to break everything down from the beginning and do all the algebra, Borna is killing me rn. I'll just include the useful final equations.

If the Surface does cover the entire sphere, i.e. $r>=R$: $$\Phi_E = \frac{Q}{\epsilon_0}$$
$$E=\frac{k_eQ}{r^2}$$
