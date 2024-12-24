
This method works ONLY if the "forcing terms" have finite numbers of derivatives with [[Linear Independence]].
$$mx''+bx'+kx=f(t)$$
Where $f(t)$ is a "forcing term."
For example, $f(x)=cos(2x), -2sin(2x), -4cos(2x), 8sin(2x)...$
There are of course infinite derivatives here, but there are also only two: $cos(2x)$ and $sin(2x)$, and the differing constants are secondary.
$f(x)=x^3,3t^2,6t,6,0$
The set up until, but not including, $0$, are Linearly Independent. Any set including 0 will necessarily become Dependent.
$f(x)=\frac{1}{t},-\frac{1}{t^2},\frac{2}{t^3},-\frac{6}{t^4}...$
These all have [[Linear Independence]], but they will go on infinitely, so there will not actually be a way to work with them and solve a problem.

Haik did two examples with this method on 11/13-2024, and I followed along with one of them in my notebook. I'll have to go back and codify how this works a little bit.

Find the homogeneous solution first. Assume it has the form $x=e^{\lambda t}$.
That assumption gets you a deterministic equation of the form $\lambda^2+b\lambda+c=0$.
This can be factored to find $\lambda$, which will often have multiple values, that's how factoring works.
Therefore, $$x_h=c_1e^{\lambda_1t}+c_2e^{\lambda_2t}$$
is your homogeneous solution.

From there, it's a fucking mess and as usual Haik is just saying "guess and you need your guess to be right and if you aren't guessing right you must just be stupid." I'm a little upset at him right now. These notes are now my diary lmao.

Lecture Notes 4.4 handle this. Haik gave good lectures at the start of the semester but he's gradually devolved. I think he's too preoccupied with making himself feel smart to actually teach.