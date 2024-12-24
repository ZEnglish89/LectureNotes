
Well that's a real long title: Second-[[Order]] [[Linear]] [[Ordinary Differential Equation]]s with constant coefficients, just so I can put all the links in there.

Applications:
Newton's Second Law: $$m\cdot dv/dt=\Sigma_i F_i$$ Where $F_i$ is some external force. This is just an alternate way or writing $F=ma$.
Can also be written as $\dot{m}$ but with two dots(just imagine it) meaning two time derivatives, or indeed meaning acceleration.
See the Restoring Force of a pendulum: $$F_R=-mgsin(\theta)$$
This can be written as a Differential Equation:$$ml\alpha = -mgsin(\theta)$$
Or$$\alpha = - (g/l) \cdot sin(\theta)$$
This is NOT solvable, at least nobody's solved it yet, so we can approximate $sin(\theta)=\theta$ to give us $$\alpha = -(g/l)\theta$$
which can be easily solved with $$\theta = cos(\sqrt{(g/l)}t)$$ Or something like that, I'm not entire sure to be completely honest. I'm not as great at this as I'm clearly supposed to be.

This type of equation is anything which satisfies the the following equation, which is also an example of [[Simple Harmonic Motion]].$$L(.) = m\cdot (d^2/dt^2)+b(d/dt)+k)\cdot(.)=f(t)$$
I'm just gonna move on from that bad boy because I don't know what's up with the dots.

THESE FUCKERS CAN BE TURNED INTO QUADRATICS!!!
With $$mx''+bx'+kx=0$$
Assume a solution of the form $x(t)=e^{\lambda t},\lambda\in C$:$$(m\lambda^2+b\lambda+k)e^{\lambda t}=0$$
This becomes the "Characteristic Equation" $$m\lambda^2 + b\lambda +k = 0$$
Which can literally be solved by the quadratic equation in the form:$$\lambda = \frac{-b \pm\sqrt{b^2-4mk}}{2m}$$
The results are called the "roots of the characteristic equation" or the "eigenvalues."

Label $\Delta = b^2-4mk$ from the equation above, this part is the "discriminant." Then:$$x(t)=c_1e^{\lambda_1t}+c_2e^{\lambda_2t}=e^{-\frac{b}{2m}t}(c_1e^{\frac{\sqrt{\Delta}}{2m}t}+c_2e^{-\frac{\sqrt{\Delta}}{2m}t})$$
Which isn't really that meaningful to me yet but I'm hoping it means I can just kinda punch numbers into that form and everything will be okay?

If $\Delta>0$ then there are two real distinct roots and the homogeneous solution is of the form$$x_h=c_1e^{\lambda_1 t}+c_2e^{\lambda_2t}$$
If $\Delta=0$ there is one real repeated root and the homogeneous solution is of the form$$x_h=c_1e^{\lambda t}+c_2te^{\lambda t}$$
If $\Delta<0$ there are two complex roots and the homogeneous solution is of the form$$x_h=e^{\alpha t}(c_1cos(\beta t)+c_2sin(\beta t))$$
where $\alpha=-\frac{b}{2m}$ and $\beta=\frac{\sqrt{4mk-b^2}}{2m}$, or $\lambda = \alpha \pm \beta i$. Just remember, when you do the quadratic equation you will wind up with some number $\pm$ another number. In the case where $\Delta<0$ that $\pm$ will contain an $i$ and the coefficient on that $i$ is $\beta$.
