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
## In $\mathbb{R}^{3}$
A force $\underline{F}(\underline{r})$ is conservative if there exists a real function $V(\underline{r})=V(x,y,z)$ such that 
$$
\underline{F}=-\frac{ \partial V }{ \partial x } \underline{e}_{1}-\frac{ \partial V }{ \partial y } \underline{e}_{2}-\frac{ \partial V }{ \partial z } \underline{e}_{3}=-\underline{\nabla V} 
$$
### Conservation of Energy
A particle of mass $m$ moving in a conservative force $\underline{F}$ has conserved energy $E$, where
$$
E=\frac{1}{2}mv^{2}+V
$$
Where $v$ is its speed. Again the first part is the kinetic energy, the second part is the potential energy
So $\frac{d E}{dt}=0$
#### Proof
First:
$$
\frac{d V}{dt} =\frac{ \partial V }{ \partial x } \frac{d x}{dt} +\frac{ \partial V }{ \partial y } \frac{d y}{dt} +\frac{ \partial V }{ \partial z } \frac{d z}{dt} 
$$
Write
$$
\underline{F}=F_{x}\underline{e}_{1}+F_{y}\underline{e}_{2}+F_{z}\underline{e}_{3}
$$
Then
$$
\frac{d V}{dt} =-F_{x}\dot{x}-F_{y}\dot{y}-F_{z}\dot{z}=-\underline{F}\cdot  \underline{\dot{r}}
$$
Then using $v^{2}=\underline{\dot{r}}\cdot  \underline{\dot{r}}$
$$
\frac{d }{dt} \left( \frac{1}{2}mv^{2} \right)=\frac{d }{dt}\left( \frac{1}{2}m(\dot{x}^{2}+\dot{y}^{2}+\dot{z}^{2}) \right)=m(\dot{x}\ddot{x} +\dot{y}\ddot{y}+\dot{z}\ddot{z})-m \underline{\dot{r}}\cdot  \underline{\ddot{r}}
$$
Thus:
$$
\frac{d E}{dt} = \underline{\dot{r}}\cdot(m  \underline{\ddot{r}}-\underline{F})=0
$$
By equation of motion
### Criterion for Conservative Forces
$\underline{F}$ is conservative iff
$$
\frac{ \partial F_{x} }{ \partial y } =\frac{ \partial F_{y} }{ \partial x } ,\frac{ \partial F_{y} }{ \partial z } =\frac{ \partial F_{z} }{ \partial y } ,\frac{ \partial F_{x} }{ \partial z } =\frac{ \partial F_{z} }{ \partial x } 
$$
#### Proof
Suppose $F$ is conservative, so $F_{x}=-\frac{ \partial V }{ \partial x }$ etc, then
$$
\frac{ \partial F_{x} }{ \partial y } -\frac{ \partial F_{y} }{ \partial x } =-\frac{ \partial^{2}V }{ \partial y\partial x }+ \frac{ \partial^{2}V }{ \partial x\partial y } =0 
$$

You can do the same for the other two by symmetry
#### Remark
In parctice, if given $\underline{F}$, just try to find $V$, if you can, then it is conservative
#### Example
Let $\underline{F}=(z-y)\underline{e}_{1}+(\alpha x-z)\underline{e}_{2}+(\beta x-y)\underline{e}_{3}$, for which values of $\alpha,\beta$ is $\underline{F}$ conservative? For those $\alpha,\beta$, find $V$
Solve
$$
\frac{ \partial V }{ \partial x } -F_{x},\frac{ \partial V }{ \partial y } =-F_{y},\frac{ \partial V }{ \partial z } =-F_{z}
$$
$$
V=(y-z)x+g(y,z)
$$
Substituting this into the $y$-equation:
$$
\frac{ \partial V }{ \partial y } =x+\frac{ \partial g }{ \partial y } =z-\alpha x\iff \alpha=-1, \frac{ \partial g(y,z) }{ \partial y } =z
$$
So
$$
g=zy+h(z)
$$
Finally substitute $V=(y-z)x+zy+h(z)$ into $z$ equation:
$$
\frac{ \partial V }{ \partial z } =y-\beta x=-x+y+\frac{d h}{dz} 
$$
Only if $\beta=1, h=c$ (some constant)



#Physics #Energy #Definition