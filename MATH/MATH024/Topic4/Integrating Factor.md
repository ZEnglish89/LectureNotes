
Can be reliably used to solve First-[[Order]] [[Linear]] [[Differential Equation]]s. Specifically that type, higher-order does not work for this technique.
The Equation can be written as: $$y' + p(t)y = f(t)$$
For the case where $p(t) = a$ and $a$ is a constant, the integrating factor will always be $e^at$.
1: Find an Integrating Factor: $\mu(t) = e^{\int p(t)dt}$
2: Multiply the [[Ordinary Differential Equation]] by $\mu (t)$ on both sides.
3: Left hand side will always be $d/dt(\mu y)$, so integrate both sides to isolate y.
4: Isolate y.

$ty' + y = d/dt(ty)$

$\mu y' + p(t)\mu y = \mu q(t)$

Separate: $\mu' = p(t)\mu$
$d\mu/dt = p(t)\mu$
$\int(d\mu/\mu) = \int p(t) dt$
$\mu = e^{\int p(t)dt}$
$\mu ' = e^{\int p(t)dt} \cdot p(t) = \mu(t)p(t)$

$y' + p(t)y = q(t)$
$\mu = e^{p(t)dt}$

$\mu y' + p(t)\mu y = \mu q(t)$
$\mu y' + p(t)\mu y = \mu q(t)$
$d/dt(\mu(t) y(t)) = \mu(t)q(t)$
This sequence has isolated y, we had a y-term and a y' term and now we only have a $y(t)$ term.

This can be written more concisely:
For any First-[[Order]] [[Ordinary Differential Equation]] which may be written in the form:$$y'+p(t)y=q(t)$$
the Product Rule and the Integrating Factor Method provide that $$\mu y = \int{\mu q(t)dt}$$
Where $\mu = e^{\int{p(t)dt}}$.
You can find $p(t),q(t)$ and $\mu$, and then just write out the above equation, evaluate the integral, and divide by $\mu$ to solve for $y$.

$dy/dt + (2ty) = t$ This is a [[Linear]] First-[[Order]] [[Ordinary Differential Equation]]
Identify p(t) and q(t):
$p(t) = 2t$ $q(t) = t$
Determine integrating factor:
$\mu = e^{\int p(t)dt} = e^{\int 2tdt} = e^{t^2}$
Multiply all terms by integrating factor:
$e^{t^2}dy/dt + 2te^{t^2}y = te^{t^2}$
Write left side as derivative:
$d/dt(y \cdot e^{t^2}) = te^{t^2}$
Integrate right side:
$ye^{t^2} = \int te^{t^2}dt +c$
Solve integral and use algebra to isolate y:
$ye^{t^2} = 1/2 e^{t^2} + c$
$y = 1/2 + ce^{-t^2}$
