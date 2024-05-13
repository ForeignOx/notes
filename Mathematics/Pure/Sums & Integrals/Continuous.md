**PDF** (probability density function), as opposed to PMF (probability mass function) for discrete, is essentially a distribution curve, and area in the interval of $\mathbb{R}$ should equal 1, ie if you have a PDF $f_{X}(x)$ then $\int _{\mathbb{R}}f_{x}(x) \, dx$
$$
P(a\leq X\leq b)=\int ^{b}_{a} f_{X}(x) \, dx  
$$
CDF (cumulative density function) will only increase, so for a CDF $F_{X}(x)$
$$
F_{X}(x)=\int _{-\infty}^{x}f_{X}(t) \, dt =F_{X}(b)-F_{X}(a)
$$
E(X) for a continuous distribution is
$$
E(X)=\int _{\mathbb{R}}xf_{X}(x) \, dx 
$$
Var(X) for a continuous distribution is
$$
Var(X)=\int _{\mathbb{R}} (x-\mu)^{2}f_{X}(x) \, dx 
$$
## Continuous uniform
$$
f_{X}(x)=\begin{cases}
\frac{1}{b-a}& a\leq X\leq b
\\ 0 & \text{otherwise}
\end{cases}
$$
This has a CDF of 
$$
F_{X}(x)=\int _{a}^{x} \frac{1}{b-a} \, dx 
$$
## Normal
Consider throwing darts at a dartboard, there will be more closer to the centre, and it will be normally distributed assuming they are radially symmetrical, the probability of having a dart at some distance r is $w(r)dA=f(x)f(y)dA\implies f(x)f(y)=\omega(r)$
$$
f(x)f(y)=\omega\sqrt{ x^{2}+y^{2} }
$$
Without loss of generality, $y=0$
$$
\implies f(x)\lambda=\omega \sqrt{ x^{2}+y^{2} }
$$
$$
\implies \omega \sqrt{ x^{2}+y^{2} }=\lambda f(\sqrt{ x^{2}+y^{2} })
$$
$$
\implies f(x)f(y)=\lambda f(\sqrt{ x^{2}+y^{2} })
$$
$$
\implies g(x)g(y)=g(\sqrt{ x^{2}+y^{2} })
$$
Which will be solved by $g(x)=e^{kx^{2}}$, so $f(x)=\lambda e^{ kx^{2} }$, which we want to converge, so we can say
$$
f(x)=\lambda e^{ -a^{2}x^{2} }
$$
And we want 
$$
\int _{\mathbb{R}} e^{ -a^{2}x^{2} } \, dx =1
$$
Consider 
$$
\int _{\mathbb{R}} e^{ -x^{2} } \, dx 
$$
and 
$$
\int _{\mathbb{R}} e^{-y^{2}}\, dy
$$
Using Fabini's theorem,
$$
\iint_{\mathbb{R}^{2}} e^{-x^{2}-y^{2}} \,dxdy
$$

dsoijsfoijsd


$$
\therefore \int \lambda e^{-a^{2}x^{2}} \, dx 
$$
doijsdoij

$$
\implies f(x)=\lambda e^{ -\pi\lambda^{2} x^{2} }
$$
and we know
$$
\sigma^{2}=oijsdoij = \frac{1}{2\pi \lambda^{2}}
$$
Solve for $\lambda$
$$
\therefore f(x) = \frac{1}{\sigma \cap stuf()}
$$
## Joint distributions
Consider random variables $X,Y$, which are jointly continuous if $\exists f_{X,Y}\geq 0, f_{X,Y}:\mathbb{R}^{2}\to \mathbb{R}$ 

