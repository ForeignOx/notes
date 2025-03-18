Lots of quantities which depend on more than one variable evolve according to some PDE, such as the heat equation
Linear partial differential equations still follow the [[Principle of Superposition|principle of superposition]] since they are [[linear|linear]]; i.e. if $y_{1}$ and $y_{2}$ are solutions, then $\alpha y_{1}+\beta y_{2}$ is a solution, so the solution space is a [[Vectorspaces|vectorspace]], but in this case, infinite [[Dimension|dimensional]] (unlike with [[Linear Ordinary Differential Equations|linear ordinary differential equations]])

## Application of [[Fourier Transform|Fourier Transforms]]
Suppose we we have a PDE of $\hspace{0pt}2$ independent variables $x,t$, and $\hspace{0pt}1$ dependent variable $u(x,t)$, then
$$
\tilde{u}(p,t)=\int_{-\infty}^{\infty} u(x,t)e^{ -ipx } \, dx 
$$
Then the fourier transform $u_{x}(x,t)$ is $ip\tilde{u}(p,t)$
The fourier transform of $u_{t}(x,t)$ is:
$$
u_{t}(x,t)=\int_{-\infty}^{\infty} u_{t}(x,t)e^{ ipx } \, dx =\frac{ \partial  }{ \partial t } \left( \int_{-\infty}^{\infty} u(x,t)e^{ -ipx } \, dx  \right)=\frac{ \partial  }{ \partial t } \tilde{u}(p,t)
$$
If the PDE has only $\partial_{x},\partial_{t}$ in it, after fourier transforming to $ip,\frac{ \partial  }{ \partial t }$, the PDE becomes an ODE which we can solve!
### Example
Find $u(x,t)$ for $t>0$ if $u_{t}=3u_{x}-5u$ and $u(x,0)=R(x)=\text{sech}(x)$:
We take the Fourier Transform:
$$
\int_{-\infty}^{\infty} u_{t}e^{ -ipx } \, dx =\int_{-\infty}^{\infty} (3u_{x}-5u)e^{ -ipx } \, dx 
$$
$$
\implies \tilde{u}_{t}=3ip \underline{u}-5\underline{u}=(3ip-5)\underline{u}
$$
So we have solution
$$
\tilde{u}(p,t)=A(p)e^{ (3ip-5)t }
$$
$$
\tilde{u}(p,0)=A(p)=\int_{-\infty}^{\infty} u(x,0)e^{ -ipx } \, dx=\int_{-\infty}^{\infty} R(x)e^{ -ipx } \, dx =\tilde{R}(p)
$$
$$
\implies \tilde{u}(p,t)=\tilde{R}(p)e^{ 3ipt }e^{ -5t }
$$
Now we need to think what function do we have that has this Fourier Transform. We know by shift theorem that the Fourier Transform of $f(x+a)$ is $\tilde{f}(p)e^{ ipa }$, so the fourier transform of $R(x+3t)$ is $\tilde{R}(p)e^{ 3ipt }$, so
$$
u(x,t)=e^{ -5t }R(x+3t)=e^{ -5t }\text{sech}(x+3t)
$$
Which is like a bump of $\text{sech}$, which moves with velocity $-3$ and scales with $e^{ -5t }$:
![[Linear Partial Differential Equations 2025-03-18 14.19.34.excalidraw]]
