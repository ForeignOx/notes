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