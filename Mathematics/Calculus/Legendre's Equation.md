Legendre's Equation is a [[Second Order Differential Equations|second order]] [[Linear Ordinary Differential Equations|linear ordinary]] [[Differential Equations|differential equation]] of the form:
$$
(1-x^{2})\frac{d ^{2}y}{dx^{2}} -2x\frac{d y}{dx} +\lambda y=0
$$
We can convert this to canonical form:
$$
\frac{d ^{2}y}{dx^{2}} +\frac{2x}{x^{2}-1}\frac{d y}{dx} -\frac{\lambda}{x^{2}-1}y=0
$$
So $p(x)=\frac{2x}{x^{2}-1}$, $q(x)=-\frac{\lambda}{x^{2}-1}$, these are rational [[functions|functions]] [[Analytic Functions|analytic]] everywhere except when $x^{2}-1=0\implies x=\pm 1$, so all points $x_{0}\in\mathbb{R}$ are [[Regular Points|regular points]], except $x_{0}=\pm 1$, which are singular
Take $x_{0}=0$, we form a [[Power Series|power series]]
$$
y(x)=\sum_{n=0}^{\infty} a_{n}x^{n} 
$$
And substitute it into Legendre's Equation:
$$
(1-x^{2})\sum_{n=0}^{\infty} a_{n}n(n-1)x^{n-2}-2x\sum_{n=0}^{\infty} a_{n}nx^{n-1}+\lambda \sum_{n=0}^{\infty} a_{n}x^{n}=0
$$
$$
\implies \sum_{ n=0} ^{\infty}  a_{n}n(n-1)x^{n-2}-\sum_{n=0}^{\infty} a_{n}n(n-1)x^{n}-\sum_{n=0}^{\infty} 2a_{n}nx^{n}+\sum_{n=0}^{\infty} \lambda a_{n}x^{n}=0      
$$
We relable $n\to n+2$ in the first term:
$$
\implies\sum_{n=0}^{\infty} a_{n}(n+2)(n+1)x^{n} -\sum_{n=0}^{\infty} a_{n} x^{n}(n(n+1)-\lambda)=0
$$
$$
\implies \sum_{n=0}^{\infty} (a_{n+2}(n+2)(n+1)-a_{n}(n(n+1)-\lambda))x^{n}=0
$$
Which gives us the [[Recurrence Relations|recurrence relation]]:
$$
a_{n+2}=\frac{a_{n}(n(n+1)-\lambda)}{(n+2)(n+1)}
$$
Since $a_{n+2}$ relates to $a_{n}$, all our even indices relate to $a_{0}$, all our odd indices are related to $a_{1}$:
$$
a_{2}=\frac{a_{0}(-\lambda)}{1\times 2}=-\frac{\lambda}{2}a_{0}
$$
$$
 a_{4}=\frac{a_{1}(6-\lambda)}{3\times 4}=-\frac{\lambda(6-\lambda)}{4!}a_{0}
$$
$$
a_{3}=\frac{a_{1}(2-\lambda)}{2\times 3}=\frac{2-\lambda}{3!}a_{1}
$$
$$
 a_{5}=\frac{a_{3}(12-\lambda)}{4\times 5}=\frac{(2-\lambda)(12-\lambda)}{5!}a_{1}
$$
So 
$$
y(x)=\sum_{n=0}^{\infty} a_{n}x^{n}=a_{0}+a_{1}x+x_{2}x^{2}+a_{3}x^{3}+\dots 
$$
$$
= (a_{0}+a_{2}x^{2}+a_{4}x^{4}+\dots)+(a_{1}x+a_{3}x^{3}+a_{5}x^{5}+\dots)
$$
$$
= a_{0}\left( 1-\frac{\lambda}{2}x^{2}-\frac{\lambda(6-\lambda)}{4!}x^{4}+\dots \right)+a_{1}\left( x+\frac{2-\lambda}{3!}x^{3}+\frac{(2-\lambda)(12-\lambda)}{5!}x^{5}+\dots \right) 
$$
$$
= a_{0}y_\text{even}(x)+a_{1}y_\text{odd}(x)
$$
Which is an example of a linear combination of two Legendre Functions, $y_\text{even}$ and $y_\text{odd}$. These functions look a bit like:
![[Pasted image 20250213143515.png]]
In general they do not converge at $x=\pm 1$, the singular points
We can test this using the [[Ratio Test|ratio test]], the neighbouting terms in the odd/even series were $a_{n}x^{n},a_{n+2}x^{n+2}$, so
$$
\lim_{ n \to \infty } \left|  \frac{a_{n+2}x^{n+2}}{a_{n}x^{n}} \right| =\lim_{ n \to \infty } \left| \frac{n(n+1)-\lambda}{(n+1)(n+2)} \right| x^{2}=x^{2}
$$
Which will converge if $x<1$, diverge if $x>1$
Suppose $\lambda=m(m+1)$ where $m$ is a non-negative integer
We get a recurrence relation for $n=m$:
$$
a_{m+2}=a_{m}\left(  \frac{m(m+1)-\lambda}{(m+1)(m+2)} \right)=0
$$
$$
a_{m+2}=a_{m+2}(\text{stuff})=0
$$
So in this case $a_{m+2},a_{m+4},a_{m+6},\dots$ vanish
For $m$ even, $y_\text{even}(x)$ will be an $m$th order polynomial, for $m$ odd $y_\text{odd}$ will be an $m$th order polynomial.
These are known as Legendre Polynomials which are examples of [[Orthogonality|orthogonal]] polynomials

| $m$             | $\lambda=m(m+1)$ | $y_\text{even}(x)$ | $y_\text{odd}(x)$   | $p_{m}(x)$ |
| --------------- | ---------------- | ------------------ | ------------------- | ---------- |
| $\hspace{0pt}0$ | 0                | 1                  | $\sim\sim\sim$      |            |
| $\hspace{0pt}1$ | 2                | $\sim\sim\sim$     | $x$                 |            |
| 2               | 6                | $1-3x^{2}$         | $\sim\sim\sim$      |            |
| 3               | 12               | $\sim\sim\sim$     | $x-\frac{5}{3}^{3}$ |            |
| 4               | 20               |                    | $\sim\sim\sim$      | ``         |

