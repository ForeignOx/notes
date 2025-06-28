The heat equation is a [[Second Order Partial Differential Equations|second order]] [[Linear Partial Differential Equations|linear PDE]] of the form
$$
u_{t}=k^{2}u_{xx}
$$
$$
\implies u_{x x }-\frac{1}{k^{2}}u_{t}=0
$$
So $A=0,B=C=0$,
$$
M=\begin{pmatrix}
1&0\\0&0
\end{pmatrix},\det(M)=0
$$
So the heat equation is parabolic
The general shape to solutions look something like:
![[Heat Equation 2025-02-28 15.11.09.excalidraw]]

## Solution Using [[Fourier Transform|Fourier Transforms]]
We want the solution to the initial value problem for on the whole line, so we have $u_{t}=k^{2}u_{x x}$, and $u(x,0)=R(x)$. Start by taking the fourier transform with respect to $x$:
$$
\tilde{u}_{t}=k^{2}(ip)^{2}\tilde{u}=-k^{2}p^{2}\tilde{u}
$$
Which is a [[First Order Ordinary Differential Equations|first order ODE]],  so
$$
\tilde{u}=A(p)e^{ -k^{2}p^{2}t }
$$
$$
 \tilde{u}(p,0)=A(p)=\int_{-\infty}^{\infty} u(x,0) \, dx =\int_{-\infty}^{\infty} R(x)e^{ ipx } \, dx =\tilde{R}(p)
$$
$$
\implies \tilde{u}(p,t)=\tilde{R}(p)e^{ -k^{2}p^{2}t }=\tilde{R}(p)\tilde{g}(p)
$$
Which is a [[Gaussian Integral|gaussian]] in $p$. By the [[Convolution of Functions|convolution]] theorem, $u(x,t)=R(x)*g(x)$, we need to find $g(x,t)$ with fourier transform $\tilde{g}(p,t)=e^{ -k^{2}p^{2}t }$. Recall that
$$
g(x,t)=\Lambda e^{ -bx^{2}-cx }
$$
Has fourier transform:
$$
\tilde{g}(p,t)=\Lambda \sqrt{ \frac{\pi}{b} }e^{ -\frac{1}{4b}(p-ic)^{2} }=e^{ -p^{2}k^{2}t }
$$
$$
\implies c=0,\Lambda=\sqrt{ \frac{b}{\pi} },\frac{1}{4b}=k^{2}t\implies b=\frac{1}{4k^{2}t}
$$
$$
 \therefore g(x,t)=\frac{1}{2k\sqrt{ \pi t }}e^{ -\frac{x^{2}}{4k^{2}t} }
$$
$$
     \therefore  u(x,t)=R*g=\int_{-\infty}^{\infty} R(x')g(x-x') \, dx'=\int_{-\infty}^{\infty} R(x')\underbrace{ \left( \frac{1}{2k\sqrt{ \pi t }}e^{ -\frac{(x-x')^{2}}{4k^{2}t} } \right)  }_{ \text{Heat Kernel!} }\, dx'  
$$
And the heat kernel looks kinda like:
![[Heat Equation 2025-03-18 14.48.11.excalidraw]]
Note that the heat kernel satisfies the heat equation. As $t\to0$, the shape looks like:
![[Heat Equation 2025-03-18 14.49.54.excalidraw]]
Which can be thought about as having a lump of heat at $x'$. So our general solution can be thought of as using $R(x)$ to describe the distribution of spikes of heat 
