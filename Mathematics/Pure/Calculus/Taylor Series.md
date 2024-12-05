## Taylor's Theorem
Taylor's theorem states that if [[Functions|$f$]] has $n+1$ continuous [[Differentiation|derivatives]] in an open [[Intervals|interval]] $I$, containing the point $x=a$, then $\forall x\in I$:
$$
f(x)=\sum_{ k=0} ^{ n}  \frac{f^{(k)}(a)}{k!}(x-a)^{k}+R_{n}(x)
$$
With
$$
R_{n}(x)=\frac{1}{n!}\int _{a}^{x}(x-t)^{n}f^{(n+1)}(t) \, dt 
$$
Called the remainder
### Proof
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
## Taylor Polynomials
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
## Examples
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
This also follows directly from the Taylor series of the exponential since $\cosh$ is the [[Even Functions]] part and $\sinh$ is the [[Odd Functions|odd]] part of $e^{ x }$. Note that this works for any odd and even function combination
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
## Lagrange Form of the Remainder
There is a more convenient expression for the remainder term in Taylor's theorem. The Lagrange form of the remainder is:
$$
R_{n}(x)=\frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}
$$
For some $c \in(a,x)$
### Lemma
Let $h(t)$ be differentiable $n+1$ times on $[a,x]$, with $h^{(k)}(a)=0$ for some $0\leq k\leq n$ and $h(x)=0$ then $\exists c_{1}\in(a,x):h'(c)=0$
Then since $h'(a)=h'(c_{1})=0,\exists c_{2}\in(a,c_{1}):h''(c_{2})=0$. Applying this arguments a total of $n$ times we get:
$$
h^{(n)}(a)=h^{(n)}(c_{n})=0,\exists c_{n+1}\in (a,c_{n}):h^{(n+1)}(c_{n})=0
$$
### Proof
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
f(x)=P_{n}(x)= \frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}
$$

