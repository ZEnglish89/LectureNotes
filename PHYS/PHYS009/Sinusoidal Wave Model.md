
This gets its own note because I don't want to risk not understanding it or losing it somewhere else.

Used to model [[Wave]]s of course, and this was actually initially written down in [[EM Disturbance]] because those are Waves. There's some equations in there but nothing too crazy.

[[Wave]]s are given a mathematical representation in terms of an oscillation $$w(t,x,y,z)$$
to quantify the disturbance at every position in space at every instant of time.

Realistic waves are approximately sinusoidal, so this is practical.

The [[Fourier Theorem]] states that you can treat any [[Wave]] as an appropriately chosen sum of sinusoidal waves.

The expression can be simplified by ignoring $y$ and $z$ because the movement in $t,x$ is a pretty good approximation of the other dimensions. When simplified, you can have$$w(t,x) = Asin(kx-\omega t)$$
Where $A$ is the amplitude, $\omega$ is the angular frequency of the wave, the number of radians per oscillation the wave covers, $k$ is the wave number that signifies how many radians the wave cycles through per unit distance(The reciprocal of wavelength),
Remember that $sin(\theta)$ oscillates between $\pm 1$ and returns every time $\theta$ increases by a multiple of $2\pi$.
This means that the wave function will oscillate between $\pm A$ and return every time $kx-\omega t$ increases by a multiple of $2\pi$.

The wavelength $\lambda$ is the physical distance, or the change in $x$, that separates two crests(peaks) in the wave. Technically it can be measured between any two equivalent points, but it's convenient and intuitive to use the crests.
From the expression, you can find that $\lambda = \frac{2\pi}{k}$ and of course from that $k=\frac{2\pi}{\lambda}$

The Period $T$ is the time between adjacent crests, so the time it takes the Wave to "wrap around." The period can be found using the angular frequency, $T=\frac{2\pi}{\omega}$ and therefore $\omega = \frac{2\pi}{T}$.

This means that all together, the Sinusoidal Wave Model is$$w(t,x) = Asin(\frac{2\pi}{\lambda}x-\frac{2\pi}{T}t)$$
This equation isn't actually "better" per se, it just puts things in terms of wavelength instead of wave number and period instead of frequency. It sits at a slightly lower level of abstraction, if that's important to you.

Mentioned above, the [[Fourier Theorem]] means that a wave moving in $n$ dimensions is just the sum of $n$ waves of the above form, one moving in each dimension.

With some work done in lecture on 12/02-2024, you can find that $$\frac{dx}{dt} = \frac{\omega}{k}$$
So the wave will move through space in its particular direction at that speed. This is the speed at which the wave propagates through the medium, or the "phase speed" $|\vec{v}|$.
With the definitions of $\omega$ and $k$, and you can find:$$|\vec{v}| = \frac{\omega}{k} = \frac{2\pi/T}{2\pi/\lambda} = \frac{\lambda}{T} = \lambda f$$
So there are a lot of relationships between the different variables and you can find phase speed from them in a few different ways.

Note that $|\vec{v}| = \lambda f$ gives you a way to find wavelength and frequency from each other, because for lots of waves that will actually be dealt with, $|\vec{v}|$ will be equal to the speed of light $c$, and therefore $f=c/\lambda$ and $\lambda = c/f$.

The simplest relationship is $\lambda f$: The wave is moving its wavelength every time it oscillates, and it oscillates a number of times each second according to its frequency, so the total distance it moves each second is its wavelength by its frequency.

The phase speed of a wave traveling through a medium is dependent on the medium's properties more so than the wave's properties(this seems to contradict what we just said about wavelength and frequency?).
The phase speed is proportional to a ratio: The rate at which the medium restores to equilibrium over the medium's inertia.

A sinusoidal wave carries an average energy proportional to the square of its amplitude. 
For a Transverse [[Wave]] on a stretched spring, you can find that$$|\vec{v}_b| = \omega A|cos(kx-\omega t)|$$ And therefore the kinetic energy is:$$\frac{1}{2}m|\vec{v}_b|^2 = \frac{1}{2}m\omega^2A^2cos^2(kx-\omega t)$$
And because of the behavior of $cos^2$,$$K_{avg} = \frac{1}{4}m\omega^2A^2\propto A^2$$

Spherical Waves can be represented by$$w(t,x,y,z) = A(r)sin(kr-\omega t)$$
Where $r=\sqrt{x^2+y^2+z^2}$
At any instant of time, the crests of the wave form nested spherical shells around the origin of the wave at $r=0$

The energy contained within the wave is spread over those spherical shells which have a surface area of $4\pi r^2$, and that energy is delivered as the shells expand, therefore decreasing in the form $\frac{1}{r^2}$.

Consider a sinusoidal [[Wave]] in Water. Successive crests form parallel lines, the waves flowing in the ocean are not just a single point but a wall of water.
These are referred to as Line Waves.
With coordinates chosen such that the wave moves in the $+x$ direction and the surface of the water lies in the $xy$ plane:$$w(t,x,y) = Asin(kx-\omega t)$$
For comparison, a Circular Wave moves in concentric circles:$$w(t,x,y) = A(r,\theta)sin(kx-\omega t)$$
where $r=\sqrt{x^2+y^2}$.

Linear Intensity of a wave is equal to $\frac{power}{length}$ and is proportional to $A^2$.
This is relevant for [[Diffraction]].