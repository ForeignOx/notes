## Linear Constant-Coefficient ODEs
### Homogeneous

For a 2nd order, linear homogeneous ODE with constant coefficients:
$$
a \frac{d^{2}y}{dx^{2}}+b \frac{dy}{dx}+cy=0
$$
Consider a solution of the form:
$$
y=e^{\lambda x}
$$
$$
\implies \frac{dy}{dx}=\lambda e^{\lambda x}
$$
$$
\implies \frac{d^{2}y}{dx^{2}}=\lambda^{2}e^{\lambda x}
$$
Substitute these back into the original equation
$$
a(\lambda^{2}e^{\lambda x} )+b(\lambda e^{\lambda x})+c(e^{\lambda x})=0
$$
$$
\implies e^{\lambda x}(a\lambda^{2}+b\lambda+c)=0
$$
So we get the auxiliary equation:
$$
a\lambda^{2}+b\lambda+c=0
$$
With solutions: $\lambda=\alpha$ and $\lambda=\beta$
$\therefore$ the general solution is the sum of these:
$$
y=Ae^{\alpha x}+Be^{\beta x}
$$
The particular solution can be found using initial conditions
### Repeated Roots
If $\alpha=\beta$, the general solution will instead be:
$$
y=(A+Bx)e^{\alpha x}
$$
Note that in this case the product rule will be needed to find the particular solution
We know this as $y_{2}=xe^{ \lambda x }$ is also a solution to $y_{1}=e^{ \lambda x }$, since:
$$
0=ay''+by+c
$$
Which one can rewrite as:
$$
0=a(y''-2\lambda y'+\lambda^{2}y)
$$
Since there is a repeated root
We have:
$$
y_{2}'=e^{ \lambda x }+\lambda e^{ \lambda x }
$$
$$
y_{2}''=\lambda e^{ \lambda x }+\lambda e^{ \lambda x }+\lambda^{2}xe^{ \lambda x }=2\lambda e^{ \lambda x }+\lambda^{2}xe^{ \lambda x }
$$
So:
$$
y_{2}''-2\lambda y_{2}'+\lambda^{2}y_{2}=(2\lambda e^{ \lambda x }+\lambda xe^{ \lambda x })-2\lambda(e^{ \lambda x }+\lambda e^{ \lambda x })+\lambda^{2}(xe^{ \lambda x })=0
$$
So $y_{2}$ is a second independent solution, as required
### Complex Roots
If $\alpha,\beta \in \mathbb{C}$, $\alpha=\beta ^{*}$, ie. $\alpha=a+bi$, $\beta=a-bi$ and the general solution will be:
$$
y=Ae^{(a+bi)x}+Be^{(a-bi)x}=e^{a}(Ae^{bix}+Be^{-bix})
$$
$$
=e^{a}(A(\cos bx+i\sin bx)+B(\cos bx-i\sin bx))
$$
$$
=e^{a}((A+B)\cos bx+(A-B)i\sin bx)
$$
Which can be rewritten as:
$$
y=e^{a}(P\cos bx+Q\sin bx)
$$
Which is the new general solution which can then be rewritten in harmonic form:
$$
y=e^{a}R\cos(bx-\theta)
$$
Where $R=\sqrt{ P^{2}+Q^{2} }$ and $\theta=\arctan\left( \frac{Q}{P} \right)$
### Non-Homogeneous
For a 2nd order, linear non-homogeneous ODE with constant coefficients:
$$
a \frac{d^{2}y}{dx^{2}}+b \frac{dy}{dx}+cy=\phi(x)
$$
#### General Form
If $y=y_{1}$ is a solution to:
$$
ay''+by'+cy=f(x)
$$
and $y=y_{2}$ is a solution to:
$$
ay''+by'+cy=0
$$
Then let 
$$
y=y_{1}+y_{2}
$$
$$
\implies y'=y_{1}'+y_{2}'
$$
$$
\implies y''=y_{1}''+y_{2}''
$$
$$
\implies a(y_{1}''+y_{2}'')+b(y_{1}'+y_{2}')+c(y_{1}+y_{2})
$$
$$
=(ay_{1}''+by_{1}'+cy_{1})+(ay_{2}''+by_{2}'+cy_{2})
$$
$$
=f(x)+0=f(x)
$$
So our general solution can be in the form $y=y_{1}+y_{2}$
#### Complimentary Function
This is $y_{2}$ from above, always do this first, this is the same as with homogeneous:
$$
y=Ae^{\alpha x}+Be^{\beta x}
$$
#### Particular Integral
We need to find a particular integral to satisfy the ODE
When $\phi(x)$ ha s the form of a polynomial, exponential or $\sin$ or $\cos$ function, or a sum or product of these, we can apply the method of undetermined coefficients
To apply this method, we try a $y_{PI}$ of a particular form based on the form of $\phi$ containing some unknown constant coefficients. We then determine these coeffifiences such that $y_{PI}$ solves the original equation
The following table lists terms that can appear in $\phi$ in order to use this method, and the corresponding form to try for $y_{PI}$

| Term in $\phi(x)$ | Form to try for $y_{PI}$                   |
| ----------------- | ------------------------------------------ |
| $e^{ \gamma x }$  | $a_{1}e^{ \gamma x }$                      |
| $x^{n}$           | $a_{0}+a_{1}x+a_{2}x^{2}+\dots+a_{n}x^{n}$ |
| $\cos(\gamma x)$  | $a_{1}\cos(\gamma x)+a_{2}\sin(\gamma x)$  |
| $\sin(\gamma x)$  | $a_{1}\cos(\gamma x)+a_{2}\sin(\gamma x)$  |
If $\phi(x)$ contains sums or products of the above terms,, we try the corresponding sum/product of the corresponding forms
If the listed form to try is already in the complimentary function, then putting this into the original ODE will give $0$ rather than $\phi(x)$, we then try a $y_{PI}$ of the suggested form multiplied by $x$. We can apply this rule twice (or more times) if the first applicatio also gives a terms in $y_{CF}$

#Mathematics #Calculus