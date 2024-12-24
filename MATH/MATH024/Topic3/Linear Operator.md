
A numerical function $L(\overrightarrow{x})$ of a Vector argument is called a [[Linear]] Operator if it satisfies:
1: $L(k\overrightarrow{x}) = kL(\overrightarrow{x})$ for all real numbers $k$.
2: $L(\overrightarrow{x}+\overrightarrow{y}) = L(\overrightarrow{x}) + L(\overrightarrow{y})$

The Derivative and Integral operators are Linear Operators: Constants can be pulled out, and sums of multiple functions can be split.

$$y' + sin(t)y = cos(t) -> L(y) = (d/dt +sin(t))(y) = cos(t)$$
$$t^2y' + ty' +y =0 -> L = t^2d^2/dt^2 + td/dt + 1$$
If $\overrightarrow{x} = [x_1,x_2,...,x_n]$ and $\overrightarrow{a} = [a_1,a_2,...,a_n]$ then define $<\vec{a},\vec{x}> = a_1x_1 + a_2x_2 + ... + a_nx_n$
This is a [[Linear]] operation called the Linear Product.
$$<\vec{a},\vec{x}+\vec{y}> = <\vec{a},\vec{x}> + <\vec{a},\vec{y}>$$
This can be proven by simply expanding the vectors out.