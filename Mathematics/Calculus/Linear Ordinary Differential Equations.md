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
