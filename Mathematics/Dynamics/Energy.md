Energy is the ability to do [[work]], it has a standard unit of $\pu{ J}$, the quantity of energy transferred is equal to the work done. Work is not the only way of transferring energy, [[Internal Energy|internal energy]] can be transferred by heat (conduction, convection or radiation)
## Mathematically
Consider the case of [[Newton's Second Law of Motion|Newton's second law]] where $F=F(x)$ (force depends only on [[Position|position]]). Define $V(x)=-\int F(x) \, dx$ as the potential. Then
$$
\frac{d }{dx} \left( \frac{1}{2}mv^{2} \right)=mv\frac{d v}{dx} =ma=F=-\frac{d V}{dx} 
$$
So
$$
\frac{d }{dx} \left( \frac{1}{2}mv^{2}+V \right)=0
$$
Since the derivative is 0, integrating will give us a connstant:
$$
E=\frac{1}{2}mv^{2}+V(x)
$$
This is a constant in time, so
$$
\frac{d E}{dt} =\frac{d E}{dx} \dot{x}=0
$$
The quantity $E$ is the energy of the particle, and we say that it is conserved. The term $K=\frac{1}{2}mv^{2}$ is the [[Kinetic Energy|kinetic energy]], and $V(x)$ is the potential energy, neither of these is conserved in general, but $E$ is constant in time. This means if one of kinetic and potential increases, the other decreases by the same amount
### Remarks
- A force of the form $F(x)$ is said to be conservative, since it conserves energy
- The potential $V$, and hence the energy $E$, are only defined up to an arbitrary constant; one can always add a constant of integration to either
- Using conservation of energy can give us a good picture of the particle's motion, even when we cannot get $x(t)$ explicitly
### Examples
Gravity close to the surface of a planet, taking $x$ upwards, then force is $F=-mg\implies V(x)=mgx+c$
___
Take $m=2$ and $V(x)=x^{6}$, so $E=\frac{1}{2}mv^{2}+V(x)=\dot{x}^{2}+x^{6}$, can one solve this equation of motion ($x(t)$)
$$
v=\frac{d x}{dt} =\sqrt{ E-x^{6} }
$$
(the plus or minus is whether the particle moves left or right, which is irrelevant)
$$
\implies \int \frac{1}{\sqrt{ E-x^{6} }} \, dx =\int  \, dt 
$$
However we can't do this integral :(
Note however, that $V(x)\leq E$, since $\frac{1}{2}mv^{2}\geq 0$, which restricts 

#Physics #Energy #Definition