Legendre's Equation is a [[Second Order Ordinary Differential Equations|second order]] [[Linear Ordinary Differential Equations|linear ordinary]] [[Differential Equations|differential equation]] of the form:
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
___
We can rewrite Legendre's equation using a [[Linear Differential Operators|linear differential operator]]:
$$
(1-x^{2})\frac{d ^{2}y}{dx^{2}} -2x\frac{d y}{dx} +\lambda y=0
$$
As
$$
\underbrace{ \left[ (x^{2}-1)\frac{d ^{2}}{dx^{2}} +2x\frac{d }{dx}  \right] }_{  =\mathcal{L}_{L}}y=\lambda y
$$
Since we can think of $\mathcal{L}_{L}$ as a matrix, we can write it as:
$$
\mathcal{L}_{L}y=\lambda y
$$
Which looks a lot like the form of 
$$
M\underline{v}=\lambda \underline{v}
$$
Which reminds us of [[Eigenvalues|eigenvalues]], so we in fact call $y$ that satisfies this an eigenfunction, and again $\lambda$ is the eigenvalue
If we consider a Legendre polynomial $p_{m}(x)$ of order $m$ satisfies the equation for $\lambda=m(m+1)$:
$$
\mathcal{L}_{L}p_{m}(x)=m(m+1)p_{m}(x)
$$
So $p_{m}(x)$ is an eigenfunction of $\mathcal{L}_{L}$ with eigenvalue $m(m+1)$
Infinite-dimensional vectorspaces are tricky things, so we make the analogy between differential operators and matrices precise by restricting, for example $y(x)\in\mathbb{R}[x]_{3}$, $y$ is a cubic polynomial. We can choose as our [[Basis|basis]] $1,x,x^{2},x^{3}$ so we can write:
$$
y(x)=a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}
$$
So $y(x)$ corresponds to the [[Vectors|vector]]:
$$
\begin{pmatrix}
a_{0}\\a_{1}\\a_{2}\\a_{3}
\end{pmatrix}
$$
Consider the action of $\mathcal{L}_{L}$ on the basis $x^{n}$ for $n=0,\dots,3$:
$$
\left[ (x^{2}-1)\frac{d ^{2}}{dx^{2}}+2x\frac{d }{dx}   \right]x^{n}=(x^{2}-1)n(n-1)x^{n-2}+2xnx^{n-1}
$$
$$
= n(n-1)x^{n}-n(n-1)x^{n-2}+2nx^{n}
$$
$$
\mathcal{L}_{L}x^{n}=n(n+1)x^{n}-n(n-1)x^{n-2}
$$
So $\mathcal{L}_{L}$ never raises the power of $x$, so $\mathcal{L}_{L}$ acting on a cubic polynomial gives a cubic polynomial:
$$
\mathcal{L}_{L}:\mathbb{R}[x]_{3}\to \mathbb{R}[x]_{3}
$$
So we can represent it as the $4\times 4$ matrix $M_{L}$, we can now consider the actions on vectors to construc $M_{L}$:
$$
\mathcal{L}_{L}x^{0}=0
$$
$$
\implies M_{L}\begin{pmatrix}
1\\0\\0\\0
\end{pmatrix}=\begin{pmatrix}
0\\0\\0\\0
\end{pmatrix}
$$
$$
\mathcal{L}_{L}x^{1}=2x
$$
$$
\implies M_{L}\begin{pmatrix}
0\\1\\0\\0
\end{pmatrix}=\begin{pmatrix}
0\\2\\0\\0
\end{pmatrix}
$$
$$
\mathcal{L}_{L}x^{2}=6x^{2}-2
$$
$$
\implies M_{L}\begin{pmatrix}
0\\0\\1\\0
\end{pmatrix}=\begin{pmatrix}
-2\\0\\6\\0
\end{pmatrix}
$$
$$
\mathcal{L}_{L}x^{3}=12x^{3}-6x
$$
$$
\implies M_{L}\begin{pmatrix}
0\\0\\0\\1
\end{pmatrix}=\begin{pmatrix}
0\\-6\\0\\12
\end{pmatrix}
$$
So
$$
M_{L}=\begin{pmatrix}
0&0&-2&0\\0&2&0&-6\\0&0&6&0\\0&0&0&12
\end{pmatrix}
$$
$M_{L}$ is upper triangular (as it cannot raise the power of $x$), so it has eigenvalues $0,2,6,12$
We expect this as these are values of $m(m+1)$ for $m=0,1,2,3$
We have the first few Legendre polynomials as:
$$
p_{0}(x)=1,p_{1}(x)=x,p_{2}(x)=\frac{3x^{2}-1}{2},p_{3}(x)=\frac{5x^{3}-3x}{2}
$$
So for example $p_{2}(x)$ corresponds to:
$$
M_{L}\begin{pmatrix}
-\frac{1}{2}\\0\\ \frac{3}{2}\\0
\end{pmatrix}=\begin{pmatrix}
0&0&-2&0\\0&2&0&-6\\0&0&6&0\\0&0&0&12
\end{pmatrix}\begin{pmatrix}
-\frac{1}{2}\\0\\ \frac{3}{2}\\0
\end{pmatrix}=\begin{pmatrix}
-3\\0\\9\\0
\end{pmatrix}=6\begin{pmatrix}
-\frac{1}{2}\\0\\ \frac{3}{2}\\0
\end{pmatrix}
$$
Where $6=m(m+1)$ for $m=2$
$p_{m}$ are of order $m$ (differnt orders to each other), so they are [[Linear Independence|linearly independent]], so $p_{0},\dots p_{3}$ can forma  basis for $\mathbb{R}[x]_{3}$
So we can write $y\in\mathbb{R}[x]_{3}$ as
$$
y=\sum_{n=0}^{3}b_{n}p_{n}(x)
$$
$$
 y=a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}=b_{0}p_{0}(x)+b_{1}p_{1}(x)+b_{2}p_{2}(x)+b_{3}p_{3}(x)
