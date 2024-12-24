
Can be [[Scalar]] or [[Vector]]; each is computed slightly differently.

Scalar:
For a function $f(x,y)$ over a curve parameterized as $\overrightarrow{r}(t)=<x(t),y(t)>$ from $a<=t<=b$,
the Scalar Line Integral is equal to $\int_a^b f(x(t),y(t)) \times ||r'(t)||dt$
The cross in the above equation denotes standard multiplication, not a cross product, as the two factors are both scalars.

Vector:
For a [[Vector Field]] $F(x,y)$=<P(x,y),Q(x,y)> over a curve parameterized as $\overrightarrow{r}(t)=<x(t),y(t)>$ from $a<=t<=b$, the Vector Line Integral is equal to $$\int_a^b <P(x(t),y(t)),Q(x(t),y(t))> \cdot <x'(t),y'(t)> dt$$ The dot in the above equation IS a dot product; it is not simply multiplication.
If the vector field is described as occurring across a region which is made up of multiple curves, the total integral is simply the sum of the integrals across each individual curve.

**Fundamental Theorem of Line Integrals:** If $C$ is a smooth curve given by $\overrightarrow{r}(t), a<=t<=b$, and $f$ is a function where $\nabla f$ is continuous on C, then: $$\int_C \nabla f \cdot d\overrightarrow{r} = f(\overrightarrow{r}(b)) -f(\overrightarrow{r}(a)) $$
Basically, the potential function of a Conservative [[Vector Field]] is also its Vector Line Antiderivative.

A line integral is called "Independent of Paths" if it will 
