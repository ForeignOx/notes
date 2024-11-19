The generic first order [[Differential Equations|ODE]] can be written in the form:
$$
\frac{d y}{dx} =f(x,y)
$$
Generically this has a one parameter family of solutions; the general solution, which will always contain a single arbitrary constant. Assigning a particular value to this constant gives the particular solution requireing that the solution satisfies an initial condition $y(x_{0})=y_{0}$ for fixed $y_{0}$ will fix a specific solution to the ODE. In this case, the ODE is called an initial value problem (IVP). To solve an IVP, one should first find the general solution to the ODE and then use the initial condition (initial value) to find the specific solution which satisfies the IVP
The method used to solve the ODE depends on the form of $f(x,y)$ (most cannot be solved)
## First Order Separable ODEs
The ODE $\frac{d y}{dx}=f(x,y)$ is separable is $f(x,y)=X(x)Y(y)$, and can be solved by direct integration:
$$
\frac{1}{Y(y)}\frac{d y}{dx} =X(x)\iff \int \frac{1}{Y(y)} \, dy =\int X(x) \, dx 
$$
Which we can check by differentiating both sides with respect to $x$:
$$
    \frac{d }{dx} \int \frac{1}{Y(y)} \, dy =\frac{d }{dx} \int X(x) \, dx 
$$
Then using the chain rule for the LHS
### Example
Solve the IVP $\frac{d y}{dx}=xe^{ y-x }$ with $y(0)=0$
$$
y'=xe^{ y }e^{ -x }
$$
$$
\implies \int e^{ -y } \, dy =\int xe^{ -x } \, dx 
$$
$$
\implies -e^{ -y }=-xe^{ -x }+\int e^{ -x } \, dx
$$
By [[Leibniz Rule|Leibniz rule]]
$$
e^{ -y }=-xe^{ -x }-e^{ -x }+c
$$
$$
\implies e^{ -y }=e^{ -x }(1+x)-c
$$
$$
\implies y=-\ln(e^{ -x }(1+x)-c)
$$
Which is the general solution, now using the initial condition $y(0)=0$, 
$$
y(0)=-\ln(1-c)=0
$$
$$
\implies c=0
$$
So the particular solution is:
$$
y=-\ln(e^{ -x }(1+x))=x-\ln(1+x)
$$
___
Solve:
$$
y'=\frac{x^{2}y-y}{1+y}=(x^{2}-1) \frac{y}{1+y}
$$
$$
\implies \int \frac{1+y}{y} \, dy= \int x^{2}-1 \, dx 
$$
$$
\implies y+\ln|y|=x^{3}-x+c
$$
Which is the general solution to the ODE in implicit form
## First Order Homogeneous ODEs
The ODE is homogeneous if in $\frac{d y}{dx}=f(x,y)$, the $f(x,y)=f(tx,ty)\forall t\in\mathbb{R}$
In this case, the substitution $y=xv(x)$ which gives a seqarable ODE for $v(x)$
