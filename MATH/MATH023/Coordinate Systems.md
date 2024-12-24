
**Cartesian coordinate system:** 
Primarily used up until this point, describes the location of something relative to the origin via x and y components: vertical and horizontal components of the element's location.
IR<sup>2</sup> is notation for "a pair of real numbers" (x,y)
Straight-line distance between any two points(including any given point and the origin) which do NOT have at least one of their two components being identical must be found via the Pythagorean theorem.
(x,y)

**Polar Coordinate System**:
Represents a point using its straight-line distance from the origin and the angle at which it extends from the origin(typically measured in radians), with straight right along what would be the positive x-axis in the Cartesian system being 0 and proceeding in a counter-clockwise-positive fashion.
The distance from any given point to the origin is given within the coordinate system.
(r,$\theta$)

**Converting Between Them:**
If given a Polar coordinate and told to convert into Cartesian:
$$<x=rcos(\theta),y=rsin(\theta)>$$

If given a Cartesian coordinate and told to convert into Polar:
r = $\sqrt{x^2+y^2}$
$\theta$ = tan<sup>-1</sup> (y/x)
When using this formula, take a look for edge cases: For example, any Cartesian coordinate with x=0 will not return a valid $\theta$ value, but if x=0 then the point must be along the y axis, so $\theta$ must = $\pi$/2

**3D Cartesian:** The exact same as the normal system, but using x,y,z to account for all three dimensions.
Distance between two given points: Pythagorean Theorem using three terms(But still a square root, not a cube root)
$\sqrt{x^2 + y^2 + z^2}$ 

**Cylindrical Coordinates:**
$$<x=rcos(\theta), y=rsin(\theta), z=z>$$

**Spherical Coordinates:**
$$<x=\rho sin(\phi)cos(\theta), y=\rho sin(\phi)sin(\theta),z=\rho cos(\phi)>$$
