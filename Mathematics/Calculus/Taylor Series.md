## 1D Taylor Series
### First Order Taylor
If you have a function $f:X\to \mathbb{C}$ and $f$ is differentiable at $c$, then there exists a constant $m\in\mathbb{R}$ and a function $r(x)$ such that
$$
f(x)=f(c)+m(x-c)+r(x)(x-c)
$$
Such that $r(x)$ is [[Continuity|continuous]] at $c$ and $\lim_{ x \to c }r(x)=r(c)=0$. In this case, $m=f'(c)$
#### Remarks
- Continuity in this context is "Taylor order 0" i.e. $f(x)=f(c)+\tilde{r}(x)$ with $\lim_{ x \to c }\tilde{r}(x)=\tilde{r}(c)=0$
- We can view differentiability as the attempt to approximate $f(x)$ in a neighbourhood of $c$ by a linear function $L(x)=f(c)+m(x-c)$. Then differentiability stipulates that the error $r(x)(x-c)$ is of "higher order" as $\lim_{ x \to c }r(x)=0$, so differentiability is "Taylor order 1"
- In practice one often considers $f_{1}(x)=m+r(x)$ which is continuous at $c$ with value $f_{1}(c)=m$. Thus differentiability at $c$ is equivalent to: there exists a function $f_{1}:X\to \mathbb{R}$ such that
$$
f(x)=f(c)+(x-c)f_{1}(x)
$$
    And $f_{1}$ is continuous at $c$. Then $\lim_{ x \to c }f_{1}(x)=f_{1}(c)=f'(c)$. This is useful as you don't need to know the value of the derivative in advance
#### Proof
Set $m=f'(c)$ and 
$$
r(x)=\begin{cases}
\frac{f(x)-f(c)-m(x-c)}{x-c}&x\neq c\\0&x=c
\end{cases}
$$
Then we only need to check whether $r(x)$ is continuous at $c$, so
$$
\lim_{ x \to c } r(x)=\lim_{ x \to c } \frac{f(x)-(f(c)+m(x-c))}{x-c}=\lim_{ x \to c } \frac{f(x)-f(c)}{x-c}-m=m-m=0
$$
As required
Conversely, if $r$ is continuous at $c$ and $r(c)=0$, then
$$
0=r(c)=\lim_{ x \to c } r(x)=\lim_{ x \to c }  \frac{f(x)-(f(c)+m(x-c))}{x-c}=\lim_{ x \to c } \left(  \frac{f(x)-f(c)}{x-c}-m  \right)
$$
This limit is only possible if $\lim_{ x \to c } \frac{f(x)-f(c)}{x-c}$ exists and is equal to $m$
### Taylor's Theorem
Taylor's theorem states that if [[Functions|$f$]] has $n+1$ continuous [[Differentiation|derivatives]] in an open [[Intervals|interval]] $I$, containing the point $x=a$, then $\forall x\in I$:
$$
f(x)=\sum_{ k=0} ^{ n}  \frac{f^{(k)}(a)}{k!}(x-a)^{k}+R_{n}(x)
$$
With
$$
R_{n}(x)=\frac{1}{n!}\int _{a}^{x}(x-t)^{n}f^{(n+1)}(t) \, dt 
$$
Called the remainder
#### Proof
Fix $x\in I$, then consider:
$$
\int _{a}^{x}f'(t) \, dt =f(x)-f(a)
$$
By the [[Fundamental Theorem of Calculus|Fundamental Theorem of Calculus]], therefore:
$$
f(x)=f(a)+\int _{a}^{x}f'(t) \, dt 
$$
We now use the following form of [[Integration by Parts|integration by parts]]; let $g(t),h(t)$ be [[Integration|integrable]] on an interval $(a,b)$, and let $G(t),H(t)$ be indefinite integrals of $g(t)$ and $h(t)$ respectively, then:
$$
(GH)'=G'H+H'G=gH+hG
$$
and integrating both sides over $(a,b)$ and rearranging for integration by parts,
$$
\int ^{b}_{a} g(t)H(t) \, dt =[G(t)H(t)]_{a}^{b}-\int ^{b}_{a} h(t)G(t) \, dt 
$$
    Applying htis over $(a,x)$ with $G(t)=t-x$ such that applying this over $(a,x)$ such that $g(t)=1$, and $H(t)=f'(t)$ such that $h(t)=f''(t)$
    $$
