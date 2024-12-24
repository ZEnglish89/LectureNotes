
Uhhh it's like [[Flux]] but with [[Magnetism]].
Magnetic Flux is a measurement of the amount of [[Magnetic Field]] lines passing through a given surface area:$$\Phi_B=\int N|\vec{B}|cos\theta d\vec{A}$$
Where $\vec{B}$ is the [[Magnetic Field]], A is the cross-sectional surface area being exposed, $\theta$ is the angle between $\vec{B}$ and $\vec{A}$, and $N$ is the "number of magnetic field lines."
If you have a $90^{\circ}$ angle then you can often get$$\Phi_B = \int |\vec{B}|d\vec{A}$$
If $\vec{B},\theta,d\vec{A}$ are all constant, this simplifies to:$$\Phi_B=N|\vec{B}||\vec{A}|cos\theta$$
Remember that the $cos$ means that this is maximized when the two vectors are $\perp$ and is $=0$ when they are $\parallel$.
Like Electrical [[Flux]], this is a signed scalar quantity and is dependent on the direction of $\vec{B}$ relative to $\vec{A}$.
The units are in $Tm^2=1W$, $W$ is a "weber" and the expression on the left is Tesla-square meters.

This was written in the context of the infinite solenoid situation from [[Faraday's Law]].

The work any non-coulombic [[Electric Field]] does on a carrier as it moves is:$$dW=\vec{F}_e\cdot d\vec{r}$$
The total EMF on a traversal around a loop is:$$\epsilon=W/q = 1/q \cdot \oint q\vec{E}\cdot d\vec{r}=\oint \vec{E}\cdot d\vec{r}$$
Take the following expression on faith as it's beyond the scope of the course to derive.
$$E_{\phi}=-(1/2)\cdot(\partial B_z)/(\partial t)\cdot(R^2/r)$$
Using that, the loop EMF is actually$$\epsilon=-(\partial B_z/\partial t)\cdot\pi R^2$$
Where $\pi R^2$ is the cross sectional area of a solenoid.

With a bit more messing around, you can express the whole thing as$$\epsilon=-d\Phi_B/dt$$