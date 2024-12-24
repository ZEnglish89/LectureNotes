
A simple closed curve C is "positively-oriented" if the region D bounded by the curve is always on the "left" when the curve is traversed.

The orientation of a curve is dependent on the direction(clockwise vs counter-clockwise) of traversal.

Let C be a positively-oriented, piecewise smooth, simple closed curve in $IR^2$, and denote D to be a region bounded by C. If $P(x,y),Q(x,y)$ has continuous first-order [[Partial Derivative]]s on an open region containing D, then: $$\int\int_D (Q_x-P_y)dA = \oint Pdx + Qdy$$
where $\overrightarrow{F}=<P,Q>$

This is primarily used to convert complex [[Double Integral]]s into simple [[Line Integral]]s; or vice-versa.
According to Professor Wan, the line-to-double use is more common.

Compute the area of D by $\overrightarrow{F} = 1/2<-y,x>$
The [[Vector Field]] does not need to be conservative to use this, you just need the curve to be closed.

Green's is for [[Line Integral]]s, [[Stokes' Theorem]] is for [[Surface Integral]]s.