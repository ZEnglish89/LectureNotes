
The Simple Harmonic Oscillator equation is$$mx''+bx'+kx=f(t)$$
which is a [[Second-Order Linear Ordinary Differential Equations with Constant Coefficients]].$$m>0,b\geq0,k>0$$
If $b=0$, we say in a physics context that the system is "undamped." Otherwise, it is considered "damped."
If $f(t)=0$ then the equation is homogeneous, or unforced, undriven, or free. Otherwise it is forced, or driven.

For cases, look to [[Second-Order Linear Ordinary Differential Equations with Constant Coefficients]]: Case 1 is $\Delta>0$, Case 2 is $\Delta=0$, Case 3 is $\Delta<0$, where $\Delta$ is the "Discriminant."

For Case 3 with $b=0$:
$$mx'' + kx = 0 -> x=-\frac{k}{m}x$$
$$x(t)=\tilde{c}_1cos(\omega_0t)+\tilde{c}_2sin(\omega_0t)$$
where $\omega_0 = \sqrt{\frac{k}{m}}$.
Using the identity $$cos(A+B)=cos(A)cos(B) + sin(A)sin(B)$$
You can turn $x(t)$ into:$$x(t)=Acos(\omega_0t-\delta)$$
where
1. $A$ is the amplitude of the oscillation.
2. $\delta$ is the phase angle.
3. $\omega_0$ is the angular frequency or circular frequency.
4. $f_0=\frac{\omega_0}{2\pi}$ is the natural frequency or just frequency, measured in Hz.
$$Acos(\omega_0t-\delta) = Acos(\omega_0t)cos(\delta) + Asin(\omega_0t)sin(\delta)$$
Therefore, $Acos(\omega_0t)cos(\delta) = \tilde{c}_1cos(\omega_0t)$ and $Asin(\omega_0t)sin(\delta)=\tilde{c}_2sin(\omega_0t)$, and therefore again, $$\tilde{c}_1=Acos(\delta)$$
and $$\tilde{c}_2 = Asin(\delta)$$
As an aside, $A^2 = \tilde{c}_1^2+\tilde{c}_2^2$ and $tan(\delta)=\frac{\tilde{c}_2}{\tilde{c}_1}$

For Case 3 with $b\neq0$:$$x(t)=e^{-\frac{b}{2m}t}\cdot(c_1e^{\frac{\sqrt{\Delta}}{2m}t}+c_2e^{-\frac{\sqrt{\Delta}}{2m}t})=e^{-\frac{b}{2m}t}(\tilde{c}_1cos(\omega_0t)+\tilde{c}_2sin(\omega_0t))$$
Because $\Delta<0$ we can define $\alpha=-\frac{b}{2m}$ and $\beta=\frac{\sqrt{-\Delta}}{2m}=\omega_d=\frac{\sqrt{4mk-b^2}}{2m}$ and get$$x(t)=A(t)cos(\omega_dt-\delta)$$
where $A(t)$ is the time-dependent amplitude: $A(t)=Ae^{-\frac{b}{2m}t}$.
1. $\delta$ is the phase angle
2. $\omega_d=\frac{\sqrt{4mk-b^2}}{2m}$ is the circular or angular quasi-frequency.
3. $f_d=\frac{\omega_d}{2\pi}$ is the natural quasi-frequency.
4. $T=\frac{1}{f_d}$ is the quasi-period.
5. $\tau = \frac{2m}{b}$ is the time constant, such that $e^{-\frac{b}{2m}t} = e^{-\frac{t}{\tau}}$.
When solving problems in this form, assume a solution of the form $x=e^{\lambda t}$, write out $x'$ and $x''$ so you know what you're working with, and plug them back into the original $mx''+kx+x=b$ equation.
You can then use the quadratic equation to solve for $\lambda$, giving you the roots $\lambda_1$ and $\lambda_2$.
Then your solution will match the original form from the start of the case above, where $\lambda_1=(-\frac{b}{2m}+\frac{\sqrt{\Delta}}{2m})$ and $\lambda_2=(-\frac{b}{2m}-\frac{\sqrt{\Delta}}{2m})$.
Yes this sucks really badly, but there is some sort of method to this nonsense.
Once you've done that, you just need to solve for the constants $c_1$ and $c_2$ and then you're done. When solving for the constants, it's not recommended to use that above form, and instead it's better to use the non-factored form$$x(t)=c_1e^{\lambda_1t}+c_2e^{\lambda_2t}$$
Which allows you to use the $x(0)$ and $x'(0)$ initial conditions to help solve.
The hard part is the last bit of solving for the constants at the end, because it will often require you to solve a [[MATH024/Topic6/System|System]] using [[MATH024/Topic7/Determinant|Determinant]]s.

