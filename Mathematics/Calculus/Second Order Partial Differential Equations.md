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
Hmm these look like [[Eigenvalues|eigenvalue]]/eigenfunction equations.
From our initial conditions, we also have:
$$
u(0,t)=X(0)T(t)=0
$$
$$
 u(\pi,t)=X(\pi)T(t)=0
$$
We assume $T(t)\neq 0$, so we have
$$
X(0)=X(\pi)=0
$$
If $\lambda=n^{2}>0$, then
$$
X''=n^{2}X
$$
$$
\implies X=Ce^{ nx }+De^{ nx }=A\sinh(nx)+B\cosh(nx)
$$
$$
X(0)=0=B\implies X=A\sinh(nx)
$$
$$
 X(\pi)=A\sinh(nx)=0\implies A=0
$$
So $X=0$ in this case. This is not very interesting so we consider more stuff:
If $\lambda=0$, then
$$
X=Ax+B
$$
But $X(0)=X(\pi)=0$ means that we have a straight line going through $(0,0),(0,\pi)$ which must mean $X=0$, also uninteresting
If $\lambda=-n^{2}<0$, then
$$
X''=-n^{2}X
$$
$$
\implies X=A\cos(nx)+B\sin(nx)
$$
$$
 X(0)=0=A\implies X=B\sin(nx)
$$
$$
 X(\pi)=B\sin(n\pi)=0
$$
Vanishes for non-zero $B$ when $n\in\mathbb{N}$, therefore $X=A\sin(nx)$
We also have
$$
\ddot{T}=-n^{2}c^{2}T
$$
$$
\implies T=A_{n}\cos(nct)+B_{n}\sin(nct)
$$
So
$$
u(x,t)=X(x)T(t)=\sin(nx)(A_{n}\cos(nct)+B_{n}\sin(nct))
$$
So there are many solutions depending on $n$, in fact infinite solutions for each $n$. We can think of the $\sin(nx)\cos(nct)$ and $\sin(nx)\sin(nct)$ as the basis vectors, and we take a [[Linear Combinations|linear combination]] of them. So we can claim that if we sum all of them together, we have a general general solution:
$$
\sum_{n=1}^{\infty} \sin(nx)(A_{n}\cos(nct)+B_{n}\sin(nct)) 
$$
For example for $n=1$ we have a linear combination:
$$
A_{1}\sin(x)\cos(ct)+B_{1}\sin(x)\sin(ct)
$$
Which is made up of two terms, the first of which, at $t=0$ has displacement, but no velocity, then the second term has velocity, but no displacement (by taking the time derivative)
This is essentially a wobbly line like so:
![[Second Order Partial Differential Equations 2025-03-04 14.19.09.excalidraw]]
For $n=2$, we instead have:
$$
A_{2}\sin(2x)\cos(2ct)+B_{2}\sin(2x)\sin(2ct)
$$
And looks like:
![[Second Order Partial Differential Equations 2025-03-04 14.22.08.excalidraw]]
Which is double the frequency, so we can think of it as playing an octave higher. Similarly $n=3$ looks like:
![[Second Order Partial Differential Equations 2025-03-04 14.23.08.excalidraw]]
Now we consider the time derivative, the velocity:
$$
u_{t}(x,t)=\sum_{n=1}^{\infty}\sin(nx)(-ncA_{n}\sin(nct)+ncB_{n}\cos(nct))
$$
Using our initial contitions:
$$
u_{t}(x,t)=0=\sum_{n=1}^{\infty}ncB_{n}\sin(nx)\implies B_{n}=0
$$
So
$$
u(x,t)=\sum_{n=1}^{\infty}A_{n}\sin(nx)\cos(nct)
$$
We also have 
$$
u(x,0)=R(x)=\sum_{n=1}^{\infty} A_{n}\sin(nx) 
$$
Which is periodic with period $2\pi$. Now $\sin$ is odd, so this sum is in fact the odd extension of $R(x)$
![[Second Order Partial Differential Equations 2025-03-04 14.29.41.excalidraw]]
So we can work out the coefficients of using the half-range $\sin$ series;
$$
A_{n}=\frac{2}{\pi}\int _{0}^{\pi}R(x)\sin(nx) \, dx 
$$
$$
= \frac{2}{\pi}\int_{0}^{\pi/2} x\sin(nx) \, dx +\frac{2}{\pi}\int_{\frac{\pi}{2}}^{\pi} (\pi-x)\sin(nx)  \, dx =\frac{4}{\pi n^{2}}\sin\left( \frac{n\pi}{2} \right)
$$
Soooo
$$
u(x,t)=\sum_{n=1}^{\infty} \frac{4}{\pi n^{2}}\sin\left( \frac{n\pi}{2} \right)\sin(nx)\cos(nct)
$$
$$
= \frac{4}{\pi}\sin(x)\cos(ct)-\frac{4}{9\pi}\sin(3x)\cos(3ct)+\dots
$$
(note the first overtone vanishes)
```desmos-graph
c=1
t=15
y=\sum_{n=1}^{100}\frac{4}{\pi n^{2}}\sin\left(\frac{n\pi}{2}\right)\sin\left(nx\right)\cos\left(nct\right)
```
___
Further example
Consider if we have a piano that we are hitting with a piano, so for some $(0,\varepsilon)$ we give it velocity
![[Second Order Partial Differential Equations 2025-03-04 14.37.56.excalidraw]]
We have these conditions:
$$
u_{tt}=c^{2}u_{x x}
$$
$$
 u(0,t)=u(\pi,t)=0
