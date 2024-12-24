
This is similar but different to the [[Electric Field]].
See [[Magnetism]].
An electrostatic interaction between two charged objects:
Each point in space has an associated Magnetic Field vector $\vec{B}$, and $\vec{B}$ is the direction of a compass needle at that point.
What's really cool about that is that with a magnet and a whole bunch of compasses, you can physically see magnetic fields.
$$\vec{F}_m = q(\vec{v}\times\vec{B})$$
Is the force of [[Magnetism]] that acts on a [[Charge]]d particle $q$ with velocity $\vec{v}$ at a point in space with Magnetic Field $\vec{B}$.
Because of the way cross products work, this means that the force will always be perpendicular to both the particle's existing motion and the direction of the field.
$\vec{B}$ obeys the superposition principle: $$\vec{B}=\vec{B}_1+\vec{B}_2+\vec{B}_3...$$

Units: $N\cdot s/C\cdot m=1T$, Tesla.
1 Tesla is a product of a very powerful magnet, just like how 1 Farad is a shitload of [[Capacitance]]. We'll be working with smaller numbers.
1 Gauss = $10^{-4}$ Tesla
$\mu_0$ gets used an awful lot on this topic. It is the magnetic permeability of a vacuum, and is equal to$$\approx(1.257 \cdot10^{-6})\frac{N}{A^2}$$
Those units are "Newtons per square Amperes" and frankly I don't understand how exactly that translates. However, the value gets used a lot so it's useful to have written down. Additionally, my TI-36X Pro has it in the Constants menu, although the $\mu$ looks a little bit vestigial.

For a free particle with charge $q$ moving with initial velocity $\vec{v}$ through a Magnetic Field $\vec{B}$ with movement constrained to a circle of Radius R: $$|q\vec{v}||\vec{B}|=|\vec{F}_m|=m|\vec{a}|=m\cdot\frac{|\vec{v}|^2}{R}$$
The first expression is related to Force, which is then expanded out using Newton's second law and a PHYS008 equation relating to centripetal motion.

Therefore: $$R=\frac{|\vec{p}|}{|q||\vec{B}|}$$
Where $p$ is momentum, $p=mv$, or$$R=\frac{mv}{q\vec{B}}$$
If $T$ is the time taken to make one full orbit:
$$T=\frac{2\pi R}{|\vec{v}|}=\frac{2\pi m}{|q||\vec{B}|}$$
Interestingly, $T$ is not dependent on the particle's initial speed.
And therefore: $$f=\frac{1}{T}=\frac{|q||\vec{B}|}{2\pi m}$$
$f$ is the **cyclotron frequency** within the field, how many revolutions are made per second. Frequency is measured in Hertz, Hz, where Hz is once per second. This is stuff that's relevant to particle accelerators.
This comes from PHYS008 stuff, regarding motions and orbits under gravity.

Under the [[Drude Model]], everything we've discussed above implies that Magnetic Fields should apply forces to wires which are carrying [[Current]], because the Drift Velocity of the current carriers is $\vec{v}$ in the above equations.
The force applied to a straight-line segment of a wire is represented as: $$\vec{F}_{m,seg} = (nLAq)\vec{v}_d\times\vec{B}$$
Which can be simplified to: $$\vec{F}_{m.seg}=L(\vec{I}\times \vec{B})$$
For variable definitions look to my notes on [[Current]], [[Current Density]], and the [[Drude Model]].
This is limited in that the wire segment must be straight, thin, in [[Dynamic Equilibrium]], and short enough that $\vec{B}$ is uniform over it.
This implies that $\vec{F}_{m,seg}$ acts $\perp$ to the Current and the Field.

To compute the total Magnetic Force along the length of a curved wire, you divide into small segments, and sum the force contributions from each of them.

Magnetic Torque on a Loop:
Can be parameterized for $$\vec{\mu}=NI\vec{A}$$
Where $\vec{\mu}$ is a magnetic moment vector in terms of the [[Current]] $I$ flowing in the loop and the tile vector $\vec{A}$
This expresses how strongly a loop of any shape responds to a Magnetic Field. $$\vec{\tau}=\vec{\mu}\times \vec{B}$$

