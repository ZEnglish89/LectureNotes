Relative position, velocity, and acceleration equations for 2D:

Position: $R_B=R_A+R_{B/A}$ 
Velocity: $V_B=V_A+(\omega \times R_{B/A})$
Acceleration: $a_B=a_A+(\alpha \times R_{B/A})-(\omega^2R_{B/A})$

Lower-case omega $\omega$ is rotational velocity
Lower-case alpha $\alpha$ is rotational acceleration

If given one of the equations as a polynomial, like velocity $v=t^2-6t-15$, you can integrate and differentiate to move to the other equations.
So velocity is the integral of acceleration, which is the derivative of velocity.
Position/displacement is the integral of velocity, which is the derivative of displacement, and so on.

The constant $C$ that comes from integration is the starting position/velocity. Position therefore includes the $C$, but displacement only cares about the *change* in position and thus ignores the $C$.

Velocity does care about the $C$, but it's likely that the problem will give the initial velocity, as there isn't really a way to find the $C$ constant using calculus.