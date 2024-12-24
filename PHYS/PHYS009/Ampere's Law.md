

Recall how [[Electric Potential]] difference $\Delta\phi$ is calculated between two points:
The Work required to bring the two points to their present location from points of infinite separation.
This ends up being a line integral:$$-\int\vec{E}\cdot d\vec{r}$$

Ampere's Law is based on a similar concept: Define the [[Magnetic Field]] **circulation** around a particular point in a closed loop:$$\oint\vec{B}\cdot d\vec{S}=\mu_0 i_{enc}$$
Note that as long as you have a closed loop which is completely immersed within a uniform [[Magnetic Field]], its magnetic circulation is zero. This is because there has been no net work, the loop just returns to its starting point. The only way you get some net magnetic circulation is when the Field is not constant at some point along the loop.

Using this integral form:
1. Determine the [[Magnetic Field]] Pattern: Unidirectional and circular patterns are easiest to analyze.
2. Choose an [[Amperian Loop]](Think [[Gaussian Surface]]s): This should be shaped such that $\vec{B}\cdot d\vec{S}$ is a simple calculation along the entire loop. More in their own note.
3. Calculate the above integral.
4. Determine $i_{enc}$: This is generally easy, but may require the formal definition of [[Current]] written below.
5. Apply the integral form of Ampere's Law

This is equal to the (signed) current $i$ flowing through any surface enclosed by the loop, multiplied by the permissivity of free space $\mu_0$.

Because this is dependent on $i_{enc}$, the enclosed current, the empty space within any object will contain no [[Magnetic Field]].

This relationship between Ampere's Law and other methods of finding Fields are similar to the relationship between [[Gauss's Law]] and [[Coulomb's Law]]. It gives a cleaner, calculus-based way to skip shitloads of algebra.

Involves the formal definition of [[Current]] flowing through a given surface:$$i_{enc}=\int\vec{J}\cdot d\vec{A}$$

This is limited by: Step vectors must be small enough that each is approximately straight and contains a constant [[Magnetic Field]]. Each tile must be small enough and the [[Current Density]] near enough to constant.

As per [[Faraday's Law]], this can be written as:$$\vec{\nabla}\times\vec{E}=\mu_0J$$
Again, he moved on, but I think that I wrote that in time.

Just like [[Gauss's Law]] can be used for Divergence, Ampere's Law can be used for Curl. The above equation is of Curl, baybeee.

A Curl meter can be devised(Lecture on 11/15-2024) to measure the Curl supplied by a local flow of [[Current]], as the [[Magnetic Field]] generated will provide some amount of torque on the center of the meter. A distant current or field will generate torque as well, but it will be net zero, so the local values are the only ones which need to be considered.

The curl will be zero in a particular dimension if the magnetic field points entirely in that direction. I think that's what he said.
$$\vec{\nabla}\times\vec{B} - \mu_0\epsilon_0\frac{\partial\vec{E}}{\partial t} = \mu_0\vec{j}$$
This is a big mess, he spent several minutes deriving it and I frankly did not really understand the derivation for the most part.
This is one of [[Maxwell's Equations]].