$$
$$
= b_{0}+b_{1}x+b_{2}\left( \frac{3x^{2}}{2}-\frac{1}{2} \right)+b_{3}\left( \frac{5x^{3}}{2}-\frac{3x}{2} \right)
$$
So
$$
a_{0}=b_{0}-\frac{b_{2}}{2}
$$
$$
a_{1}=b_{1}-\frac{3b_{3}}{2}
$$
$$
 a_{2}=\frac{3b_{2}}{2}
$$
$$
 a_{3}=\frac{5b_{3}}{2}
$$
So
$$
\begin{pmatrix}
a_{0}\\a_{1}\\a_{2}\\a_{3}
\end{pmatrix}=N\begin{pmatrix}
b_{0}\\b_{1}\\b_{2}\\b_{3}
\end{pmatrix}=\begin{pmatrix}
1&0&-\frac{1}{2}&0\\0&1&0& -\frac{3}{2}\\0&0& \frac{3}{2}&0\\0&0&0& \frac{5}{2}
\end{pmatrix}\begin{pmatrix}
b_{0}\\b_{1}\\b_{2}\\b_{3}
\end{pmatrix}
$$
So in Legendre polynomial basis,
$$
\mathcal{L}_{L}y=\mathcal{L}_{L}\sum_{n=0}^{3}b_{n}p_{n}(x)=\sum_{n=0}^{3}b_{n}\mathcal{L}_{L}p_{n}(x)=\sum_{n=0}^{3}n(n+1)b_{n}p_{n}(x)
$$
So we can represent $\mathcal{L}_{L}$ as a [[Diagonalisation|diagonal]] matrix:
$$
\begin{pmatrix}
0&0&0&0\\0&2&0&0\\0&0&6&0\\0&0&0&12
\end{pmatrix}=N^{-1}M_{L}N
$$
This in fact works for any $n$th order polynomial:
- can represent $\mathcal{L}_{L}$ as a $n+1\times n+1$ matrix
- eigenvalues would be $m(m+1)$ for $m=0,\dots,n$
- eigenfunctions would correspond to $p_{m}(x)$ for $m=0,\dots,m$
- could write $y(x)\in\mathbb{R}[x]_{n}$ as $y(x)=\sum_{n=0}^{n}b_{n}p_{n}(x)$
- in this basis, $\mathcal{L}_{L}$ would be diagonal
In fact we can expand this to any suitable non-polynomial functions by considering [[Power Series|power series]] and write $y(x)=\sum_{n=0}^{\infty} b_{n}p_{n}(x)$

