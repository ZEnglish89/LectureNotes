Used within [[Ampere's Law]]

Build the loop out of contiguous segments. Three types:
1. Type Z: Segment lies in a region or on a line where $\vec{B}=0$
2. Type P: Segment's step vectors $d\vec{S}$ are all $\perp \vec{B}$
3. Type CC: Where $\vec{B}$ is collinear and constant
Types Z and P yield evaluations of $\vec{B}\cdot d\vec{S}=0$ for all steps.

Type CC yields $$\vec{B}\cdot d\vec{S}=\pm|\vec{B}||d\vec{S}|$$
There's a way to simplify or at least rewrite that last expression further but he moved on too fast.

For unidirectional [[Magnetic Field]]s, use a rectangular loop with two legs aligned with the field and two legs perpendicular to the field:
Two segments of Type CC, and two of Type P. This allows you to only have to calculate for the two CC straight lines.

For circular fields, use a circular loop, made entirely of Type CC segments.
Example: An infinite straight pipe allows you to choose a circle of radius $u$, $i_{enc}=I$ the entire current, so:$$\oint\vec{B}\cdot d\vec{S}=\mu_0 i_{enc}=\mu_0I ->|\vec{B}|=\frac{\mu_0I}{2\pi u}$$