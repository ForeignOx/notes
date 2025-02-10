What if $\sigma$ is unknown and $n$ is smol? If $X_{i}\sim N(\mu,\sigma^{2})$ or approximately normal
We still use $s$ to estimate $\sigma$, but now:
$$
\frac{\bar{X}-\mu}{\frac{S}{\sqrt{ n }}}\sim t_{n-1}
$$
This is a $t$-distribution with $n-1$ degrees of freedom
Everything proceeds as before, but we use $t_{n-1}$ tables instead of normal talbes :sob:
## Definition
A random variable $T-t$ (when measured) has a $t$-distribution with degrees of freedom parameter $\nu$, where $\nu=n-1$, if it has the following pdf:
$$
f(t|\nu)=\frac{\Gamma\left( \frac{\nu+1}{2} \right)}{\sqrt{ \nu \pi }\Gamma\left( \frac{\nu}{2} \right)}\left( 1+\frac{t^{2}}{\nu} \right)^{- \frac{\nu+1}{2}}
$$
We write
$$
T\sim t_{\nu}
$$
Note $E(T)=0$, $Var(T)=\frac{\nu}{\nu-2}$
The limit as $n\to \infty$ is $t_{n-1}\to N(0,1)$
