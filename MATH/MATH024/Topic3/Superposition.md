
The Superposition Principle for [[Linear]] Homogeneous Equations.

Let $\vec{u}_1$ and $\vec{u}_2$ be [[Solution]]s of the linear homogeneous equation $L(\vec{u})=0$
Then their sum $\vec{u}=\vec{u}_1+\vec{u}_2$ is also a solution; and a constant multiple $\vec{u} = k\vec{u}_1$ is also a solution.

The sum of two solutions is a solution, and multiplying a solution by a constant will also yield a solution.

Given $y''+4y=0$, two solutions are $y_1=sin(2t)$ and $y_2=cos(2t)$
$y_1' = 2cos(2t)$ -> $y_1'' = -4sin(2t)$
$y_2 = -2sin(2t)$ -> $y_2'' = -4cos(2t)$

$y_1'' + 4y_1 = (-4sin(2t)) + 4(sin(2t)) = 0$ this proves that $y_1$ is a solution.
$y_2'' + 4y_2 = (-4cos(2t) + 4(cos(2t)) = 0$ this proves that $y_2$ is a solution.
Now for Superposition:
$y=y_1+y_2$
$y''+4y=(y_1+y_2)''+4(y_1+y_2)$ -> $(y_1'' + 4y_1) + (y_2'' + 4y_2) = 0 + 0 = 0$ so the sum of the solutions is a solution.

$y=ky_1$
$y'' + 4y = (ky_1)'' + 4(ky_1)$ -> $ky'' + 4ky_1 = k(y'' + 4y_1) = k(0) = 0$ so a multiple of a solution is a solution.

