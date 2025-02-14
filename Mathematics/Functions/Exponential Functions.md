An exponential [[Real Functions|function]] is any function of the form $f(x)=b^{x}$, where $b$ (called the base) is a positive real number not equal to $\hspace{0pt}1$
For all values of the base, the graph passes through the point $(0,1)$
There are two types of behaviour
- If $b>1$, the graph is increasing and has a horizontal asymtote $y=0$ along the negative $x$-axis
- If $0<b<1$ the graph is decreasing and has a horizontal asymtote $y=0$ along the positive $x$-axis
There is a special value of the base (called the natural base) $b=e$. One of the many reasons why $e$ is special is that the gradient of the graph of $e^{x}$ is always equal to $e^{x}$. Another way to say this is
$$
\frac{d}{dx}e^{x}=e^{x}
$$
___
## $e^{ x }$
### [[Convergence|Convergence]]
For every $x\in\mathbb{R}$, the sequence 
$$
(x_{n})_{n\in\mathbb{N}}=\left( 1+\frac{x}{n} \right)^{n}
$$
is convergent. We denote the limit by $e^{ x }$, it satisfies $e^{ x }>0$ and $e^{ -x }=\frac{1}{e^{ x }}$
#### Proof for $e^{ -x }=\frac{1}{e^{ x }}$:
$$
\left( 1+\frac{x}{n} \right)^{n}\times \frac{\left( 1-\frac{x}{n} \right)^{n}}{\left( 1-\frac{x}{n} \right)^{n}}=\frac{\left( \left( 1+\frac{x}{n} \right)\left( 1-\frac{x}{n} \right) \right)^{n}}{\left( 1-\frac{x}{n} \right)^{n}}=\frac{\left( 1-\frac{x^{2}}{n^{2}} \right)^{n}}{\left( 1+\frac{-x}{n} \right)^{n}}
$$
By the [[Bernoulli Inequality|Bernoulli inequality]], 
$$
1\geq \left( 1-\frac{x^{2}}{n^{2}} \right)^{n}\geq 1-\frac{nx^{2}}{n^{2}}=1-\frac{x^{2}}{n}
$$
So by the [[Squeeze Theorem|squeeze theorem]], $\left( 1-\frac{x^{2}}{n^{2}} \right)\to1$
So by [[Calculus of Limits Theorem|CoLT]], $e^{ x }=\frac{1}{e^{ -x }}$
### Lemma
Let $x\in(-\infty,1)$, then
$$
1+x\leq e^{ x }\leq \frac{1}{1-x}
$$
![[Exponential Functions 2024-11-14 11.14.41.excalidraw]]
#### Proof
Pick $n\in\mathbb{N}$ with $\frac{x}{n}>-1$, then
$$
\left( 1+\frac{x}{n} \right)^{n}\geq 1+\frac{nx}{n}=1+x
$$
By the Bernoulli inequality, so $e^{ x }\geq 1+x$
For the other inequality, look at $\frac{1}{\left( 1-\frac{x}{n} \right)^{n}}$:
$$
\frac{1}{\left( 1-\frac{x}{n} \right)^{n}}\leq \frac{1}{1-x}
$$
By the bernoulli inequality again, and since $\frac{1}{\left( 1-\frac{x}{n} \right)^{n}}$ converges to $e^{ x }$,
$$
e^{ x }\leq \frac{1}{1-x}
$$
___
### $e^{ x+y }=e^{ x }e^{ y }$
Let $x,y\in\mathbb{R}$, then
$$
e^{ x+y }=e^{ x }e^{ y }
$$
___
### The $\exp$ Function
Since $x$ was an arbitrary real number, we have a function:
$$
\exp:\mathbb{R}\to(0,\infty)
$$
$$
 x\mapsto e^{ x }=\exp(x)
$$
If $x<y$, ten
$$
\exp(y-x)=\lim_{ n \to \infty } \left( 1+\frac{y-x}{n} \right)^{n}>1=\exp(y)\exp(-x)=\frac{\exp(y)}{\exp(x)}
$$
So $\exp(x)<\exp(y)$, so the exponential function is strictly monotonically increasing
___
### [[Power Series|Power Series]]
We can instead define $\exp (x)$ as:
$$
\exp(x)=\sum_{k=0}^{\infty} \frac{x^{k}}{k!}
$$
This power series converges for all $x\in\mathbb{R}$
#### $\exp(0)=1$
To show this we let $x=0$; so
$$
\exp(0)=\frac{1}{0!}+0+\dots=1
$$
#### [[Differentiation|Differentiation]]
We want to show:
$$
\exp'(x)=\exp(x)
$$
$$
\left( \sum_{k=0}^{\infty} \frac{x^{k}}{k!}  \right)'=\sum_{k=1}^{\infty} \frac{kx^{k-1}}{k!}=\sum_{k=0}^{\infty} \frac{(k+1)x^{k}}{(k+1)!}=\sum_{k=0}^{\infty} \frac{x^{k}}{k!}   
$$
Which is what we want
#### Additive property
We want to show for all $x,y\in\mathbb{R}$:
$$
\exp(y+x)=\exp(x)\exp(y)
$$
$$
 \exp(-x)=\frac{1}{\exp(x)}
$$
We can do this in two ways. One uses the [[Cauchy Product Theorem|Cauchy Product theorem]], the other, we can consider
$$
f(t)=\exp(x+t)\exp(y-t)
$$
$$
f(0)=\exp(x)\exp(y)
$$
$$
 f(y)=\exp(x+y)\exp(y-y)=\exp(x+y)
$$
Consider 
$$
f'(t)=epx(x+t)\exp(y-t)-\exp(x+t)\exp(y-t)=0
$$
So from what we know about [[Monotonic Functions|monotonic functions]] and the growth theorem, we $f(t)$ is constant, hence 
$$
\exp(x)\exp(y)=\exp(x+y)
$$
Since $f(y)=f(0)$
For $\exp(-x)=\frac{1}{\exp(x)}$, we plug in $y=-x$
$$
\exp(0)=\exp(x)\exp (-x)
$$
$$
\implies \exp(-x)=\frac{1}{\exp(x)}
$$
#### $\exp(x)>0\forall x\in\mathbb{R}$
It is clearly true for $x>0$, for $x<0$, $\exp(x)=\frac{1}{\exp(-x)}>0$
#### $\exp(x)$ is Monotone Increasing
$$
\exp'(x)=\exp(x)>0
$$
So strictly increasing by growth theorem
#### Limits Tending to Infinity
For $x>0$, $\exp(x)>1+x$ which is unbounded, so
$$
\lim_{ x \to \infty } \exp(x)=\infty
$$
## Other bases
For $a>0$ and $x\in\mathbb{R}$, define
$$
a^{x}=\exp(x\ln (a))
$$
### Properties
- $a^{x+y}=a^{x}a^{y}$
- $(a^{x})^{y}=a^{xy}$

#Mathematics #Functions 