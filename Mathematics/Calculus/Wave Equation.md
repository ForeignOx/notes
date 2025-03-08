The wave equation is a [[Second Order Partial Differential Equations|second order]] [[Linear Partial Differential Equations|linear PDE]] of the form
$$
u_{tt}=c^{2}u_{x x}
$$
$$
\implies c^{2}u_{ x x}-u_{tt}=0
$$
$$
\implies M=\begin{pmatrix}
c^{2}&0\\0&-1
\end{pmatrix}
$$
$$
\implies \det(M)=-c^{2}<0
$$
So the Wave equation is a hyperbolic PDE
On the whole line, the general solution is:
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
We can think of this as having two lumps $f$ and $g$, moving along a line at speed $c$ towards each other:
![[Wave Equation 2025-02-27 14.53.07.excalidraw]]
## Derivation
![[Wave Equation 2025-03-03 14.15.45.excalidraw]]
If you have a thin string which lies along the $x$-axis, and is moved a small distance in an orthogonal direction (for example plucking the strings on a musical instrument) called $u$. Acceleration is $\ddot{u}$, but $u=u(x,t)$, so this is in fact $\frac{ \partial^{2}u }{ \partial t^{2} }$. The string is uniform with [[Density|density]] (mass per unit length) $\rho$; so the mass of the piece from $x$ to $\delta x$ is $\rho\delta x$. The force comes from the [[Tension|tension]] along the string: it is a vector $\underline{T}$ with constant magnitude $T$. The force acts on a piece of string between $x$ and $x+\delta x$
We will assume $\theta$ is small since there was only a small displacement. The $x$-component of the force involves $T\cos(\theta)$ (positive at $x+\delta x$, but negative at $x$); but $\cos(\theta)= 1-\frac{\theta^{2}}{2}+\dots \approx1$, so no net $x$-component. The $u$-component is $T\sin(\theta)(x+\delta x)-T\sin(\theta)x$, so the equation of motion is:
$$
(\rho\delta x)\frac{ \partial^{2}u }{ \partial t^{2} } =T(\sin(\theta)(x+\delta x)-\sin(\theta)x)
$$
However, since $\theta$ is small, we can say $\sin\theta \approx\theta \approx \tan\theta=\frac{\delta u}{\delta x}$, and by dividing by $\rho\delta x$, our equation becomes:
$$
\frac{ \partial^{2}u }{ \partial t^{2} } =\frac{T}{\rho} \frac{1}{\delta x}\left( \frac{\delta u}{\delta x}(x+\delta x)-\frac{\delta u}{\delta x}(x) \right)
$$
Now we take the limit as $\delta x\to0$, where we say (assume) that $\frac{\delta u}{\delta x}=\frac{ \partial u }{ \partial x }$, and we also use the definition of the derivative that:
$$
\lim_{ \delta x \to 0 }  \frac{f(x+\delta x)-f(x)}{\delta x}=\frac{ \partial f }{ \partial x } 
$$
Where we put $f=\frac{ \partial u }{ \partial x }$, so we get
$$
\frac{ \partial^{2}u }{ \partial t^{2} } =\frac{T}{\rho}\frac{ \partial^{2}u }{ \partial x^{2} } 
$$
Which we tend to rewrite:
$$
u_{tt}=c^{2}u_{x x}
$$
Where $c=\sqrt{ \frac{T}{\rho} }$ is the wave speed
## General Solution
Let $f(p)$ be a function of one variable $p$, and take $u(x,t)=f(x-ct)$, (so we are letting $p=x-ct$) then we can substitute this in after doing a bit of brunt work using the [[Chain Rule|chain rule]]:
$$
\frac{ \partial u }{ \partial x } =\frac{d f}{dp} \frac{ \partial p }{ \partial x } =\frac{d f}{dp} 
$$
$$
\implies \frac{ \partial^{2}u }{ \partial x^{2} } =\frac{ \partial  }{ \partial x } \left( \frac{d f}{dp}  \right)=\frac{d ^{2}f}{dp^{2}} 
$$
$$
\frac{ \partial u }{ \partial t } =\frac{d f}{dp} \frac{ \partial p }{ \partial t } =\frac{d f}{dp} (-c)
$$
$$
\implies \frac{ \partial^{2}u }{ \partial t^{2} }-0c\frac{ \partial  }{ \partial t } \left( \frac{d f}{dt}  \right)=-c\frac{d ^{2}f}{dp^{2}} (-c)=c^{2}\frac{d ^{2}f}{dp^{2}}  
$$
So this equation must be a solution to the wave equation as:
$$
\frac{ \partial^{2}u }{ \partial t^{2} } -c^{2}\frac{ \partial^{2}u }{ \partial x^{2} } =c^{2}\frac{d ^{2}f}{dp^{2}} -c^{2}\frac{d ^{2}f}{dp^{2}} =0
$$
So $u(x,t)=f(x-ct)$ represents a wave travelling along the string for any $f(p)$. Take for example $f(p)$ :
![[Wave Equation 2025-03-03 14.46.26.excalidraw]]
Then we can make the same shape for
![[Wave Equation 2025-03-03 14.47.22.excalidraw]]
We can consider $t=10$,
![[Wave Equation 2025-03-03 14.49.40.excalidraw]]
This is a wave travelling rightwards with speed $c$, but the profile is the same
Another solution of the wave equation is obtained by taking any function $g(q)$ and putting
$$
u(x,t)=g(x+ct)
$$
Which is a wave of fixed shape moving in negative direction at speed $c$
Since the wave equation is [[linear|linear]] in $u$, if $u_{1},u_{2}$ are solutions, then so is $u=u_{1}+u_{2}$, so for any $f(p),g(q)$, the function
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
We claim that this is the general solution
We need to prove that if we specify initial conditions at $t=0$, namely $u(x,0)=R(x)$, the initial position, and $\frac{ \partial u }{ \partial t }(x,t)|_{t=0}=S(x)$, the initial velocity, then we need to find $f(p),g(q)$ such that
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
Has those initial conditions
### Proof
We have 
$$
u(x,0)=f(x)+g(x)=R(x)
$$
$$
\dot{u}(x,0)=c(g'(x)-f'(x))=S(x)
$$
By integrating with respect to $x$, we get
$$
-cf(x)+cg(x)=\int_{0}^{x} S(x) \, dx 
$$
So we can solve these to get:
$$
f(x)=\frac{1}{2}\left( R(x)-\frac{1}{c}\int_{0}^{x} S(x) \, dx  \right)
$$
$$
 g(x)=\frac{1}{2}\left( R(x)+\frac{1}{c}\int_{0}^{x} S(x) \, dx  \right)