Potential Energy of a Loop:$$V_m=-|\vec{\mu}||\vec{B}|cos\theta=-\vec{\mu}\cdot\vec{B}$$
Magnetic Field of a loop off the axis:$$|\vec{B}|=\frac{\mu_0IR^2}{2(x^2+R^2)^{\frac{3}{2}}}$$
Can be rewritten as:$$|\vec{B}|=\frac{\mu_0}{4\pi}\cdot\frac{2|\vec{\mu}|}{|\vec{r}_{PD}|}$$
Ugh too fast again, that most recent equation is missing something on the right-most term.
Magnetic Field of two circular Loops:$$\vec{B}_{tot}=\vec{B}_{left}+\vec{B}_{right}=(\mu_0IR^2/2((R/2)^2+R^2)^{3/2})+(\mu_0IR^2/2((R/2)^2+R^2)^{3/2})=(2\mu_0I/2)\cdot(R^2/((5/4)\cdot R^2$$
Ugh that's such a long equation and he moved on too quickly still. The right-most term is incomplete.

At a significant distance from the Loop, the Magnetic Field Vectors will be similar to those created by a bar magnet(with the loop wrapped around the boundary between the magnet's poles), which is also similar to the [[Electric Field]] of a [[Dipole]].

Magnetic Field of a moving [[Charge]]: $$\vec{B} = \frac{\mu_0}{4\pi}\cdot\frac{q}{|\vec{r}_{PS}|^2}\cdot(\vec{v}\times\hat{r}_{PS})$$
This describes the magnetic field vector $\vec{B}$ created at point $P$ by a particle with charge $q$ moving at velocity $\vec{v}$. $\vec{r}_{PS}$ is the position of $P$ relative to the source particle, and $\hat{r}_{PS}$ is the unit vector in the direction of P.
Double check this^ He moved on while I was still typing.

This is the Biot-Savart Law, normally written as:$$\vec{B}=\frac{\mu_0}{4\pi}\cdot\Sigma\frac{dL}{|\vec{r}_{Pi}|^2}\cdot(\vec{E}\times\hat{r}_{Pi})$$
Magnetic Field $\vec{B}$ produced at point $P$ by a uniform but arbitrarily shaped wire carrying a [[Current]] $I$, assuming the wire has been divided into segments, $dL$ is the length of the $i$th segment, $\vec{r}_{Pi}$ is the distance from point $P$ to the $i$th segment, and $\hat{r}_{Pi}$ is the unit vector of that distance.

For an infinite wire, that is:$$\vec{B}=\frac{\mu_0}{4\pi}\cdot\Sigma\frac{dx}{|\vec{r}_{Pi}|^2}\cdot I\cdot sin\theta_i$$
This can turn out to be very similar to the infinite wire case for an [[Electric Field]], and can be simplified to:$$|\vec{B}|=\frac{\mu_0I}{2\pi r}$$
Two parallel [[Current]]-carrying wires will attract if their current flows in the same direction and repel if the directions oppose.
The force the wires exert on each other is:$$|\vec{F}_{m}|=|L_2\vec{I}_2\times\vec{B}_1|$$
$$|\vec{F}_{wires}|=\frac{\mu_0LI_1I_2}{2\pi r}$$
Where the two wires have currents $I_1$ and $I_2$ and are separated by distance $r$.

A rotating conducting disk with radius $R$ at rotational velocity $\omega$ in a Magnetic Field $\vec{B}$ will have [[Electric Potential]] or EMF which is:$$\frac{\omega\cdot\vec{B}R^2}{2}$$
Remember that EMF is equal to work per [[Charge]], or $\frac{W}{Q}$.

The Magnetic Field of a circular loop with current $I$ and radius $R$: $$|\vec{B}|=\frac{\mu_0I}{2R}$$
Magnetic Field of a Solenoid, as per [[Ampere's Law]]:$$|\vec{B}|=(\mu_0NI)/L$$
This is a solenoid with $N$ turns of wire, total wire length $L$. $i_{enc}=+NI$.

The power lost by driving [[Current]] through a [[Resistor]] is equal to $$U^{th}=1/2\cdot LI_0^2$$
This is still solenoid-specific.
Solenoid Volume is $(\pi R^2)L$
Using the power and the volume, Energy Density of the solenoid is $$u_B=|\vec{B}_0^2|/2\mu_0$$
Recall that $$u_e=\epsilon_0|\vec{E}_0|^2/2$$
And $$u_{EM}=(\epsilon_0/2)\cdot(|\vec{E}|^2+|\vec{B}|^2)$$
Fuck you mean "recall?" This is entirely new nonsense. Just random characters mashed together.