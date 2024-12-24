
An application of [[Faraday's Law]]. Borna claims they are among the most important modern applications of it.

Any electrical device which uses [[Faraday's Law]] to transfer electrical energy from one coil to another while giving you control over the EMF.
These devices allow wide-scale distribution of electrical power.
Human's external skin has [[Resistance]] on the order of $10^4\Omega$, but conditions can bring that much smaller, and internal organs have exceptionally low resistances. Due to [[Ohm's Law]] and the fact that a [[Current]] as low as $0.1A$ can be lethal, that puts a hard cap on the quantity of [[Electric Potential]] that a person can be exposed to.

However, transporting power at low Voltage is problematic in its own way: $$P=|\epsilon|I$$
Power is equal to EMF by Current. When passing a Power $P_0$ through a wire to a destination load [[Resistor]](See slides for 11/01-2024), the amount of power which reaches your destination is equal to $$P_L=1-\frac{I^2R}{P_0}$$
So transferring power at a high [[Current]] is undesirable, and increasing the EMF or Voltage allows you to transfer the same power at a lower Current.

Transferring power at high [[Current]] is expensive and inefficient, but transferring Power at high Voltage is dangerous. With Transformers, you can transfer high-voltage low-current power for long distances where humans won't come into contact with it and ensure that the power isn't wasted, but once you get closer to human contact you can lower the voltage in order to have it reach its destination in a safer form.

Consider two independent long skinny solenoid-like coils of wire:
1. One "Primary" solenoid of $N_1$ turns wrapped around a cylindrical form of radius $R$ and length $l$.
2. One "Secondary" coil of $N_2$ turns wrapped around directly on top of the first.

Connecting the primary coil to an AC source will give it a sinusoidal [[Current]], and subsequently a [[Magnetic Field]] based on that sinusoidal function.

Primary is connected to a source: $\epsilon_{src}(t)=$
Secondary is initially unconnected.

The current oscillates and creates $B_{ind}$
[[Faraday's Law]] incudes oscillating opposing EMF in both coils.$$\epsilon_{src}(t)\approx \epsilon_1(t)$$
Where the RHS of that equation is the EMF Induced in the primary coil.
Remember that $$\epsilon_{turn}=-d\Phi_B/dt$$
The total EMF induced in the primary and secondary coils are the sums of the EMF induced in each coil:$$\epsilon_1=N_1\epsilon_{turn}$$
And $$\epsilon_2 = N_2\epsilon_{turn}$$
Where $\epsilon_1$ is the EMF in the Primary and $\epsilon_2$ is the EMF in the Secondary.
These equations can be solved for: $$\frac{\epsilon_1}{N_1}=\epsilon_{turn}=\frac{\epsilon_2}{N_2}$$
And therefore:$$\epsilon_2=(\frac{N_2}{N_1})\epsilon_1$$
This means that by constructing a Transformer with whatever values of $N_1$ and $N_2$ you want, you have almost complete control over the $\epsilon$ values.
Some equations for the operation of a transformer:$$L\cdot \frac{di_1}{dt} = \epsilon_1(t)=\epsilon_0sin(\omega t)$$
With a bit more work on this topic, the EMF jump can be found to lag behind by roughly one quarter cycle, or $\pi/2$ radians.
I lost it a bit at the end there, but the conceptual bits make sense.