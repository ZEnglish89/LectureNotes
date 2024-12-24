
When Line [[Wave]]s(See [[Sinusoidal Wave Model]]) approach some small opening in a barrier, and then pass through, they will emerge on the other side of the barrier as Circular Waves.

This can easily be seen when watching waves crash through the entryway of a bay or harbor.

If there are two small openings in a barrier, each opening will act as its own source of Circular [[Wave]]s. If the waves from those two sources interact, they obey the [[Superposition Principle]]. They combine into a single wave at their point of contact, before moving past that point unaffected.
Of course, when two circular waves meet, there are a variety of different points of contact, making a whole mess.

That interference may either be Constructive, where the waves combine to increase the net amplitude, or Destructive, where they reduce the net amplitude.

One set of two-slit [[Diffraction]] will produce multiple points of each type of interference via the circular waves.

The path to a peak constructive point(the waves are fully combined) will occur at length $\Delta s =n\lambda$ in this scenario, and the peak destructive point(the waves are fully cancelled) will occur at $\Delta s = (n+\frac{1}{2})\lambda$
I believe that both of these occur at all multiples of $n$, so the $n$th point occurs at that distance.

$$d sin(\theta_{nc}) = n\lambda -> \theta_{nc} = sin^{-1}(\frac{n\theta}{d})$$
I think I wrote that down correctly, unless I forgot how sin reciprocals work.
This was from the lecture on 12/06-2024.

For single-slit Diffraction:
The light is conceptualized as emerging from an infinite number of point sources across the slit.

Again look at the lecture slides there's diagrams that I'm not really understanding and have no chance of replicating. There's lots of useful stuff on there but the equations are not particularly useful without the diagrams.

The diffraction pattern for the two resemble each other, the double-slit can be thought of as a single-slit centered between the two.
Except not really, because the single-slit is much more centrally focused on the points straight out beyond the slit, they are divided to the left and right much less.

Human sight is a feature of single-slit diffraction through a circular aperture(your pupil!).
With that circular aperture the angle of the innermost dark ring is given by$$sin(\theta) = $$
The equation is gone lol.
If objects are too close according to that angle, they can not be differentiated as two different objects.
A "diffraction limited" instrument is capable of differentiating up until that point of diffraction collapsing.

When two-slit diffraction occurs, and is projected onto a screen, a central maximum appears straight out from the point exactly between the two slits. When light is the [[Wave]] in question, it appears as a bright fringe.
Subsequent maxima, of order $m$, appear at distances $x_m$ away from the central maximum.
If the wavelength of the wave is $\lambda$, the distance between the slits is $d$, the distance from the slits to the screen(and also the central maximum) is $D$, the distance from the slits to the maximum of order $m$ is $r$, and the angle between the central maximum and the maximum of order $m$ is $\theta$, then$$x_m = Dtan(
\theta)$$
When $x_m<<D$, aka $\theta$ is small, then$$\theta\approx tan(\theta)\approx sin(\theta)$$ is a valid approximation, meaning that$$x_m=Dsin(\theta)$$ It is achieved by solving the "double-slit maxima equation"(idk look it up) that$$sin(\theta)=m\frac{\lambda}{d}$$
and combining those two things means that the distance of the $m$th maximum away from the central maximum $x_m$ is$$x_m=m\frac{D\lambda}{d}$$
For dark spots, or minimum, a similar process is used to get the final equation, which is instead$$y_m=(m-\frac{1}{2})\cdot\frac{D\lambda}{d}$$
Because the bright and dark spots, maxima and minima, differ from each other by exactly a half-wavelength.

APPARENTLY, and I say apparently because the only evidence I have in favor of this is that it resulted in a correct answer to a homework problem, these equations also hold true for single-slit diffraction, with $d$ being the width of the slit.

KEEP IN MIND the equations which do not contain trig terms above are ONLY able to be used if $\theta$ is small enough that the approximation holds true. You can check using a calculator to see if it holds true, because when $\theta$ is sufficiently small most calculators will lack the precision to differentiate between $\theta$, $sin(\theta)$, and $tan(\theta)$ so they'll all return the same answer.

In single-slit, if the central maximum is considered to have Intensity(See [[EM Disturbance]]) $I_0$, then a point on the screen separated from the maximum by angle $\theta$ will have intensity $I$ such that$$I=I_0\cdot(\frac{\lambda sin(\frac{\pi\cdot d\cdot sin(\theta)}{\lambda})}{\pi\cdot d\cdot sin(\theta)})^2$$
That is a HUGE mess, but that's the equation given to me in the problem. Note that in this equation $\lambda$ is the light's wavelength, $d$ is the width of the slit, and all angles and trig is done in radians.
The point will be separated on the screen by a distance $\Delta y$, which is equivalent to the $x_m$ term in the equations above, it's just distance from the central maximum.
The distance from the slit to the screen is $D$.
When $\theta$ is sufficiently small such that $D>>\Delta y$, you can use the approximation $sin(\theta)\approx\frac{\Delta y}{D}$ which makes the above equation much more manageable. Just remember that this requires you to use radians, not degrees.
With that approximation, the equation is instead$$I=I_0\cdot(\frac{\lambda sin(\frac{\pi\cdot d\cdot \frac{\Delta y}{D}}{\lambda})}{\pi\cdot d\cdot \frac{\Delta y}{D}})^2$$ Which is still an awful lot of stuff but is significantly better to deal with than the original, especially because trig can cause some serious precision losses due to rounding errors.

Diffraction Gratings are barriers with massive amounts of slits placed next to each other. You can use the number of slits per unit distance to find the distance between each slit $d$, and then the angle for an $m$th maxima away from the central maximum for a light of wavelength $\lambda$ can be found using the equation$$d\cdot sin(\theta) = m\lambda$$ And from the angle, the position on the screen can be found via basically the same strategy as above. In fact, I'll see if I can derive it myself to find if the$$x_m = m\frac{D\lambda}{d}$$ equation still works, just with $d$ defined slightly differently. It's unclear so far because the one chance I've gotten has been a situation where the $x_m << D$ or $\theta\approx sin(\theta)$ approximations didn't hold true so I couldn't use it anyway.