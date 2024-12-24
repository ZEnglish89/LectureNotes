The expression below was introduced in [[Faraday's Law]] and [[Magnetic Flux]], but supposedly it belongs here.
$$\epsilon=-\frac{d\Phi_B}{dt}$$

This law states that the [[Magnetic Field]] created by flowing [[Current]] induced by an "invading" Magnetic Field will be in the opposing direction of that original Field.

The expression for the [[Magnetic Flux]] of a [[Magnetic Field]] is equal to $$\Phi_M=|\vec{B}||\vec{A}|cos(\theta)$$
Where theta is the angle between the field and the surface.
In the case of a solenoid, you also multiply by $N$ where the solenoid has $N$ coils:$$\Phi_M=N|\vec{B}||\vec{A}|cos(\theta)$$
When taking the time-derivative, if the surface is rotating at angular velocity $\omega$, then $\theta=\omega\cdot t$, and you need to use the chain rule when taking the derivative, which gives you:$$\Phi_M = \omega N|\vec{B}||\vec{A}|sin(\omega t)$$ When I had a question about the homework, they said that angular speed was $f$, and they wanted angular frequency $\omega=2\pi f$? I don't know what that was about, but keep an eye out for that conversion.
Ah! It's because the question was asking for the maximum EMF, which as per [[Faraday's Law]] requires the maximum Flux, so it only occurred when the $sin$ term was equal to 1, which only happens every $2\pi$ rads. So I at least partially see where that comes from.

More broadly, this means that [[Current]] induced by a [[Magnetic Field]], and the Field created by that current, and the EMF in the system, will always oppose the derivative of that Magnetic Field, acting to stabilize the system or attempt for equilibrium.

This means that attempting to drive a bar magnet through a conducting loop will cause the loop to create a Magnetic Field which repels the bar, not allowing it to pass through.

That negative sign is critical, as if this expression were positive then it would create a positive feedback loop, creating kinetic energy from nothing, and therefore violating thermodynamics.

This might be how magnetic brakes on roller coasters work?

Pushing or Pulling a [[Conductor]] through a [[Magnetic Field]] therefore has a force opposing it, and as such that action requires work equal to the product of that force and the distance the object is moved.