$$
Which proves that $f(x-ct)+g(x+ct)$ is the general solution
## D'Alembert's Formula
We've shown that
$$
u(x,t)=\frac{1}{2}\left( R(x-ct)-\frac{1}{c}\int_{0}^{x-ct} S(x) \, dx  \right)+\frac{1}{2}\left( R(x+ct)+\frac{1}{c}\int_{0}^{x+ct} S(x) \, dx  \right)
$$
And since $\int_{0}^{a}-\int_{0}^{b}=\int_{b}^{a}$, we have
$$
u(x,t)=\frac{1}{2}(R(x-ct)+R(x+ct))+\frac{1}{2c}\int_{x-ct}^{x+ct} S(x) \, dx 
$$
## Examples
An infinite string is plucked, so $S(x)=0$, with $R(x)=e^{ -x^{2} }$. Then
$$
u(x,t)=\frac{1}{2}e^{ -(x-ct)^{2} }+\frac{1}{2}e^{ -(x+ct)^{2} }
$$
```desmos-graph
R\left(x\right)=e^{-x^{2}}
S\left(x\right)=0
t=1.8
c=2.3
\frac{1}{2}\left(R\left(x-ct\right)+R\left(x+ct\right)\right)+\frac{1}{2c}\int_{x-ct}^{x+ct}S\left(a\right)da
```
Instead, strike the string, so $R(x)=0$, take $S(x)=xe^{ -x^{2} }$, here $\int S(x)  \, dx=-\frac{1}{2}e^{ -x^{2} }$ and
$$
u(x,t)=-\frac{1}{4c}(e^{ -(x+ct)^{2} }-e^{ -(x-ct)^{2} })
$$
```desmos-graph
R\left(x\right)=0
S\left(x\right)=xe^{-x^{2}}
t=1.8
c=1
\frac{1}{2}\left(R\left(x-ct\right)+R\left(x+ct\right)\right)+\frac{1}{2c}\int_{x-ct}^{x+ct}S\left(a\right)da
```
___
Solve $4\frac{ \partial^{2}u }{ \partial t^{2} }=\frac{ \partial^{2}u }{ \partial x^{2} }$ with $u(x,0)=\frac{1}{1+x^{2}}$, and $\frac{ \partial u }{ \partial t }(x,t)|_{t=0}=\frac{x}{(1+x^{2})^{2}}$, this has the solution
$$
\int S \, dx =\int \frac{x}{(1+x^{2})^{2}} \, dx =-\frac{1}{2} \frac{1}{1+x^{2}}=-\frac{1}{2}R(x)
$$
(note $c=\frac{1}{2}$), so
$$
u(x,t)=\frac{1}{2}R(x+ct)+\frac{1}{2}R(x-ct)-\frac{1}{2}R(x+ct)+\frac{1}{2}R(x-ct)=R(x-ct)=\frac{1}{1+(x-ct)^{2}}
$$
$$
=\frac{1}{1+\left( x-\frac{t}{2} \right)^{2}}
$$

$$
