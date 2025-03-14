An $n$th order [[Linear|linear]] ordinary [[Differential Equations|differential equation]] can be written
$$
\frac{d ^{n}y}{dx^{n}} +p_{1}(x)\frac{d ^{n-1}y}{dx^{n-1}}+p_{2}(x)\frac{d ^{n-2}y}{dx^{n-2}} +\dots+p_{n-1}(x)\frac{d y}{dx} +p_{n}(x)y(x)=C(x) 
$$
If $C\neq 0$, then they are inhomogeneous. If $C=0$, they are homogeneous.
Linear is a constraint on how the independent variable, $y$, appears (only have $y$ or one of its derivatives appearing in each term)
The general solution to an $n$th order differential equation has $n$ parameters in it
Linear equations are non-linear equation because of the principle of superposition, so the solution space of a linear homogeneous ODE is a [[Vectorspaces|vectorspace]]. Hence, if I find $n$ [[Linear Independence|linearly independent]] solutions $y_{1},\dots,y_{n}$ to my equation, they are a [[basis|basis]] for my solution space, so the general solution is a [[Linear Combinations|linear combination]] of these:
$$
y(x)=\alpha_{1}y_{1}(x)+\alpha_{2}y_{2}(x)+\dots+\alpha_{n}y_{n}(x)
$$
The general form of solution of an inhomogeneous equation is
$$
y(x)=y_{PI}+y_{CF}=y_{PI}+(\alpha_{1}y_{1}(x)+\alpha_{2}y_{2}(x)+\dots+\alpha_{n}y_{n}(x))
$$
Where $y_{PI}$ is a solution to the inhomogeneous equation, and $y_{CF}$ is the general solution to the homogeneous equation. Note that this is an affine space
In general, if $p_{1},\dots,p_{n}$ are not constants, the solutions cannot be written in terms of elementary functions
For a particular solution, you need to specify $\alpha_{1},\alpha_{2},\dots,\alpha_{n}$, the $n$ boundary conditions
## Series Solutions
In order to allow for a wide-class of solutions, we can consider [[Series|series]] solutions by substituting $y=\sum_{k=0}^{\infty} a_{k}x^{k}$ and solving the [[Recurrence Relations|recurrence relation]] for $a_{k}$
## Using [[Fourier Transform|Fourier Transforms]] to help with Inhomogeneous ODEs
If we take derivatives of $f(x)$ in $x$-space, this corresponds to multiplying $\tilde{f}(p)$ by $ip$ in $p$-space, so a differential equation in $x$-space becomes an algebraic equation
So we can solve for $\tilde{y}(p)$ and then return to $x$-space to get a solution $y(x)$
### Example
$$
\frac{d y}{dx} +3y=f(x)
$$
Taking the fourier transform of both sides gies:
$$
ip\tilde{y}=3\tilde{y}=\tilde{f}(p)
$$
$$
\implies \tilde{y}(p)=\frac{\tilde{f}(p)}{ip+3}=\tilde{f}(p)\tilde{g}(p)
$$
Where $\tilde{g}(p)=\frac{1}{ip+3}$
So if I can find $g(x)$ such that $\tilde{g}(p)=\frac{1}{ip+3}$, then using the [[Convolution of Functions|convolution]] theorem, we find that the fourier transform of $f*g$ is $\tilde{f}(p)\tilde{g}(p)$ i.e. we can take $y=f*g$
The one-sided exponential 
$$
g(x)=\begin{cases}
e^{ -ax } & x\geq 0\\0 & x<0
\end{cases}
$$
Has Fourier transform $\frac{1}{ip+a}$, so we can take $g(x)=e^{ -3x }$ for $x\geq 0$ and find that
$$
    y(x)=f*g=\int_{-\infty}^{\infty} f(t)g(x-t) \, dt=\int_{-\infty}^{x} f(t)e^{ -3(x-t) } \, dt=e^{ -3x }\int_{-\infty}^{x} f(t)e^{ 3t } \, dt
$$
This makes sense as if we used the integrating factor method, the integrating factor is $e^{ 3x }$, and we get that
$$
y=\frac{1}{e^{ 3x }}\int_{}^{x} f(t)e^{ 3t } \, dt 
$$
___