$$
$$
 u(x,0)=0
$$
$$
 u_{t}(x,0)=S(x)=\begin{cases}
1&0\leq x\leq \varepsilon\\0&\varepsilon <x\leq \pi
\end{cases}
$$
We have our first two identical to the previous example, so we already know the general solution will be:
$$
u(x,t)=\sum_{n=1}^{\infty}\sin(nx)(A_{n}\cos(nct)+B_{n}\sin(nct))
$$
$$
u(x,0)=0=\sum_{n=1}^{\infty}A_{n}\sin(nx)\implies A_{n}=0
$$
$$
 u(x,t)=\sum_{n=1}^{\infty}\sin(nx)B_{n}\sin(nct)
$$
$$
u_{t}(x,t)=\sum_{n=1}^{\infty}\sin(nx)(ncB_{n})\cos(nct)
$$
$$
 u_{t}(x,0)=S(x)=\sum_{n=1}^{\infty}ncB_{n}\sin(nx)=\sum_{n=1}^{\infty}D_{n}\sin(nx)
$$
We can use Fourier series again to find the $D_{n}$'s but we also know that
$$
X(x)=\sin(nx)
$$
Solves
$$
X''=-n^{2}X
$$
Which is an [[Eigenfunctions|eigenfunction]] of [[Linear Differential Operators|$\mathcal{L}=\frac{d }{dx^{2}}$]], so we can guess that we have the [[Inner Product|inner product]]
$$
(f,g)=\int_{0}^{\pi} fg \, dx 
$$
So we need to show $\mathcal{L}$ is [[Self-Adjoint|self-adjoint]], 
$$
(\mathcal{L}f,g)=(f,\mathcal{L}g)
$$
$$
(\mathcal{L}f,g)=(f'',g)=\int_{0}^{\pi} f''g \, dx =[f'g-fg']_{0}^{\pi}+\int_{0}^{\pi} fg'' \, dx 
$$
And if $f,g$ are $0$ at $x=0,\pi=0$, so 
$$
[f'g-fg']_{0}^{\pi}+\int_{0}^{\pi} fg'' \, dx =0+(f,\mathcal{L}g)
$$
Which is what we wanted, so our eigenfunctions are orthogonal, i.e. 
$$
(\sin(nx),\sin(mx))=\delta_{nm}
$$
(Using the [[Kronecker Delta Function|Kronecker delta here]])
Soooo
$$
S(x)=\sum_{n=1}^{\infty}D_{n}\sin(nx)
$$
And we can consider the dot product with the eigenfunctions:
$$
(S(x),\sin(mx))=\sum_{n=1}^{\infty}D_{n}(\sin(nx),\sin(mx))=D_{m}(\sin(mx),\sin(mx))
$$
As all other terms vanish, soo
$$
D_{m}=\frac{(S(x),\sin(mx))}{(\sin(mx),\sin(mx))}=\frac{\int_{0}^{\pi} S(x)\sin(mx) \, dx }{\int_{0}^{\pi} \sin ^{2}(mx) \, dx }=\frac{2}{\pi}\int_{0}^{\pi} S(x)\sin(mx) \, dx 
$$
Which is what we would have gotten with Fourier, and now we substitute:
$$
=\frac{2}{\pi}\int_{0}^{\varepsilon} \sin(mx) \, dx =\frac{2}{\pi m}(1-\cos(m\varepsilon))=B_{m}mc
$$
So
$$
u(x,t)=\sum_{n=1}^{\infty}B_{n}\sin(nx)\sin(nct)=\sum_{n=1}^{\infty} \frac{2}{\pi n^{2}c}(1-\cos(n\varepsilon))\sin(nx)\sin(nct)
$$
