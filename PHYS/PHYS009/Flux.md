
A rate of flow through a surface, an oriented area element or "tile."
A tile's Normal vector $\hat{n}$ denotes the tile's orientation.
$\overrightarrow{A} = A\hat{n}$ where A is the scalar area of the tile.

Assume there is a space filled with particles traveling at a velocity $\overrightarrow{v}$, we can calculate the particle travel rate through the space(the tile).

Distance traveled is just equal to $|\overrightarrow{v}|\Delta t$.
Number of particles is $\Delta N$.
$n$ is number density: particles per unit volume.
$\Delta N/\Delta t = n|\overrightarrow{v}||\overrightarrow{A}|$


If the tile is slightly slanted with a height difference of $L\cdot cos(\theta)$
$\frac{\Delta N}{\Delta t} = n|\overrightarrow{v}||\overrightarrow{A}|cos\theta = \overrightarrow{J}_N \cdot \overrightarrow{A}$ if $\overrightarrow{J}_N = n\overrightarrow{v}$

$\overrightarrow{U} \cdot \overrightarrow{A}$ represents the flux of a vector $\overrightarrow{U}$ over an area $\overrightarrow{A}$?? He moved on too fast a-fucking-gain.

$\vec{A}$ is area represented as a vector:
A vector normal to the surface with magnitude equal to the surface's area.

This model assumes uniform flow, which is not realistic for the actual world.
Look at local velocities $\overrightarrow{J}_N$. In the river example this are local [[Current Density]]. Define many of these.
Model number density in local volume, then multiply by flow velocity.
Divide the tile S into many smaller tiles, $d\overrightarrow{A}_i$ and the Flux is $\overrightarrow{j}_{N,i} \cdot d\overrightarrow{A}_i$
Total Flux over surface S = $\int \overrightarrow{J}_N \cdot d\overrightarrow{A}$

For Flux through a 2-D surface, general equation is $$\overrightarrow{J}_N \cdot \overrightarrow{A}$$ or $$\Phi_E = \overrightarrow{E} \cdot \overrightarrow{A}$$
These are just dot products, relatively manageable if all the constituent variables are known.
*Do these dot products in terms of $|\vec{E}||\vec{A}|cos\theta$, NOT in terms of the different components.*

If the [[Electric Field]] is tangent to the surface at all points, then the Flux of the [[Electric Field]] will just be 0.
If the Field is normal to the surface at all points, then the Flux of the Field will be $EA$(magnitude of the field $\cdot$ magnitude of the area).
If a [[Charge]] is placed at the corner of an object, then the sides of that object which contact the corner are not considered to be enclosing the Charge, and therefore their Field/Flux is 0.

The Displacement [[Current]] is proportional to the time-derivative of Electric Flux via:$$i_d =\epsilon_0\frac{d\Phi_e}{dt}$$