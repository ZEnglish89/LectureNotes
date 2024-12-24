
The work with [[Extrema]] from recently is foundational to optimization with respect to a constraint.

The constraint can be considered a level curve, and optimization is the process of looking for Extrema such that the point which they occur at lies on that level curve.

Extrema must be where the level curves of f() is tangent to the level curve of g(), where g() is the constraint.

$\nabla f$ is perpendicular to the level curves of f(); the same is true for $\nabla g$ and g().
Therefore, if the level curves of f() are tangent to the level curves of g(), then $\nabla f$ and $\nabla g$ are colinear, that is to say that $\nabla f = \lambda \nabla g$, where $\lambda$ is the "Lagrange Multiplier."

You can then solve the system of equations including the lagrange multiplier. You will get two equations which will imply either an x solution or a lambda solution each; if you pick one lambda solution the other x/y solution is correct, and the remaining x/y is dependent on the constraint, and vice versa if you pick the other lambda solution. That gives you your two solution points. You can then proceed to find the extrema within those points as normal.