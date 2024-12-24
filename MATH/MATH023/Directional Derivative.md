
A derivative with respect to a variable measures the rate at which the function changes as that variable changes.

The Directional Derivative of f at $\overrightarrow{r}_0 = <x_0,y_0>$ in the direction of an unit vector $\hat{u} = <a,b>$ is:
$$D_\hat{u}f(\overrightarrow{r}_0) = lim_{h → 0}f(\overrightarrow{r}_0+h\hat{u}-f(\overrightarrow{r}_0)/h$$
or $$lim_{h → 0}f(x_0+ha,y_0+hb)-f(x_0,y_0)/h$$if it exists.

If f is differentiable at $(x_0,y_0),$ then f has a directional derivative in the direction of any unit vector $\hat{u}$ and $D_\hat{u}f(\overrightarrow{r}_0) = <f_x(x_0,y_0),fy(x_0,y_0)> \cdot <a,b>$
The f portion of the right side of that equation is referred to as the "gradient vector" of f and $(x_0,y_0)$. $\nabla f(x,y)$   

If f is differentiable, f can be approximated by its tangent plane, meaning $$f(\overrightarrow{r}+h\hat{u}) = f(\overrightarrow{r_0})+f_x(\overrightarrow{r_0})a + f_y(\overrightarrow{r_0})b + \epsilon_1h +\epsilon_2h$$ where $\epsilon_1, \epsilon_2, and h → 0$.

Because of the properties of the [[Dot Product]], the maximum rate of increase/decrease of f is equal to the magnitude of the Gradient Vector. This is maximized when $\hat{u}$ is parallel to f, and minimized when they are perpendicular.


On level curves, $\nabla f$ is orthogonal to the tangent vector.
In 3D, $\nabla f$ is orthogonal to the tangent plane.