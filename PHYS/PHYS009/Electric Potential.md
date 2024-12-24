
As opposed to Vector Fields, electric [[Electric Field]]s may also be understood in terms of Scalar Fields 
$\Phi (x,y,z)$ is a scalar function of position.

Example of a topographical map in class, I'm not sure if I understand the analogy.

Scalar Fields represent "the total amount of energy required to change between locations."

The Electrostatic Potential Energy of a system of point charges is the work needed to bring the charges from an infinite separation to their final positions.

$W_{ext} = \vec{F}_{ext} \cdot \Delta \vec{r}$
$\vec{F}_e = q\vec{E} = \frac{kqQ}{r^2} \cdot \hat{r}$

Bringing a single particle in requires no energy, because there is no force acting against it.
However, bringing a particle into a system which already has [[Charge]] will require energy, because the existing Charge will exert a force of some kind on it.

For a three-point system, you need $W_{12} + W_{13} + W_{23}$: The work done by particle 1 on particle 2, by particle 1 on particle 3, and by particle 2 on particle 3.
The 1,2,3 is the particles numbered in the order in which they entered the system. Basically, you need to sum every possible pair of particles.

Adding additional particles will greatly increase the work, because each new particle is acted on by *every* existing one.

$\vec{F}_e$ is conservative, so $\Delta K = -\Delta V$
The kinetic energy must change by the same magnitude in the opposite direction of the change in the potential energy.

The total potential energy associated with a set of fixed charges is:
$$V_e = \frac{q}{4\pi \epsilon_0} \cdot \frac{Q_i}{|\vec{r}_i|}$$
For a movable particle with charge $q$ and fixed charges $Q_i$
$\vec{F}_e = q\vec{E}$
Important to note that above is a Scalar Quantity with linear dependence on $Q$ and $\vec{r}$.
It is also signed, it can possibly be negative.
As $r->\infty$, $V_e -> 0$
If $V_e < 0$, the force is repulsive; separating the charges.
If $V_e>0$, the force is attractive; bringing the charges together.

Electric Potential $\phi_E$
$$V_e = \phi_e = \frac{q}{4\pi \epsilon_0} \cdot \frac{Q_i}{|\vec{r}_i|}$$
$$\Phi (x,y,z) = \frac{V_e(x,y,z)}{q}$$

This needs a fixed [[Charge Distribution]] and $V_e$ and $\phi$ need well-defined values.
The SI Unit is Volts, where $1V = 1J/C$, one Volt = One Joule per Coulomb.
The strength of a [[Electric Field]] between two plates with known voltage between them is $E = \frac{V}{d}$, or the voltage divided by the distance between the plates.

Electric [[Electric Field]] to Electric Potential: $$\Delta \phi = \int d\phi = -\int \vec{E} \cdot d\vec{r}$$
When moving in a straight line from A->B through a [[Electric Field]], the Potential is 0, but when moving in a circular path $\Delta \phi <0$

Potential to [[Electric Field]]: $$\vec{E}(x,y,z) = -\vec{\nabla}\phi(x,y,z)$$
Remember Gradient Vectors from Math023.
$$\vec{E} = -\frac{\partial\phi}{\partial x}$$

For energy storage, see [[Capacitance]] and the section of [[Electric Field]] on carriers of energy.

Batteries use chemical reactions to separate [[Charge]]s to generate electric potential and therefore store energy, the work done to separate their charge is called the EMF, Electro Motive Force, or $\mathcal{E}$, and for ideal theoretical batteries $\mathcal{E} = \Delta\phi$
When actually used in a [[Circuit]] so [[Current]] is flowing with [[Resistance]], the relation is$$\Delta\phi = \mathcal{E}-IR$$When products use multiple batteries, the electric potential within each battery can be summed.

This electric potential can then be used to Charge the two sides of a capacitor, granting it [[Capacitance]].

