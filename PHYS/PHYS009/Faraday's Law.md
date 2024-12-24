
This links the EMF "induced" in a closed loop to the rate of change in the [[Magnetic Flux]] through an area enclosed by the loop.
This creates a uniform [[Magnetic Field]] $\vec{B}$.

Consider an infinite cylindrical solenoid with inner radius $R$.

If you assume that the current within that solenoid varies with time:
Then Faraday's law states that the dynamic [[Magnetic Field]] must be correlated with an [[Electric Field]] that satisfies the following conditions:$$\vec{\nabla}\times\vec{E}+\frac{\partial\vec{B}}{\partial t}=0$$
Also written as:$$\vec{\nabla}\times\vec{E}=-\frac{\partial\vec{B}}{\partial t}$$
Those nablas are yet another thing that's asking me to look back at Math023, unfortunately. I think those are Curl? I'm not entirely sure.

This predicts the tendency for a [[Current]] to "swirl" around a given point.

We do a bit of messing about in [[Magnetic Flux]] and we eventually get to this statement, which is a whole bunch of shit:$$\epsilon=-\frac{d\Phi_B}{dt}=IR=-\frac{\partial I_B}{\partial t} = -\frac{\partial(\vec{B}\cdot\vec{A})}{\partial t}$$
The left-most expression is [[Lenz's Law]].

Moving a [[Conductor]] through a [[Magnetic Field]] requires work equal to the Force exerted on it multiplied by the distance it is moved: $$W=\int Fdx$$
According to the homework, a changing [[Magnetic Field]] will induce an [[Electric Field]] according to:$$\int(\vec{E}\cdot d\vec{s})=-\frac{d\Phi_B}{dt}$$
Don't know what's up with that but I'll take the equation I suppose.

A Faraday LC circuit (See [[Inductance]])provides an AC [[Current]]: an oscillation with a sinusoidal time-derivative.
AC voltage([[Electric Potential]]):$$\epsilon(t)=\epsilon_0sin(\omega t)$$ and Current:$$i=I_0sin(\omega t)$$
With a [[Resistor]]: $$\epsilon_R(t)=\epsilon_0sin(\omega t)$$
$$i_R(t)=\frac{\epsilon_0}{R}\cdot sin(\omega t)=I_0sin(\omega t)$$
The [[Resistance]] is a modifier. Very slight resistance will increase [[Current]], whereas significant resistance will decrease it.
[[Charge]] given by $Q=C\phi$:$$q(t)=C\phi(t)=C\phi_0sin(\omega t)$$
$$i_C(t)=\frac{dq(t)}{dt}=\omega C\phi_0cos(\omega t)=I_0cos(\omega t)$$
and $$I_0=\omega C\phi_0$$
This can be put in terms of sin instead of cos with a 90 degree phase-shift:$$i_C(t)=I_0sin(\omega t+\pi/2)$$
The **Capacitive Reactance** of a capacitor([[Capacitance]]):$$\frac{\epsilon_0}{I_0}=\frac{1}{\omega C}=\mathbb{X}_C$$
That X might need to be written differently. It's in a curly/cursive font, rather than the blackboard.
Capcitive Reactance in AC [[Current]] is analogous to [[Resistance]] in DC [[Current]].

With AC, the average value of [[Current]] and [[Electric Potential]] will be 0, because of the oscillation. Instead, root-mean-squared is used to deal with those negatives.
You're moving things back and forth rapidly and repeatedly, so you're net moving nothing, but stuff is in fact getting moved, so you need to account for that total motion by using RMS.
$$I_{rms}=\frac{I_0}{\sqrt{2}} -> $$

AC circuits with a [[Resistor]]: The EMF can be given by $$\epsilon_{ind}=-L\cdot \frac{di}{dt}$$ and $$\Delta \epsilon_L(t)=L\cdot \frac{di_l(t)}{dt} -> \frac{di_L(t)}{dt}=\frac{\epsilon_0}{L}sin(\omega t)$$
$$i_L(t)=\frac{\epsilon_0}{\omega L}\cdot sin(\omega t-\frac{\pi}{2})=I_0sin(\omega t-\frac{\pi}{2})$$
The Inductive reactance of the inductor:$$I_0=\frac{\epsilon_0}{\omega L} -> \frac{\epsilon_0}{I_0}=\omega L =\mathbb{X}_L$$
