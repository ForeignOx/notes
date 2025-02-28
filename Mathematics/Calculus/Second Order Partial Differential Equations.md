## [[Linear Partial Differential Equations|Linear]] PDEs of Two Variables
If we have some function $u(x,t)$, then we have a general partial differential equation:
$$
Au_{xx}+2Bu_{xt}+Cu_{tt}+Du_{x}+Eu_{t}+Fu=0
$$
Where $A,B,C,D,E,F$ could depend on $x,t$
PDEs are classified according to the sign of
$$
\det(M),M=\begin{pmatrix}
A&B\\B&C
\end{pmatrix}
$$
### Hyperbolic PDE
If $\det(M)<0$, then the PDE is hyperbolic. An equation of this form is the [[Wave Equation|Wave equation]]
These describe propagation along lines
### Parabolic PDE
If $\det (M)=0$, then the PDE is parabolic. An equation of this form is the [[Heat Equation|Heat equation]] 
### Elliptic PDE
If $\det(M)>0$, then the PDE is elliptical. An equation of this form is [[Laplace's Equation|Laplace's Equation]]
___
A linear PDE solution space is an infinite-[[Dimension|dimensional]] [[Vectorspaces|vectorspace]], so
$$
u(x,t)=\sum_{i} a_{i}u_{i}(x,t) 
$$
Which is an infinite sum (or an integral)
We need to specify $\infty$ of $a_{i}$ numbers (or functions) to pin down $u$
___
## Important Examples
Consider an IVP on the whole line $x$, for example the transverse displacement of infinitely long string obeys the wave equation $u_{tt}=c^{2}u_{x x}$:
![[Second Order Partial Differential Equations 2025-02-28 15.25.24.excalidraw]]
We can define the initial position $u(x,0)=R(x)$, and the initial velocity $u_{t}(x,0)=S(x)$
If instead we have an infinitely long bar of metal, we might want to use the heat equation to model its heat, so it obeys $u_{t}=k^{2}u_{x x}$
![[Second Order Partial Differential Equations 2025-02-28 15.28.04.excalidraw]]
For the heat equation on the whole line we need $u(x,0)=R(x)$
If we switch to finite pieces of string/metal, we instead do things on an interval $x\in[a,b]$ and we can consider the $xt$-plane:
![[Second Order Partial Differential Equations 2025-02-28 15.29.55.excalidraw]]
For the wave equation, at $t=0,u(x,0)=R(x)$ for $a\leq x\leq b$, and $u_{t}(x,0)=S(x)$ for $a\leq x\leq b$
But we need to specify what happens at the endpoints; boundary conditions: 
- $u(b,t)=0$ would be known as a fixed end Dirichlet boundary condition
- $u_{x}(b,t)=0$ would be known as a fixed end Neumann boundary condition
- And the same thing but at $x=a$
For the heat equation, it's the same except for the first part, we don't need $u_{t}$, so only $u(x,0)=R(x)$
For Laplace's equation, we have a similar sort of thing, but we either specify $u$ or a normal derivative of $u$ on boundary
## Method of Separation of Variables
The solution space will look like:
$$
u(x,t)=\sum_{i}a_{i}u_{i}(x,t)
$$
Where the $u_{i}(x,t)$ are our [[Basis|basis]] [[Functions|functions]]. We will choose basis functions of the form:
$$
u_{i}(x,t)=X_{i}(x)T_{i}(t)
$$
Such that we can separate out $x$ and $t$
___
### Example
For a string lying between $x=0,x=\pi$, this has transverse displacement and obeys the wave equation $u_{tt}=c^{2}u_{x x}$ at ends $u(0,t)=u(\pi,t)=0$
We can impose initial conditions $u_{t}(x,0)=0$,
$$
u(x,0)=R(x)=\begin{cases}
x&0\leq x\leq \frac{\pi}{2}\\ \pi-x&  \frac{\pi}{2}\leq x\leq \pi
\end{cases}
$$
So we look for a solution satisfying these of the form $u(x,t)=X(x)T(t)$, we substitue into the wave equation:
$$
u_{tt}=X\ddot{T}=c^{2}u_{x x}X''T
$$
Dividing through by $c^{2}XT$:
$$
\frac{X\ddot{T}}{c^{2}XT}=\frac{c^{2}X''T}{c^{2}XT}
$$
$$
\implies \frac{\ddot{T}}{c^{2}T}=\frac{X''}{X}
$$
Since these are two functions of different variables, they can only be equal if they are both constant, so our PDE has become $\hspace{0pt}2$ ODEs, yayy:
$$
X''=\lambda X
$$
$$
 \ddot{T}=\lambda c^{2}T
$$
Hmm these look like [[Eigenvalues|eigenvalue]]/eigenfunction equations, 