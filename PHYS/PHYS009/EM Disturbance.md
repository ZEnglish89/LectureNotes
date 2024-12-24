A Disturbance in a [[Field]] of the [[Electromagnetic Force]], or an [[Electromagnetic Field]].
Also called [[Wave]]s, waves are literally just disturbances.

If you imagine an infinite charged sheet in the $y-z$-plane with $x=0$, and you leave that sheet at rest, it will give off or create an [[Electric Field]] with $E_x$ is constant and $E_y=E_z=0$ and no [[Magnetic Field]].

If the sheet is moved up and down, $\pm z$, then there will be [[Current]], the movement of [[Charge]], creating a [[Magnetic Field]].

When $\rho=0$ and $\vec{J}=0$, [[Charge Distribution]] and [[Current Density]] are 0, such as in empty space, then [[Maxwell's Equations]] reduce to simpler forms.
Under these conditions, $$\frac{\partial E_x}{\partial x}+\frac{\partial E_y}{\partial y}+\frac{\partial E_z}{\partial z}=0$$$$\frac{\partial B_x}{\partial x}+\frac{\partial B_y}{\partial y}+\frac{\partial B_z}{\partial z}=0$$
And in the above, most of the components are already known to be zero.
$$\frac{1}{\mu_0\epsilon_0}\frac{\partial^2 B_y}{\partial^2x}-\frac{\partial^2B_y}{\partial t^2} =0$$

After this Borna legit wrote down a Second-[[Order]] [[Partial Differential Equation]] which is a topic you don't even get to in MATH024:$$B_y = f(h) = F(h) = F(t-(\mu_0\epsilon_0)^{\frac{1}{2}}x)$$
And from this he got:$$|\vec{v}|=|\frac{\Delta x}{\Delta t}| = \frac{|\Delta x}{}$$
Which he moved on from too fast for me to type.

A big old equation that solves for the speed of light.
This basically just means that [[Field]]s propagate at the speed of light, and therefore any disturbances or changes to the field will spread out from the point at which the disturbance is initiated at the speed of light.
This was followed by another history lesson about the discovery of radio waves. Pretty cool but I'm still preoccupied with all those equations we brushed over.

As such, a disturbance in $\vec{B}$ is also always accompanied by a disturbance in $\vec{E}$ and vice-versa. This is actually a consequence of [[Faraday's Law]].

The relationship between the two [[Field]]s can be found to be$$E_z = -cf(h) = -cB_y = -\bar{B}_y$$
The important thing to remember here is that $|\vec{E}| = |c\vec{B}| = |\vec{\bar{B}}|$ for a field in a vacuum.

This was solved for in a full-slide series of equations, but it's crazy.

The Wave Motion $\bar{B}$ is in the direction of $\vec{E}\times\vec{B}$, according to the right-hand rule.

An EM Wave is a "transverse" wave. This means that a traveling EM Disturbance moving through empty space will have NO [[Field]] components in the direction of its motion.

EM Waves have two independent polarizations. Returning to the infinite sheet of [[Charge]], if the sheet is jostled in a single direction, a disturbance wave function is created only in that dimension, so if the sheet is jostled within a single plane, the disturbance function is the result of a superposition of the wave functions corresponding to the directions which that plane contains.
Moving the sheet diagonally in the $y$ and $z$ directions will create a superposition of the $y$ and $z$ disturbance functions.

Borna derived the following on the board:$$\nabla\times\vec{E} = -\frac{\partial\vec{B}}{\partial t}$$
If you take the curl of both sides, you get$$\nabla\times\nabla\times\vec{E} = -\frac{\partial}{\partial t}(\nabla\times\vec{B}) = -\mu_0\epsilon_0\frac{\partial^2\vec{E}}{\partial t^2}$$
His final form of the equation, with both sides expanded out, was:$$\nabla^2\vec{E} = \mu_0\epsilon_0\frac{\partial^2\vec{E}}{\partial t^2}$$
Which he said was a wave equation.
You can do the same thing with [[Magnetism]] and you get:$$\nabla^2\vec{B}=\mu_0\epsilon_0\frac{\partial^2\vec{E}}{\partial t^2}$$
It's weird to me that both of those are related to the exact same expression in terms of the [[Electric Field]], despite one being electric and one being magnetic.

Properties:
Intensity:
The energy density of an EM Disturbance is:$$u_{EM} = \frac{1}{2}\epsilon_0(|\vec{E}|^2+|\vec{\bar{B}}|^2)$$
Where $\vec{\bar{B}} = c\vec{B}$,  and $|\vec{E}| = |\vec{\bar{B}}|$. Because of that relationship between $E$ and $\bar{B}$, we can simplify the above equation to: $$u_{EM} = \epsilon_0|\vec{E}|^2$$
Because Intensity is power per unit Area, we can find that the average intensity of a Wave will be$$I_{avg} = c\epsilon_0[|\vec{E}|^2]_{avg}$$
With $\vec{E} = E_0sin(kx-\omega t)\hat{y}$ you can find that$$I_{avg} = c\epsilon_0\frac{E_0^2}{2}$$
The direction of the wave can be determined using the Poynting{sic} Vector$$\vec{S} = \frac{1}{\mu_0}(\vec{E}\times\vec{B}) = \frac{E_0^2}{c\mu_0}$$
The magnitude of the Poynting Vector represents the energy transfer per unit area of the wave.

Unpolarized light can be polarized by passing through a filter, which would remove the portions in particular directions, therefore polarizing it and reducing its magnitude. Like sunglasses.
Check out [[Malus's Law]].


For constant intensity waves, the relevant component is:$$E_{x/y/z} = E_0sin(2\pi f[t-\frac{x}{c}])$$
The energy of a Photon can be related to either the Frequency or Wavelength of an EM Wave using one of the following two equations:$$E = hf$$
or $$E = \frac{hc}{\lambda}$$
$f$ is the frequency, $\lambda$ is the wavelength, and for both equations $h = 6.62607015\times10^{-34}\frac {J}{Hz}$ is the Planck Constant.

When a light beam strikes a surface, it creates a Radiation Pressure:$$p=\frac{I_{ab}}{c}$$
Where $I_{ab}$ is the Intensity of the portion of the light that is absorbed. [[Malus's Law]] defines what portion of the light's total intensity is transmitted when it strikes an ideal polarizer, and everything that is not transmitted is absorbed.
Remember that the Force exerted by a Pressure on a surface is defined by$$F=pA$$
Where $A$ is the surface or cross-sectional area of the surface.
Therefore, the Force exerted on an ideal polarizer by a light beam can be derived to be$$F_L = \frac{I_0-(I_0cos^2(\theta))}{c}\cdot A$$