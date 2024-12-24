
Can be called the Fundamental Theorem of [[Linear Algebra]]

Let $\vec{u}_p$ be any particular [[Solution]] to a [[Linear]] nonhomogeneous equation.

$L(\vec{u})=c$ if it's linear algebraic.
$L(\vec{u}) = f(t)$ if it's linear differential.

Let $\vec{u}_h$ be a [[Solution]] to the associated Linear homogeneous equation $L(\vec{u}_h)=0$
Then $\vec{u} = \vec{u}_h+\vec{u}_p$ is also a solution to the nonhomogeneous equation $L(\vec{u})=C$ or $L(\vec{u}) = f(t)$
Furthermore, **every** [[Solution]] to the nonhomogeneous equation must be of the form $$\vec{u}=\vec{u}_h+\vec{u}_p$$
When plugged in, the $\vec{u}_h$ gives zero and the $\vec{u}$ gives $f(t)$ or $c$

$$L(\vec{u}_h+\vec{u}_p) = L(\vec{u}_h)+L(\vec{u}_p) = 0 + {C or f(t)}$$

$dy/dt = cos(t)$ -> $y=y_h+y_p$ -> $y_p = sin(t)$ -> $y_h=c$ -> $y=sin(t) + c$

This also holds for [[System]]s and [[Matrix]]es: The Matrix A is a [[Linear Operator]], therefore any non-homogeneous system $Ax=b$ has solutions of the form $Ax=b$ with $x=x_h+x_p$ where $A(x_h)=0$ and $A(x_p) = b$
This is another section where I'm gonna recommend looking back at Lecture Notes 3.2