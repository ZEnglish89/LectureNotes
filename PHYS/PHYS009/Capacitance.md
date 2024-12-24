
A pair of [[Conductor]]s which have differing [[Charge]], and have an [[Electric Potential]] between them, but have 0 net charge, are considered a capacitor.

Each individual conductor is a capacitor's plate.

Capacitance is the amount of [[Charge]] that a capacitor can store at a given [[Electric Potential]] or voltage. The capacitance of a given capacitor is dependent on the shape, size, arrangement, and material of the plates.
Capacitance does not actually depend on the magnitude of the potential difference between the plates. The situation below for a Parallel-Plate Capacitor goes into this, with the derivation of its capacitance equation.

The Capacitance of a Capacitor is $$C = |\frac {Q}{\Delta \phi}|$$
The unit of capacitance is a Farad, and one Farad is one Coulomb per Volt: $$F=\frac {C}{V}$$
1 Farad is a very large amount of capacitance, most capacitors will be operating in microfarads or smaller.

The field between the plates of a capacitor:
$$\vec{E} \approx \frac{|\sigma|}{\epsilon_0}$$
or $$\vec{E} = \frac {Q}{\epsilon_0 A}$$
For a circuit with a Capacitor and a [[Resistor]], the [[Electric Potential]] across the capacitor after the capacitor has been discharged for time $t$ is equal to $$\Delta V = \Delta V_0e^{-t/\tau}$$
Where $\tau = RC$.
If you can find them, look over the notes for 9/20 for more capacitance stuff, I'm rather lost honestly.


With a Parallel-Plate Capacitor with a separation of $s$: $|\vec{E}| \approx |\sigma|/s$ between the plates, and $|\vec{E}| \approx 0$ elsewhere.
You can derive an equation for Capacitance: $$C=\epsilon_0 \cdot \frac{A}{s}$$
where the two plates have area $A$ and are separated by $s$.
Lecture Slides for 09/27 show this derivation.

Using [[Electric Field]]s as storage for energy as discussed in the parallel-plate scenario, capacitors can store energy. They're used for this purpose commonly in everyday life, and when designed efficiently enough they can replace chemical batteries(See batteries section in [[Electric Potential]]).
The energy stored in a capacitor with plate area $A$ and separation $s$ is $$U_e = u_eAs = 1/2C(\Delta\phi)^2$$
This can be rearranged: $$U_e = Q/2\phi = Q^2/2C$$The [[Electric Potential]] within a battery is used to [[Charge]] the two sides of a capacitor.

For a system of Capacitors joined in parallel where the total [[Charge]] is distributed evenly between them, the total capacitance of the system is simply equal to the sum of each capacitor's capacitance:$$\Sigma_1^n C_i$$

When they are instead joined in series, only the topmost and bottommost plates are actually given additional [[Charge]], all other plates must together have net zero charge. The total capacitance can be obtained by adding the reciprocals of each individual capacitance, and then taking the reciprocal of the sum:$$(\Sigma_i^n(C_i)^{-1})^{-1}$$

Parallel and Series capacitors are often combined, and they won't always be in neat rows and columns.
Parallel capacitors can be identified by being fed by the same set of vertexes in a diagram, while capacitors in series can be identified by not having any junctions between them.