\int ^{x}_{a} f'(t) \, dt =[(t-x)f'(t)]_{a}^{x}-\int ^{x}_{a}  f''(t)(t-x) \, dx =(x-a)f'(a)(x-a)+\int _{a}^{x}f''(t)(x-t) \, dt 
$$
Which is the claimed result when $n=1$, for $n=2$, we integrate by parts again and you can show it is true by [[Proof by Mathematical Induction!!!!!|induction]] 
### Taylor Polynomials
The combination $P_{n}(x)=f(x)-R_{n}(x)$ is a polynomial in $x$ of degree $n$ called the $n$th order Taylor polynomial of $f$ about $x=a$:
$$
P_{n}(x)=f(a)+f'(a)(x-a)+\frac{f''(a)}{2}(x-a)^{2}+\dots+\frac{f^{(n)}(a)}{n!}(x-a)^{n}
$$
If the term about $x=a$ is omitted, then we take this to mean about $x=0$
The Taylor polynomial $P_{n}(x)$ is an approximation to $f(x)$. Generally it is a good approximation when sufficiently close to $a$ and the approximation improves as $n$ increases. The remainder $R_{n}(x)$ gives an exact expression for the error
If $f(x)$ is infinitely differentiable (smooth) on an open interval $I$ that contains the point $x=a$, and if in addition for each $x\in I$ we have $\lim_{ n \to \infty }R_{n}(x)=0$ , then we say $f(x)$ can be expanded as a Taylor series about $x=a$:
$$
f(x)=\sum_{ k=0} ^{\infty}  \frac{f^{(k)}(a)}{k!}(x-a)^{k}
$$
Note that the $n$th order Taylor polynomial $P_{n}(x)$ is obtained by taking the first $n+1$ terms of the Taylor series (counting terms even if they're zero)
### Examples
I can do these, but can't be bothered rn:
$$
e^{x}=\sum_{ k=0} ^{\infty}  \frac{1}{k!}
$$
$$
\sin(x)=\sum_{ k=0} ^{\infty}  \frac{(-1)^{k}}{(2k+1)!}x^{2k+1}
$$
$$
\cos(x)=\sum_{ k=0} ^{\infty}  \frac{(-1)^{k}}{(2k)!}x^{2k}
$$
We can calculate the Taylor series of $\sinh x=f(x)$ by noting that for any non-negative integer $k$, the $k$th derivative of $\sinh$ is $\sinh$ if $k$ is even, and is $\cosh$ if $k$ is odd, and then the same sort of thing for $\cosh$, and so for $\sinh$, $f^{(2k)}(0)=0,f^{(2k+1)}(0)=1$, so
$$
\sinh (x)=\sum_{ k=0} ^{\infty} \frac{1}{(2k+1)!}x^{2k+1}
$$
$$
\cosh(x)=\sum_{ k=0} ^{\infty}  \frac{1}{(2k)!}x^{2k}
$$
This also follows directly from the Taylor series of the exponential since $\cosh$ is the [[Even Functions|even]] part and $\sinh$ is the [[Odd Functions|odd]] part of $e^{ x }$. Note that this works for any odd and even function combination
Since $\ln (x)$ is not defined at $x=0$, it doesn't make sense at $x=0$, so instead, we usually consider the Taylor series about $x=1$
$$
f(x)=\ln x,f(1)=0

$$
$$
 f'(x)=\frac{1}{x},f'(1)=1
$$
$$
 f''(x)=-\frac{1}{x^{2}},f''(1)=-1

$$
$$
 f'''(x)=\frac{2}{x^{3}},f'''(1)=2
$$
$$
 f^{(4)}(1)=-6
$$
We see that for $k>0$, 
$$
f^{(k)}(x)=(-1)^{k-1} \frac{(k-1)!}{x^{k}},f^{(k)}(1)=(-1)^{k}(k-1)!
$$
Hence 
$$
\ln (x)=\sum_{ k=1} ^{\infty}  \frac{(-1)^{k-1}(k-1)!}{k!}-\sum_{ k=1} ^{\infty}  \frac{(-1)^{k-1}}{k}(x-1)^{k}
$$
It is common to change variables with $y=x-1$ such that
$$
\ln(y+1)=\sum_{ k=1} ^{\infty}  \frac{(-1)^{k}}{k}x^{k}
$$
One can show that in order for $\lim_{ n \to \infty }R_{n}(x)=0$ we must have $-1\leq x\leq 1$. So this Taylor series for $\ln(1+x)$ is vali only for $-1\leq x\leq 1$ (otherwise it doesn't converge)
### Lagrange Form of the Remainder
There is a more convenient expression for the remainder term in Taylor's theorem. The Lagrange form of the remainder is:
$$
R_{n}(x)=\frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}
$$
For some $c \in(a,x)$
#### Lemma
Let $h(t)$ be differentiable $n+1$ times on $[a,x]$, with $h^{(k)}(a)=0$ for some $0\leq k\leq n$ and $h(x)=0$ then $\exists c_{1}\in(a,x):h'(c)=0$
Then since $h'(a)=h'(c_{1})=0,\exists c_{2}\in(a,c_{1}):h''(c_{2})=0$. Applying this arguments a total of $n$ times we get:
$$
h^{(n)}(a)=h^{(n)}(c_{n})=0,\exists c_{n+1}\in (a,c_{n}):h^{(n+1)}(c_{n})=0
$$
#### Proof
We use a similar idea to the proof of the [[Mean Value Theorem|mean value theorem]]
Consider 
$$
h(t)=(f(t)-P_{n}(t))(x-a)^{n+1}-(f(x)-P_{n}(x))(t-a)^{n+1}
$$
We have $h(x)=0$
Since 
$$
P_{n}(t)=f(a)+f'(a)(t-a)+\frac{f''(a)}{2}(t-a)^{2}+\dots+\frac{f^{(n)}(a)}{n!}(t-a)^{n}
$$
Then $P_{n}(a)=f(a)$, $P_{n}'(a)=f'(a)$ ad more generally, since
$$
\frac{d^{k}}{dt^{k}} (t-a)^{n+1}|_{t=a}=0
$$
For $0\leq k\leq n$ and 
$$
\frac{d ^{n+1}}{dt^{n+1}} (t-a)^{n+1}|_{t=a}=(n+1)!
$$
So in general, 
$$
P_{n}^{(k)}(a)=f^{(k)}(a)
$$
Then $h^{(k)}(a)=0$ for $0\leq k\leq n$ and hence by the previous Lemma, there exists a $c\in(a,x):h^{(n+1)}(c)=0$ 
$P_{n}^{(n+1)}(t)=0$, since $P_{n}(t)$ is degree $n$, and
$$
\frac{d^{n+1}}{dt^{n+1}} (t-a)^{n+1}=(n+1)!
$$
Hence $0=h^{(n+1)}(c)=f^{(n+1)}(c)(x-a)^{n+1}-(f(x)-P_{n})(x)(n+1)!$ and by rearranging:
$$
f(x)=P_{n}(x)+ \frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}
$$
___
The Lagrange form of the remainder is useful for putting a bound on the error of a Taylor polynomial approximation to a function. Suppose,
$$
|f^{(n+1)}(t)|\leq M\forall t\in [a,x]
$$
Then
$$
\left| R_{n}(x) \right|\leq M \frac{\left| x-a \right| ^{n+1}}{(n+1)!} 
$$
Which provides a bound on the error
#### Example
Show that the error in approximating $e^{ x }$ by its 6th order Taylor polynomial is less than $0.0006$ throughout the interval $[0,1]$
We have $f(x)=e^{ x }$ and $a=0$, and we wnat a bound on $|R_{6}(t)|$ for $t\in[0,1]$. Then $\left| f^{(7)}(t) \right|=\left| e^{t} \right|$, since $e^{ t }$ is monotonic increasing and positive, $e^{ t }=e^{ t }\leq e^{ 1 }<3$, so take $M=3$
Then
$$
\left| R_{6}(x) \right| \leq \frac{3\left| x \right| ^{7}}{7!}\leq \frac{3}{7!}
$$
Since $\frac{3}{7!}<0.0006$, and so we have the required result
### [[Limit|Limits]] using Taylor Series
If we knwo a Taylor series is valid on some suitable open interval, then it may be useful for calculating certain limits
One can show that the Taylor Series for $\sin$ and $\cos$ are valid $\forall x\in\mathbb{R}$
#### Example
Use Taylor series to calculate $\lim_{ x \to 0 } \frac{\sin x}{x}$
From the Taylor series:
$$
\sin x=x-\frac{x^{3}}{3!}+\frac{x^{5}}{5!}-\dots=x+o(x^{2})
$$
(using [[o Notation|o notation]])
Hence 
$$
\lim_{ x \to 0} \frac{\sin x}{x}=\lim_{ x \to 0 } \frac{x+o(x^{2})}{x}=\lim_{ x \to 0 }(1+o(x))=1 
$$
___
Use Taylor series to calculate $\lim_{ x \to 0 } \frac{1-\cos x}{x}$
From the Taylor series:
$$
\cos x=1-\frac{x^{2}}{2}+\frac{x^{4}}{4!}-\dots=1-\frac{x^{2}}{2}+o(x^{3})
$$
Hence
$$
\lim_{ x \to 0 } \frac{1-\cos x}{x}=\lim_{ x \to 0 } \left( \frac{1-\left( 1-\frac{x^{2}}{2}+o(x^{3}) \right)}{x} \right)=\lim_{ x \to 0 } \left( \frac{x}{2}+o(x^{2}) \right)=0
$$
## 2D Taylor Series
In $2D$ we want to know $f(x_{0}+\delta x,y_{0}+\delta y)$ in terms of $f(x_{0},y_{0})$ and derivatives of $f$ at $(x_{0},y_{0})$. Construct
$$
F(t)=f(x_{0}+t\delta x,y_{0}+t\delta y)
$$
![[Taylor Series 2025-01-28 14.43.15.excalidraw]]
We can use the 1D taylor series in terms of $t$ about $t=0$ to get:
$$
F(t)=F(0)+tF'(0)+\frac{t^{2}}{2!}F''(0)+\dots+\frac{t^{n}F^{(n)}}{n!}+\frac{t^{n+1}F^{(n+1)}(\xi)}{n!}
$$
For $0<\xi<t$. We use the [[Chain Rule|chain rule]] to calculate the derivatives, for example:
$$
\frac{d F}{dt} =\frac{d }{dt} (f(x_{0}+\delta x,y_{0}+\delta y))=\frac{ \partial f }{ \partial x } \frac{ \partial x }{ \partial t } +\frac{ \partial f }{ \partial y } \frac{ \partial y }{ \partial t } =\delta x\frac{d f}{dx} +\delta y\frac{ \partial f }{ \partial y } 
$$
And in fact, bby repeated use of chain rule,
$$
F^{(n)}(t)=\frac{d ^{n}F}{dt^{n}} =\left( \delta x\frac{ \partial  }{ \partial x } +\delta y \frac{ \partial  }{ \partial y } \right)^{n}f
$$
Then using [[Binomial Theorem|binomial theorem]],
$$
=\sum_{i=0}^{n}\left( \delta x\frac{ \partial  }{ \partial x }  \right)^{i}\left( \delta y\frac{ \partial  }{ \partial y }  \right)^{n-i}{n \choose i }f
$$
$$
= \sum_{i=0}^{n}(\delta x)^{i}(\delta y)^{n-i}{n \choose i }f_{\underbrace{ x\dots x }_{ i } \underbrace{ y\dots y }_{ n-i }}
$$
So for example
$$
\frac{d ^{2}F}{dt^{2}} =\left( \delta x\frac{ \partial  }{ \partial x } +\delta y \frac{ \partial  }{ \partial y } \right)^{2}=(\delta x)^{2}f_{xx}+2(\delta x)(\delta y)f_{xy}+(\delta y)^{2}f_{yy}
$$
So                         
___
### Example
Find the Taylor series of $f(x,y)=x+\sin(x+y)$ around the point $(x_{0},y_{0})=\left( \frac{\pi}{2},0 \right)$ to quadratic order
$$
f(x_{0},y_{0})=f\left( \frac{\pi}{2},0 \right)=\frac{\pi}{2}+\sin\left( \frac{\pi}{2}+0 \right)=\frac{\pi}{2}+1
$$
$$
f_{x}=1+\cos(x+y)=1+0=1
$$
$$
 f_{y}=\cos(x+y)=0
$$
$$
 f_{xx}=-\sin(x+y)=-1
$$
$$
 f_{xy}=-\sin(x+y)=-1
$$
$$
 f_{yy}=-\sin(x+y)=-1 
$$
So
$$
f(x,y)=1+\frac{\pi}{2}+\left( x-\frac{\pi}{2} \right)+\frac{1}{2}\left( -\left( x-\frac{\pi}{2} \right)^{2}-2\left( x-\frac{\pi}{2} \right)y-y^{2} \right)+\dots 
$$


#Mathematics #Calculus #Theorem 