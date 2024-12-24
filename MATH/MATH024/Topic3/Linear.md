Linear models are unrealistic for actual scenarios, but they operate as good approximations for existing curves.

A line is a linear approximation of a curve, a plane is a linear approximation of a surface, etc.

With proper use of "linearizations," previously unsolvable [[Differential Equation]]s can be given Qualitative or rough solutions. Not the same as truly solving them, but extremely useful regardless.

An Equation is Linear if it is in the form $a_1x_1 + a_2x_2 + ... + a_n x_n = c$ where the a-values are constants.
If $c=0$, the linear equation is called "homogeneous."

An [[Ordinary Differential Equation]] is linear if it is in the form $$a_n(t) (d^ny)/(dt^n) + a_{n-1}(t)(d^{n-1}y)/(dt^{n-1})+...+a_1(t)(dy)/(dt) = f(t)$$
where $a_i(t)$ and $f(t)$ are defined over some common integral.
If $f(t)=0$ over that integral, then the ODE is called "homogenous."
Derivative of y, function $\cdot$ lower derivative of y, function $\cdot$ lower again derivative of y, etc etc until you differentiate y down to a constant or zero. Constants are considered functions of t for these purposes.

**All** first-[[Order]] ODEs can be written as $y'+p(t)y = f(t)$, which allows them to be solved via the [[Integrating Factor]] method.

$(y')^2 + p(t)y=f(t)$ is non-linear because y and y' do not appear with only exponent 1.

$y'' + p(t)y' + g(t)y = f(t)$ is linear because it matches the form above.