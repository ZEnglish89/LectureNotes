For the Geometry of [[System]]s.

**Homogeneous case**: Row Picture: We can interpret Ax=0 as a collection of rows:
$$a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n = 0$$
$$a_{m1}x_1 + a_{m2}x_2 + ... + a_{mn}x_n = 0$$
Each of those rows is a plane.

The column vector $\vec{x} = x_1, x_2, ..., x_n$ is the collection of all vectors that are orthogonal to all m planes.

Column Picture: $$(a_{11}, a_{21}, ... , a_{m1})\cdot x_1 + (a_{12},a_{22},...,a_{m2})\cdot x_2 + ... + (a_{1n},a_{2n},...,a_{mn})\cdot x_n = (0,0,...,0)$$
$\vec{x} = (x_1,x_2,...,x_n)$ is the collection of all numbers such that the above collection of vectors cancel out to be equal to 0.

**Singular Case:** Row Picture:
If there are two parallel planes, there will be no solutions: [[Solution]]s occur when all available planes intersect, and if two are parallel then they cannot all three intersect.

Similarly, if all planes are parallel, there are no solutions.

If there are no intersections, there are obviously no solutions. The parallel planes cases above are just ways to guarantee that this case occurs.

With a line of intersections, where all three lines intersect along a line, there are infinite solutions: Every point along that line.

Column Picture:
Singularity occurs when the columns are incapable of equaling b regardless of how they are scaled. No solution. Most commonly occurs when the columns are all in a plane which b is normal to.

If b exists on the same plane as the columns then there are infinite solutions, infinite ways for the columns to equal it.