For Case 2, that is $\Delta = 0$, referred to as "Critically Damped Motion:"

You can assume a solution of the form $x(t) = e^{\lambda t}$ again, and it will work it's way through:$$(m\lambda^2+b\lambda+k)e^{\lambda t} = 0$$
$$m\lambda^2+b\lambda+k$$
And that's the quadratic again, but remember that $\Delta=0$ and $\Delta=b^2-4mk$
The quadratic gives you $x(t)=Ce^{-\frac{b}{2m}t}$ which is a problem because... ? He didn't explain it. I'm assuming that it has something to do with the $\Delta=0$.
From $\Delta=b^2-4mk$, $b=2\sqrt{mk}$
So the original equation can be rewritten as $$mx''+2\sqrt{mk}x'+kx=0$$$$(\sqrt{m}\frac{d}{dt}+\sqrt{k})^2x=0$$$$(\sqrt{m}\frac{d}{dt}+\sqrt{k})(\sqrt{m}\frac{d}{dt}+\sqrt{k})x=0$$$$\sqrt{m}\frac{dy}{dt}+\sqrt{k}y=0$$
By [[Separability]], $\frac{dy}{dt}=-\sqrt{\frac{k}{m}}y$ and therefore $y=Ce^{-\sqrt{\frac{k}{m}}t}$
Which allows you to set up $$\sqrt{m}\frac{dx}{dt}+\sqrt{k}x=Ce^{-\sqrt{\frac{k}{m}}t}$$
Which may be solved via the [[Integrating Factor]] method, eventually giving $$x(t)=(\tilde{C}+\tilde{D})e^{-\sqrt{\frac{k}{m}}t}$$
which leads to the two solutions$$[e^{-\sqrt{\frac{k}{m}}t},te^{-\sqrt{\frac{k}{m}}t}]$$
Using $\frac{b}{2m}=\frac{2\sqrt{mk}}{2m}=\sqrt{\frac{k}{m}}$ the solution is $$c_1e^{-\frac{b}{2m}t}+c_2te^{-\frac{b}{2m}t}$$
And BOOM $\lambda =-\frac{b}{2m}$ so the final solution will be:$$x(t)=c_1e^{\lambda t}+c_2te^{\lambda t}$$
The solution for critically damped motion will ALWAYS be of that form.
You can solve for the constants if you have an [[Initial Value Problem]].

In this case, the function $x(t)$ will only cross the $t$ axis one time, at the point $t=-\frac{c_1}{c_2}$.

Finally, Case 1, where $\Delta>0$, referred to as Overdamped Motion.
$\lambda = \frac{-b \pm \sqrt{b^2-4mk}}{2m}$ where $\lambda_1$ is the positive root and $\lambda_2$ is the negative root.
Simply enough, we get:$$x(t)=c_1e^{\lambda_1 t}+c_2e^{\lambda_2t}$$
Depending on the Initial Condition, the solution crosses the $t$-axis at most once.

In summary:$$mx''+bx'+k=0$$ gives the characteristic equation: 
There are three distinct cases:
1. Case 1 where $\Delta>0$ is called Overdamped Motion gives two distinct real roots $\lambda_{\pm}=\frac{-b\pm\sqrt{b^2-4mk}}{2m}$ and gives a solution of the form $$x(t)=c_1e^{\lambda_+t}+c_2e^{\lambda_-t}$$
2. Case 2 where $\Delta=0$ is Critically Damp Motion and gives one repeated real root $\lambda = -\frac{b}{2m}$ and gives a solution of the form $$x(t)=c_1e^{\lambda t}+c_2te^{\lambda t}$$
3. Case 3 where $\Delta<0$ is called Underdamped Motion and gives two complex roots $\lambda_{\pm}=\alpha\pm i\beta$ where $\alpha=-\frac{b}{2m}$ and $\beta = \frac{\sqrt{4mk-b^2}}{2m}$ and gives the solution$$x(t)=e^{\alpha t}(c_1cos(\beta t))$$
That's incomplete because go figure Haik moved on a bit too quickly and jumped around like crazy.

For the purposes of Case 3, it's important to note that $e^{i\theta}=cos(\theta)+sin(\theta)$ and $e^{-i\theta} = cos(\theta)-sin(\theta)$ which gives a [[Linear]] [[MATH024/Topic6/System|System]] which may be potentially solved via [[Gauss Elimination]].