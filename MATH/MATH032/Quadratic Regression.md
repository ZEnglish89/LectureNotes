
[[Linear Regression]], but for datasets that don't like to be linear.

The equation produced will be in the form of $y = ax^2 + bx + c$

The Quadratic Regression equations are OFFENSIVELY complex.
The ones I found online are below, these are specifically the Least Squares ones.
You need to calculate the following: $$\bar{x}, \bar{y}, \bar{x^2}$$
$$S_{xx} = \Sigma_1^n(x_i^2) - n \cdot \bar{x}^2$$
$$S_{xy} = \Sigma_1^n(x_iy_i) - n \cdot \bar{x} \cdot \bar{y}$$
$$S_{xx^2} = \Sigma_1^n(x_i^3) - n \cdot \bar{x} \cdot \bar{x^2}$$
$$S_{x^2x^2} = \Sigma_1^n(x_i^4) - n \cdot \bar{x^2} \cdot \bar{x^2}$$
$$S_{x^2y} = \Sigma_1^n(x_i^2y_i) - n \cdot \bar{x^2} \cdot \bar{y}$$
Note the difference between $\bar{x}^2$ and $\bar{x^2}$. Now, finally, the three coefficients can be calculated:
$$a = (S_{x^2y}S_{xx} - S_{xy}S_{xx^2})/(S_{xx}S_{x^2x^2} - (S_{xx^2})^2)$$
$$b = (S_{xy}S_{x^2x^2} - S_{x^2y}S_{xx^2})/(S_{xx}S_{x^2x^2} - (S_{xx^2})^2)$$
$$c = \bar{y} - b\bar{x} - a\bar{x^2}$$

Yep this is a real nightmare lmao. The good news is that now I have this to break it down as easily as possible, and it's just mixing around the placement of eight values that are not individually that difficult to compute(at least for reasonably small datasets).