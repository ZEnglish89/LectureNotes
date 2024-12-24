
Example: Solve$$a_2x''+a_1x'+a_0x=f(t)$$ with $a_2\neq 0$.
Homogeneous solution will be of the form:
$$x_h = c_1x_1+c_2x_2$$
You literally vary the parameters: $c_1 -> u_1(t)$ and $c_2 -> u_2(t)$, straight up turn them into functions temporarily. This gives a particular solution of the form$$x_p = u_1(t)x_1(t)+u_2(t)x_2(t)$$
So$$x_p=u_1x_1+u_2x_2$$$$x_p' =(u_1x_1'+u_2x_2')+(u_1'x_1+u_2'x_2)$$$$x_p'' = (u_1x_1''+u_2x_2'')+(u_1'x_1'+u_2'x_2')+\frac{d}{dt}(u_1'x_1+u_2'x_2)$$
Using this, and the original ODE, you get:$$a_2(u_1x_1''+u_2x_2'')+a_2(u_1'x_1'+u_2'x_2')+a_2\frac{d}{dt}(u_1'x_1+u_2'x_2)+a_1(u_1x_1'+u_2x_2')+a_1(u_1'x_1+u_2'x_2)+a_0(u_1x_1+u_2x_2) = f(t)$$
Which is a ROYAL mess.

The first term's coefficient gets put before the second derivative, the second term's coefficient gets the first derivative, and the third term's coefficient gets the base function.

However, some of those terms can be removed as they are present within the homogeneous solution. Namely, the first term with each coefficient.
That gives you$$a_2(u_1'x_1'+u_2'x_2')+a_2\frac{d}{dt}(u_1'x_1+u_2'x_2)+a_1(u_1'x_1+u_2'x_2) = f(t)$$
From this, your Auxiliary Condition is $u_1'x_1+u_2'x_2=0$, as setting that value transforms the above equation all the way down to$$a_2(u_1'x_1'+u_2'x_2')=f(t)$$
And therefore you have a [[MATH024/Topic3/System|System]] of $$u_1'x_1'+u_2'x_2'=\frac{f(t)}{a_2}$$$$u_1'x_1+u_2'x_2=0$$
And with this system, you can turn it into a [[Matrix]] and solve using [[Cramer's Rule]].
The Matrix system is below(albeit missing its pretty parentheses) and you end up getting:$$u_1' = \frac{-x_2f(t)/a_2}{W[x_1,x_2]}$$$$u_2' = \frac{x_1f(t)/a_2}{W[x_1,x_2]}$$
$$\begin{array}{cc} x_1&x_2\\x_1'&x_2'\end{array}\cdot\begin{array}{cc}u_1'\\u_2'\end{array} = \begin{array}{cc}0\\ \frac{f(t)}{a_2}\end{array}$$
He did an example in lecture but he literally was done with the example before I even finished writing down his previous work.
Haik thinks we've all taken this class before and already understand everything, so he doesn't need to explain anything he can just do the problems at his own pace.