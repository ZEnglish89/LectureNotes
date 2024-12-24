 Translation and Rotation can occur in different planes from each other
A stationary reference frame is denoted with XYZ, a moving one is denoted with xyz

xyz will be tethered to a specific point, the absolute location, velocity, and acceleration of points tethered to that reference frame can be found using both the values of that point relative to that reference frame and the values of the point the reference frame is tethered to relative to the stationary reference frame.

For rotation: Positive and negative are decided by the right hand rule, where your thumb follows the positive direction of the axis the rotation is along; meaning that you put your hand on the origin of the reference frame and point your thumb along the axis. Counter-clockwise, following the direction of your fingers, is positive. Clockwise, opposing the direction of your fingers, is negative.

If B is defined in the moving reference frame which is tethered to A:
Position: $$R_B = R_A + R_{B/A}$$
Velocity: $$V_B = V_A + (Ω_{xyz} \times R_{B/A}) + (V_{B/A})_{xyz}$$ 
Acceleration: $$a_B = a_A + (A_{xyz} \times R_{B/A}) + (Ω_{xyz} \times (Ω_{xyz} \times R_{B/A})) + (2Ω_{xyz} \times (V_{B/A})_{xyz}) +(a_{B/A})_{xyz}$$ 
Wow these equations fucking suck

The capital A above is denoting rotational acceleration. This is normally shown with an omega dot, but I can't figure out how to type that. An $_{xyz}$ means that the measurements are taken in the $xyz$ frame as opposed to the $XYZ$ one, so the directions change with the rotation.
$\hat{i}$, $\hat{j}$, and $\hat{k}$ unit vectors are used for $x, y,$ and $z$.
With rotation, the $\hat{i}$, $\hat{j}$, and $\hat{k}$ vectors for the rotating reference frame xyz can change:
$$d\hat{i}/dt = \Omega_{xyz}\times \hat{i}$$
$$d\hat{j}/dt = \Omega_{xyz}\times \hat{j}$$
$$d\hat{k}/dt = \Omega_{xyz}\times \hat{k}$$

if $$\Omega_{xyz}=w_1\hat{i}+w_2\hat{j}+w_3\hat{k}$$then $$A_{xyz}=(dw_1/dt\cdot\hat{i})+(w_1\cdot d\hat{i}/dt)+(dw_2/dt \cdot \hat{j})+(w_2 \cdot d\hat{j}/dt)+(dw_3/dt\cdot \hat{k})+(w_3\cdot d\hat{k}/dt)$$
Take the derivative of all three sides, applying product rule to each one.
This means that the vectors are changing in the same way and at the same pace as the reference frame overall.

If one of the rotational vectors is affected by the other(like the arm of a crane rotating about the x-axis while the body of the crane rotates about the y-axis), then the derivative of that rotational vector is equal to the cross product of the unit vector by the rotational vector affecting it.

For the crane example: Crane's entire body is rotating in the y-axis at w<sub>1</sub> rad/s. At the same time, the crane's arm is rotating in the x-axis at $w_2$ rad/s. The reference frame is tethered to the body of the frame. The y-axis does not move, because it is only the arm, not the body, rotating in the x-axis, the arm only rotates relative to the body. However, the x-axis does move, because the entire body is rotating about the y-axis.
The derivative of i(and therefore the angular acceleration which i contributes) is:$$(dw_2/dt\cdot \hat{i})+(w_2\cdot (w_1\hat{k}\times\hat{i})$$
To solve a problem with these situations:
Draw all necessary diagrams;
Choose where to center the fixed frame $XYZ$ and a point to tether the moving frame $xyz$ to;
Calculate the relative and angular velocities and accelerations(these will typically be known or calculatable within the problem);
Use the above equations to turn the relative and angular velocities and accelerations into their absolute versions which you desire.