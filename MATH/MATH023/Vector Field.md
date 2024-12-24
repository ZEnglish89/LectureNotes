
Force Fields are a synonym for Vector Fields.

Vector Fields can be classified as Radial or Rotational, though not all fields will be one of the two(neither is an option).
Radial Vector Fields contain [[Vector]]s which are all perpendicular to a circle centered at the origin. In simpler terms, all the vectors point either directly towards or directly away from the origin.
Rotational Vector Fields contain vectors which are all tangent to that circle, so all the vectors point either clockwise or counter-clockwise.

If a vector field $F(x,y) = <P(x,y),Q(x,y)>$, then F is considered to be a conservative vector field if $\partial P/dy = \partial Q/dx$
The Curl test(below) is more authoritative for determining conservatism, especially when the field has more than two dimensions.

A "potential function" is a function which could produce the vector field. If a vector field $F(x,y)=\nabla G(x,y)$ then $G(x,y)$ is a potential function of F. Remember that when integrating a multivariable function indefinitely, the +C can be a function of the variable not being integrated, so an integral dx will have a +C(y), and vice versa. If the integrals of a Vector Field do not match, consider if adding these C-functions could make it match.
Potential functions are non-unique for the same reason that indefinite integrals are non-unique; there could be any constant involved that is eliminated in the formation of the vector field.

Easy to mix this up: When determining CONSERVATISM, take the DERIVATIVE. When finding POTENTIAL FUNCTIONS, take the INTEGRAL.

The "curl" of a vector field $\overrightarrow{F}=<P(x,y,z),Q(x,y,z),R(x,y,z)>$ is denoted as "curl $\overrightarrow{F}$" or "$\nabla \times \overrightarrow{F}$" is equal to $<\partial_x, \partial_y, \partial_x> \times <P,Q,R>$, the cross product.
This is not completely accurate, or at least it's just a bit difficult to understand. The formula given by Knewton Alta is instead as follows: $$\nabla \times \overrightarrow{F}<P(x,y,z),Q(x,y,z),R(x,y,z)> = (R_y - Q_z)\hat{i} + (P_z - R_x)\hat{j} + (Q_x-P_y)\hat{k}$$
This is because the $\partial$s in the above cross product do not represent a specific partial derivative, but actually represent "take the derivative of." So $\partial_x \times Q$ would mean $\partial Q/\partial x$.

The curl of a vector field is also a vector field.

If $A_r$ is a disk of radius r centered at $\overrightarrow{r}_0$ with a normal unit vector $\hat{n}$, then $$curl\overrightarrow{F}(\overrightarrow{r}_0)\cdot \hat{n} = lim_{r → 0}[ 1/\pi r^2 \oint_C \overrightarrow{F}\cdot d\overrightarrow{r}]$$ The curl measures the "average circulation" of $\overrightarrow{F}$ over $A_r$ as $r → 0$.

The "divergence" of a vector field, denoted as "$div\overrightarrow{F}$" or "$\nabla \cdot \overrightarrow{F}$" is equal to $<\partial_x, \partial_y, \partial_x> \cdot <P,Q,R>$, the dot product.
The divergence of a vector field is a scalar function.

If $V_r$ is a sphere of radius v centered at $\overrightarrow{v}_0$ with outward unit normal vector $\hat{n}$ and S is the surface enclosing it, then $$div\overrightarrow{F}(\overrightarrow{r}_0) = lim_{r → 0} [1/(4\pi^3/3)\int\int_S\overrightarrow{F}\cdot\hat{n} dS]$$

The divergence measures the average "outward-goingness" of $\overrightarrow{F}$ over $V_r$ as $r → 0$ 

The Divergence of a Curl of a vector field is always equal to 0(because it's the dot product of a cross product).

The Curl of a Conservative Vector Field will always be 0.

"Irrotational" means that the Curl=0, which also means that there exists a scalar f such that $F = \nabla f$
Or in other words, that F is conservative. HOWEVER: Even if a Vector Field has a Curl of 0, you must inspect the domain to verify its conservatism.

"Incompressible" means that the Divergence = 0, which also means that there exists a Vector Field G such that $F = \nabla \times G$, meaning that F is/can be the Curl of some Vector Potential.