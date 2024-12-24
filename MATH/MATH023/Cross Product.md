The cross product of two [[Vector]]s is the same as the "determinants" of two matrices

i->j->k->i
If the multiplication follows the order of the arrows, the result will be positive, if it goes against the order the result will be negative.

The positive direction of the resultant vector will be consistent with the counter-clockwise-positive rule for rotation.

Note: This does not guarantee that the result will or won't have a negative sign, it just refers to whether you do or don't multiply the existing result by -1

![[Pasted image 20240124114858.png]]

A cross product will return a third vector which is perpendicular/orthogonal to both of the original vectors.
(This means that the [[Dot Product]] of a Vector with a cross product involving that Vector will always return 0)

The magnitude of the cross product will be equal to the magnitudes of the two component vectors multiplied by the sin of the angle between them. This means that colinear(parallel/antiparallel) vectors will return a cross product of 0. This is opposed to the [[Dot Product]] which returns 0 for perpendicular vectors.

The magnitude of a cross product is equal to the area of a parallelogram with the two constituent vectors as the side lengths.

Cross Products are distributive, so to speak:
u x (v+w) = u x v + u x w

The [[Dot Product]] of one vector with the Cross product of two other vectors (i.e. $u \cdot (v \times w)$ ) is referred to as the "Triple Scalar Product." If this product returns a value of 0, the three vectors are Coplanar.
The volume of a parallelpiped formed by u v and w is equal to the absolute value of this Triple Scalar Product.


For the derivative of the Cross Product of [[Vector Function]]s:$$d/dt [r(t) \times u(t)] = r'(t) \times u(t) + r(t) \times u'(t)$$

