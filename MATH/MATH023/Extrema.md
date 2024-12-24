
A function will have a local maximum at (a,b) if $f(x,y)<=f(a,b)$ for all (x,y) in the same disk centered at (a,b).
It will ahve a local minimum if the same statement, but with the inequality flipped, is true.

$f(a,b)$ is called a local maximum value or local minimum value if a local maximum or minimum occurs at (a,b).

The encompassing term for local maximums and minimums is "extremum."

If t is differentiable at (a,b) and has a local extremum at (a,b), then its first-order [[Partial Derivative]]s are zero at (a,b):$$\nabla f(a,b)=0$$
This corresponds with single-variable functions, whose first derivatives are equal to 0 at their local extrema.

A point where $\nabla f(a,b)=0$ or where one of the partial derivatives does not exist is called a critical point.

Finding all critical points: Find the points at which each of the partial derivatives = 0, for two-variable equations this will typically be four points.
$D=f_{xx} \cdot f_{yy} - f_{xy}^2$
Test D at each of the critical points, 
if $D>0$ and $f_{xx}>0$, the point is a local minimum.
if $D>0$ and $f_{xx}<0$, the point is a local maximum.
if $D<0$, the point is a saddle point.
if $D=0$, the test is inconclusive.

Absolute Extremum:
A function has an absolute maximum or minimum at (a,b) if $f(a,b)> or <f(x,y)$ for ALL (x,y).
This can also be referred to as "global" rather than absolute.

Extreme Value Theorem: if a function is continuous on a closed and bounded set D, then f has an absolute maximum and an absolute minimum for some points on D.
A closed set contains all its boundary points. A bounded set is contained in some bounded disk.

In interval notation, a closed set would be [], an open set would be ().
A wedge(like a pizza slice) extending off with infinite length is closed, because it contains the edges of the wedge, but not bounded, because it cannot be completely encircled.

To find the absolute max/min of a continuous f on a closed and bounded set D, there are three steps:

1) Find all critical points(local extrema) of f in D.
2) Find extremal points of f on the boundary of D.
3) Compare all function values on those points to find the absolute max/min

In short, find all local maxes/mins and just find the largest/smallest one.
The hard part is step 2. This is accomplished by:
Parameterizing the boundary equation into x(t) and y(t).
Declare $g(t)=f(x(t),y(t))$
Find critical points of g(t), that is to say find the points where $g'(t)=0$.
The value of the critical points is equal to the value of g(t), and the x and y values can be found by plugging the t value into the parameterized x(t) and y(t).