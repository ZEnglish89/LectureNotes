
A multivariable function is considered to be differentiable if its tangent plane approximation at $(a,b)$ is a "good approximation" as $(\Delta x,\Delta y) → (0,0)$.

This is different from single variable functions, where to be "differentiable" simply means that the derivative exists. [[Partial Derivative]]s can exist, but the function they come from can still not be considered differentiable.

This means that in reference to multivariable functions, differentiability is a "stronger condition" than in other contexts.

Multivariable Chain Rule:

The variables of a multivariable function may depend on functions of other variables
if s<sub>1</sub>=t and $f(x(t),y(t),z(t))$ 
then $$d/dt[f(x(t),y(t),z(t))] = ((\partial f/\partial x)\cdot (dx/dt))+((\partial f/\partial z)\cdot (dy/dt))+((\partial f/\partial z)\cdot (dz/dt))$$
Once you have found all the derivatives, simplify and then substitute t in for x,y,z.

If $f(x,y,z)$ is dependent on multiple other variables, like $(s_1,s_2,...,s_i)$, or if $f$ is dependent on another multivariable function, then the formula becomes:$$\partial f/\partial s_i = ((\partial f/\partial x_1)\cdot (\partial x_1/\partial s_i))+$$ and add the terms for all  $x_n$ terms.

For chain rule: Be very clear on the dependence of variables; draw the tree diagrams done in class.
Apply the appropriate one of the two formulas.

Chain rule may also be used for implicit differentiation.