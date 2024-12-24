Three points are needed to specify a plane, one for each of the three dimensions the plane has.
This is as opposed to the two points needed for a line.
The same way that you can draw a line between any two points, you can draw a plane for any three points.

Planes can be represented multiple different ways.

Vector equation of a plane: $\overrightarrow{n}$ * ($\overrightarrow{r}$  - $\overrightarrow{r}$<sub>0</sub>) = 0

$\overrightarrow{n}$ is a perpendicular vector to the plane
$\overrightarrow{r}$ is a vector for "any" point on the plane
$\overrightarrow{r}$<sub>0</sub> is a vector representing ONE point on the plane.

Scalar equation of a plane: ax+by+cz = k

To find a plane containing the points Q, R, and S:

Find $\overrightarrow{QR}$ and $\overrightarrow{QS}$, take the cross product of the two to get a third vector, $\overrightarrow{n}$


The a, b, and c in the above equation are the components of $\overrightarrow{n}$.
To complete the equation, replace the x, y, and z with (x-), (y-), and (z-), where you are subtracting the matching component of any of the three points from the variables in the equation. Then k=0.
So the equation would be a(x-Qx) + b(y-Qy) + c(z-Qz) = 0
I'm not clear why you need to do this so that k=0, rather than just substituting in the point's values and solving for a different k, but Knewton Alta will only accept an answer with subtraction making k=0.

To find a plane containing the point P and a line $\overrightarrow{r}$(t): Find $\overrightarrow{r}$(0) and use that to find $\overrightarrow{qr}$. Take the cross product of that and $\overrightarrow{v}$, which is the parts of $\overrightarrow{r}$ that are dependent on t, and finish out the scalar representation like the first example.


Two planes are considered parallel or perpendicular if their normal vectors are parallel or perpendicular.
The angle between two planes is the acute angle between their normal vectors. Specifically the acute angle, measure it in whatever way allows it to be acute.

To find this angle: Find the two vectors and their magnitudes.
$\theta$ = cos<sup>-1</sup>(dot product of the vectors/their magnitudes multiplied together)
To find a vector equation at their point of intersection: take the cross product of the two vectors;


Given a point and a plane which does not contain the point, find the distance from the point to the plane:
Find a line from one of the points on the plane to the outside point. The distance is the scalar projection of that line onto the normal vector.
If the plane is ax + by + cz = d, the normal vector is (a,b,c) and the point off of the plane is (x,y,z)
The distance is |ax + by + cz - d|/$\sqrt{a^2 + b^2 + c^2}$ 
More specifically: For a plane containing point Q with normal vector $\overrightarrow{n}$ to a point P not contained within the plane is:
d = |$\overrightarrow{QP}$ * $\overrightarrow{n}$| / ||$\overrightarrow{n}$||
For these purposes, any point Q will work so long as it is on the plane, so you can just set two components to 0 and solve the equation of the plane for the third.

To find the distance between two parallel planes: Find one point on one of the planes, and then do the above process, treating that point as P and finding its distance from the second plane.

The direction [[Vector]] of the [[Line]] of intersection of two planes is the cross product of their normal vectors.
To find a point along that line, assume x=0, and solve the system of equations given by the two planes for y and z. You can assume x=0 because you just need to find *any* line, not a specific one, and unless the direction vector has 0$\hat{i}$, the line is guaranteed to have a point for which x=0.