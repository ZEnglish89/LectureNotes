
This is a higher-dimension version of a Linear Approximation.

For a [[Plane]], at any given point: $z=f(x,y)$
Let $(x,y,z)$ be a point on the plane.

$\overrightarrow{RP}=<\Delta{x},0,f_x(x_0,y_0)\Delta{x}>$
$\overrightarrow{RQ}=<0,\Delta{y},f_y(x_0,y_0)\Delta{y}>$

$\overrightarrow{n}=\overrightarrow{RP}\times\overrightarrow{RQ} = \Delta{y}\Delta{x}<-f_x(x_0,y_0),-f_y(x_0,y_0),1>$
Vector in the plane $\overrightarrow{r} - \overrightarrow{r} _0 =<x-x_0,y-y_0,z-z_0>$
The tangent plane equation at $(x_0,y_0)$:
$<-f_x(x_0,y_0),-f_y(x_0,y_0),1>\cdot< \overrightarrow{r} - \overrightarrow{r} _0>=0$
$Z = f(x_0,y_0) + f_x(x_0,y_0)(x-x_0)+f_y(x_0,y_0)(y-y_0)$
Z is the equation of the tangent plane!!!!
Deriving that equation fucking sucks, but all you actually need to get the answer you're looking for is to know that equation Z.

For example: For $f(x,y)=\sqrt{41-x^2-4y^2}$ at the point (3,2):
$f(3,2)=4$
$f_x(3,2)=-3/4$
$f_y(3,2)=-2$
So the equation of the tangent plane is:$$Z=4+((-3/4)(x-3)) + ((-2)(y-2))$$
Which simplifies to $$-2y-3x/4+41/4$$
To perform a tangent plane approximation, simply then plug in the x and y of the point you intend to approximate to that new equation.