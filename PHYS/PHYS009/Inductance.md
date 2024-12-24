
Inductors act as storage devices for the energy contained within a [[Magnetic Field]], the same way that [[Capacitance]] allows energy storage for [[Electric Field]]s. Kinda.
$$|\epsilon|=L|\frac{di}{dt}|$$

Inductance of a solenoid:$$L_{sol}=\mu_0\pi r^2\cdot \frac{N^2}{l}$$
Connect a coil with significant inductance L and a [[Resistor]] to a battery.

The solution with a discharging Inductor or a discharging Capacitor([[Capacitance]]) are based on a decaying exponential.$$I(t)=I_0[1+e^{-\frac{R}{L}t}]$$
For Charging:$$I(t)=I_0[1-e^{-\frac{R}{L}t}]$$

LC(Inductor-Capacitor) Circuits:

When hooked up together, a capacitor will drive [[Current]] through an inductor, which will convert that current into a [[Magnetic Field]]. Because this field will be increasing, then the system will have an increasing amount of [[Magnetic Flux]], which will cause [[Faraday's Law]] and [[Lenz's Law]] to create an opposing magnetic field via an opposing current.

At time $t=0$ the capacitor is fully charged and no circuit is flowing.
As the capacitor discharges, current is pushed through the inductor's coils, and the above happens.
When the capacitor hits zero [[Charge]], the current within the coil reaches a maximum.
The inductance will continue to push current though, overshooting an equilibrium point, and will push current back to the capacitor, recharging it but in the opposing direction.
By this process, magnetic energy is channeled back into electrostatic energy in the capacitor, until the capacitor reaches a critical charge, at which point it begins to discharge back into the inductor, and we go again.

As such, LC circuits will oscillate. With no resistance, that oscillation will be endless.

A coil with emf $\epsilon_L$ as if it were a battery with the same emf. That is equivalent to the [[Electric Potential]] difference of the capacitor plates:$$\frac{Q}{C}=L\cdot \frac{di}{dt} -> \frac{Q}{LC}=\frac{di}{dt}$$
Using $$i=-\frac{dQ}{dt}$$
This becomes:$$\frac{d^2Q}{dt^2}=-\frac{Q}{LC}$$
This can be considered in the exact same way as the oscillation of a spring:$$\frac{d^2x}{dt^2}=-\frac{k_s}{m}\cdot x$$
[[Charge]] is position, 
When $t=0$ and $Q$ is maximal:$$Q(t)=Q_0cos(\omega t)$$ where $\omega = \frac{1}{\sqrt{LC}}$.
Feeding energy into such a circuit is a relatively efficient way to generate a steadily oscillating signal, which is extremely useful for lots of different forms of wireless communication.