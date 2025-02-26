We had an equation for $r(t)$, under a central force, such as gravity, namely,
$$
m  \ddot{r}-\frac{L^{2}}{mr^{3}}=f(r)
$$
We want a curve (orbit) as $r=r(\theta)$, so we use the [[Chain Rule|chain rule]]; for any function $h$, we have:
$$
\frac{d h}{dt} =\frac{d h}{d\theta} \frac{d \theta}{dt} =\frac{d h}{d\theta} \frac{L}{mr^{2}}
$$
It is also convenient to change from $r$ to $u=\frac{1}{r}$, then
$$
\frac{d r}{dt} =\frac{d }{dt} \left( \frac{1}{u} \right)=-\frac{1}{u^{2}}\frac{d u}{d\theta} \frac{L}{mr^{2}}=-\frac{L}{m}\frac{d u}{d\theta} 
$$
And
$$
\ddot{r}=\frac{d }{dt} \frac{d r}{dt}=-\frac{L}{m}\frac{d }{dt} \frac{d u}{d\theta} =-\frac{L}{m}\frac{d ^{2}u}{d\theta^{2}} \frac{L}{m}u^{2}=-\frac{L^{2}u^{2}}{m^{2}}\frac{d ^{2}u}{d\theta^{2}} 
$$
So our original equation becomes:
$$
-\frac{L^{2}u^{2}}{m}\frac{d ^{2}u}{d\theta^{2}} -\frac{L^{2}u^{3}}{m}=f\left( \frac{1}{u} \right)
$$
$$
\implies \frac{d u^{2}}{d\theta^{2}} +u=-\frac{m}{L^{2}u^{2}}f\left( \frac{1}{u} \right)
$$
From here we need to specify $f$ to determine a solution to this differential equation
## Example
For gravity, $f(r)=-\frac{1}{r^{2}}$ with $m=1$. Our differential equation becomes:
$$
\frac{d ^{2}u}{d\theta^{2}} +u=-\frac{1}{L^{2}u^{2}}(-u^{2})=\frac{1}{L^{2}}
$$
We have a solution of the form $y_{cf}+y_{pi}$, impose $u'(0)=0$, where $u'=\frac{d u}{d\theta}$. The solution of the complimentary function $u(\theta)$ will be given by:
$$
u(\theta)=A\cos\theta
$$
Since the coefficient of $\sin\theta$ vanishes, then the particular integral will be $\frac{1}{L^{2}}$, so
$$
u(\theta)=A\cos(\theta)+\frac{1}{L^{2}}
$$
This can be written as:
$$
r(\theta)=\frac{L^{2}}{1+\varepsilon \cos\theta}
$$
Where $\varepsilon=AL^{2}$
Note if $\left| \varepsilon \right|<1$, then $r(\theta)$ is finite $\forall\theta$, so the orbit is elliptical as $r_\text{min}\leq r(\theta)\leq r_\text{max}$
Also
$$
L^{2}=r+\varepsilon r\cos\theta=r+\varepsilon x\implies r=L^{2}-\varepsilon x
$$
$$
 \implies r^{2}=x^{2}+y^{2}=(L^{2}-\varepsilon x)^{2}
$$
Which is an equation of an ellipse in the $xy$-plane
Note that $\varepsilon$ is known as the eccentricity of the ellipse
If $\varepsilon=0$, the ellipse has no eccentricity :sob: so the equation is that of a circle; $r=L^{2}$ 
___
Take $m=1,f(r)=-\frac{1}{r^{3}},u'(0)=0$, then our equation is:
$$
u''+u=-\frac{1}{L^{2}u^{2}}(-u^{3})=\frac{u}{L^{2}}
$$
$$
\implies u''+\left( 1-\frac{1}{L^{2}} \right)u=0
$$
The type of this depends on the sign of $1-\frac{1}{L^{2}}$
If $L=1$, then the solution is $u=c$, which means that $r=\frac{1}{c}$, so is a circle (of constant radius)
If initial $\underline{v}$ is perpendicular to $\underline{r}$, then $\underline{\dot{r}}(0)=0\implies u'(0)=0$ (from $\dot{r}=-\frac{L}{m}u'$), this motivates our initial condition :)
If $L>1$, then $1-\frac{1}{L^{2}}>0$, so we write $1-\frac{1}{L^{2}}=-\omega^{2}$, to give solution:
$$
u(\theta)=A\cos(\omega\theta)
$$
$$
\implies r(\theta)=\frac{1}{A\cos(\omega\theta)}
$$
```desmos-graph
A=0.8
\omega=0.3
r(\theta)=1/(A*\cos(\omega*\theta))
```
