## Systems of 1st Order Linear ODEs
A system of $n$ coupled [[First Order Ordinary Differential Equations|1st order linear ODEs]] for $n$ dependent variables can be re-written as a single $n$th order linear ODE for a single dependent variable by eliminating the other dependent variables
An associated IVP is obtained if all the values of the dependent variables are specified at a single value of the independent variable
Note this process can be used to convert an $n$th order ODE as a set of $n$ first order linear ODEs, which can be solved with linear algebra :)
### Example
Find the solution $y(x),z(x)$ of the pair of 1st order linear ODEs
$$
y'=y-2z+2x
$$
$$
 z'=3y-4z+2x
$$
Satisfying the initial conditions $y(0)=1,z(0)=2$
We rewrite the system of two coupled first order ODEs as a [[Second Order Differential Equations|second order ODE]] for $y$ or $z$, which we can solve
From the first equation;
$$
z=-\frac{y'}{2}+\frac{y}{2}+x
$$
$$
\implies z'=-\frac{y''}{2}+\frac{y'}{2}+1
$$
Then we can substitute these expressions for $z$ and $z'$ into the second equation:
$$
-\frac{y''}{2}+\frac{y'}{2}+1=3y-4\left( -\frac{y'}{2}+\frac{y}{2}+x \right)+2x
$$
Which can be rearranged and solved
