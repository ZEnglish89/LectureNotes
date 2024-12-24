
$$f_{x} = \partial f/\partial x$$ Or "The partial derivative with respect to x"

To take a partial derivative: Treat all variables other than the one the derivative is taken with respect to as if they were constants, and take the derivative normally. For example:
if $f(x,y)=x^2e^{2y}+ysin(xy)$ then $f_x=2xe^{2y}+y^2cos(xy)$ and $f_y=2x^2e^{2y}+xycos(xy)+sin(xy)$


Partial derivatives can be taken to higher orders. $(f_{x})_{x}$ is the second-order partial derivative with respect to x.
These can be mixed, for example you can have $(f_{x})_{y}$ which is the partial derivative with respect to y ***of*** the partial derivative with respect to x.
$$(f_{x})_{y}=f_{xy}=\partial^2f/(\partial y \partial x)$$
So be careful about notation. The above looks like a mess, but you need to check the order in which the derivatives are taken. Start with the derivative closest to the function, work your way outwards.

If $f_{xy}$ and $f_{yx}$ are both continuous, then they will be equal to one another. This extends out to all higher-order partials, their order is interchangable if they are ALL continuous.