## Regulated Integral
Let $f:[a,b]\to \mathbb{R}$ be a [[Regulated Functions|regulated function]], say [[Sequences of Functions|$f_{n}\to f$]] where $f_{n}$ are [[Step Functions|step functions]], then we say the integral of $f$ is:
$$
I(f)=\lim_{ n \to \infty } I(f_{n})
$$
Where $I(f_{n})$ is the integral of the step functions, or the [[Riemann Sum|riemann sums]]
We need to check whether this limit exists however
### Proof
Since we don't know what $I(f_{n})$'s [[Convergence|converge to]], and we don't know if they are [[Convergent Bounded Sequences have Limits in the Bound|monotone and bounded]], we need to use [[Cauchy Sequences|cauchy sequences]], so we will show that the sequence $I(f_{n})=:a_{n}$ forms a cauchy sequence
Take $\varepsilon>0$, we need to find $N$ such that $\forall n,m\geq N$, $\left| a_{n}-a_{m} \right|<\varepsilon$
We can take $N$ to be the same as the one fro the convergence of the regulated function, and let  $n,m\geq N$. For the step functions $f_{n}(x),f_{m}(x)$, take a common refinement of the two underlying partitions $a=x_{0},x_{1},\dots,x_{N}=b$, then we need to check
$$
I(f_{n})-I(f_{m})=\sum_{k=0}^{N}(x_{k+1}-x_{k})f_{n}(x_{k}^{*})-\sum_{k=0}^{N}(x_{k+1}-x_{k})f_{m}(x_{k}^{*})
$$
$$
 \left| I(f_{n})-I(f_{m}) \right| =\sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-f_{m}(x_{k}^{*}) \right| 
$$
$$
= \sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-f(x_{k}^{*})+f(x_{k}^{*})-f_{m}(x_{k}^{*}) \right| 
$$
Which by the [[Triangle Inequality|triangle inequality]] we have:
$$
\leq \sum_{k=0}^{N}(x_{k+1}-x_{k})(\underbrace{ \left| f_{n}(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } +\underbrace{ \left| f_m(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } )<2\varepsilon \sum_{k=0}^{N}(x_{k+1}-x_{k})=2(b-a)\varepsilon
$$
We know those parts are less than $\varepsilon$ from the definition of $f_{n},f_{m}$ as regulated functions
Hence it is a Cauchy sequence, hence it converges
___
We also need to check that it is independent of the choice of sequence of step functions, as there are many that could converge
### Proof
Take $f_{n}\to f$, $g_{n}\to f$ where $f_{n},g_{n}$ are step functions which converge [[Uniform Convergence|uniformly]], we need
$$
\lim_{ n \to \infty } I(f_{n})=\lim_{ n \to \infty } I(g_{n})
$$
We are going to do the same thing :/
Take $\varepsilon>0$, we need to find $N$ such that $\left| I(f_{n})-I(g_{n}) \right|<\varepsilon \forall n\geq N$, again we take $N$ as in the definition of regulated function for both $f_{n},g_{n}$ (the maximum of those at least, which works for both). For $f_{n},g_{n}$, take a common refinement so we have the same partition for each, then the process is identical:
$$
I(f_{n})-I(g_{n})=\sum_{k=0}^{N}(x_{k+1}-x_{k})f_{n}(x_{k}^{*})-\sum_{k=0}^{N}(x_{k+1}-x_{k})g_{n}(x_{k}^{*})
$$
$$
  \left| I(f_{n})-I(g_{n}) \right| =\sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-g_{n}(x_{k}^{*}) \right| 
$$
$$
 = \sum_{k=0}^{N}(x_{k+1}-x_{k})\left| f_{n}(x_{k}^{*})-f(x_{k}^{*})+f(x_{k}^{*})-g_{n}(x_{k}^{*}) \right| 
$$
$$
 \leq \sum_{k=0}^{N}(x_{k+1}-x_{k})(\underbrace{ \left| f_{n}(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } +\underbrace{ \left|g_{n}(x_{k}^{*})-f(x_{k}^{*}) \right| }_{ <\varepsilon } )<2\varepsilon \sum_{k=0}^{N}(x_{k+1}-x_{k})=2(b-a)\varepsilon
$$
___
### Example
Consider $f(x)=x$ on $[a,b]$, then to define $f_{n}(x)$, take the equidistant partition, $x_{k}=a+k \frac{b-a}{n}$ for $k=0,\dots,n$, and let $x_{k}^{*}=x_{k}$, set $f(x)=f(x_{k}^{*})=f(x_{k})$ for $x\in(x_{k},x_{k+1})$, and since $f_{n}\to f$ are lipschitz as it is bounded, they tend uniformly. Take for example $a=0,b=1$, then
$$
I(f_{n})=\sum_{k=0}^{n}\underbrace{ (x_{k+1}-x_{k}) }_{ =\frac{b-a}{n}=\frac{1}{n} }f\left( \underbrace{ x_{k}^{*} }_{ =x_{k}=\frac{k}{n} } \right)=\frac{1}{n^{2}}\sum_{k=0}^{n}k=\frac{1}{n^{2}} \frac{(n+1)n}{2}\to \frac{1}{2}
$$
## Indefinite Integrals (or Anti-[[Differentiation|Derivative]]s)
A [[Functions|function]] $F(x)$ is called an indefinite integral or antiderivative of a function $f(x)$ in the [[Intervals|interval]] $(a,b)$ if $F(x)$ is differentiable:
$$
F'(x)=f(x)\forall x\in (a,b)
$$
We write:
$$
F(x)=\int f(x) \, dx
$$
Note that if $F(x)$ is an indefinite integral, then so is $F(x)+c$ for any constant $c$, since $\frac{d }{dx}(F(x)+c)=\frac{d }{dx}(F(x))$
It is important to include this arbitrary constant when writing indefinite integrals
If $F_{1}(x)$ and $F_{2}(x)$ are both indefinite integrals of $f(x)$, then $F_{2}(x)-F_{1}(x)=c$, since:
$$
\frac{d }{dx} (F_{2}(x)-F_{1}(x))=\frac{d }{dx} (F_{2}(x))-\frac{d }{dx} (F_{1})(x)=f(x)-f(x)=0
$$
Therefore $F_{2}(x)-F_{1}(x)$ is constant. or is it...? yeh it is
___
### Examples
Let $f(x)=\frac{1}{x}$ on $(0,\infty)$, set 
$$
L(x)=\int_{1}^{x} \frac{1}{t} \, dt
$$
Then $L(1)=0$, $L'(x)=\frac{1}{x}$ from [[Fundamental Theorem of Calculus|FToC]]. Now $L(x)$ is increasing, $L'(x)>0$, we also have 
$$
L(xy)=L(x)+L(y)
$$
We can show it is true for one point $y=1$, we want to take derivatives and show that it is constant:
$$
LHS:  y\times \frac{1}{xy}=\frac{1}{x}
$$
$$
RHS: \frac{1}{x}
$$
These are the same, so this is always true, so we also have by letting $y=\frac{1}{x}$:
$$
L\left( \frac{1}{x} \right)=-L(x)
$$
We also know that $L(2)>\frac{1}{2}$, since
$$
\int_{1}^{2} \frac{1}{t} \, dt >\int_{1}^{2} \frac{1}{2} \, dt
$$
We can then say that $L(2^{n})>\frac{n}{2}$ by using the addition law many times, i.e. $nL(2)$, so $L(x)\to \infty$ as $x\to \infty$
So we have a function that satisfies all the logarithm properties, so it is the logarithm, hence we have the exponential function as the inverse, so from this we can get $\sinh$ and $\cosh$ properties ect. We can do the same technique with $\arcsin$ to find $\sin$
## Integrability
We say $f(x)$ is integrable in $(a,b)$ if it has an indefinite integral on $(a,b)$ which is [[Continuity|continuous]] on $[a,b]$
## Definite Integrals
A definite integral of a function $f(x)$ gives the (signed) area between $f(x)$ and the $x$-axis
![[Integration 2024-11-05 14.26.00.excalidraw]]
In the above diagram, the green would have positive area, and the blue, negative
We define this as the [[Limit|Limit]] of a [[Riemann Sums|Riemann Sum]], by splitting the area into rectangles:
![[Integration 2024-11-05 14.28.16.excalidraw]]
There are lots of ways we could do this, by choosing where we place the $x_{i}$s and where we define the heights of the rectangles. If $f(x)$ is continuous, and the rectangles have small width, we expect this to be a good approximation and the error can be reduced to zero by taking the limit of the width of the rectangles to zero. We say this limit exists if it is independent of how we construct hte rectangles
The definite integral is given in terms of a Riemann sum by taking a limit as the [[Subdivisions|norm]] $|S|$ goes to 0
We say this limit exists if it is independent of subdivision and set of sample points:
Let $f(x)$ be defined $\forall x\in[a,b]$, the definite integral of $f(x)$ from $a$ to $b$ is then:
$$
\int ^{b}_{a} f(x) \, dx =\lim_{ |S| \to 0 } R
$$
It can be shown that this limit does exists if $f$ is continuous on $[a,b]$
We can define:
$$
\int ^{b}_{a} f(x) \, dx= -\int ^{a}_{b}  f(x)\, dx 
$$
Which implies:
$$
\int ^{a}_{a} f(x) \, dx=0
$$
### Properties
The definite integral satisfies the following properties:
Let $f(x),g(x)$ be integrable functions in $(a,b)$
- Linearity, if $\lambda,\mu \in\mathbb{R}$, then $(\lambda f+\mu g)(x)$ is also integrable in $(a,b)$ with
$$
\int ^{b}_{a} (\lambda f+\mu g)(x) \, dx =\lambda \int ^{b}_{a} f(x) \, dx +\mu \int ^{b}_{a} g(x) \, dx 
$$
- If $c\in[a,b]$, then we have additivity:
$$
\int ^{b}_{a} f(x) \, dx =\int ^{c}_{a} f(x) \, dx +\int ^{b}_{c} f(x) \, dx 
$$
- If $f(x)\geq g(x)\forall x\in(a,b)$, then we have monotonicity:
$$
\left| \int ^{b}_{a} f(x) \, dx  \right| \leq \int ^{b}_{a} \left| f(x) \right|  \, dx 
$$
$$
\int ^{b}_{a} f(x) \, dx \geq \int ^{b}_{a} g(x) \, dx 
$$
- If $m\leq f(x)\leq M\forall x\in(a,b)$ then
$$
m(b-a)\leq\int ^{b}_{a} f(x) \, dx \leq M(b-a)
$$
- If $f(x)\geq 0\forall x\in(a,b)$, then and $f$ continuous and there exists a point $c\in[a,b]:f(c)>0$
$$
\int ^{b}_{a} f(x) \, dx >0
$$
#### Proof of Monotonicity
By linearity, it is enough to consider if $f(x)\geq 0$ and show $\int ^{b}_{a} f(x) \, dx \geq 0$. So take $f_{n}\to f$ uniformly, so given $\varepsilon>0$, find $f_{n}(x)$ such that $\left| f(x)-f_{n}(x) \right|<\varepsilon \forall x\in[a,b]$
Since $f(x)>0$, we get
$$
f_{n}(x)>-\varepsilon \forall x\in [a,b]
$$
(We can't rule out that $f_{n}$ is not negative, but the most negative it can be is if $f(x)=0\forall x\in[a,b]$, giving us the above inequality)
![[Integration 2025-03-13 11.26.40.excalidraw]]
This means that
$$
I(f_{n})>-\varepsilon(b-a)
$$
So $\lim_{ n \to \infty }I(f_{n})$ is bigger than any negative number $\implies I(f)\geq 0$
Next consider that $\left| f(x) \right|=\pm f(x)$, so $f(x)\leq \left| f(x) \right|$, but $\left| f(x) \right|>0$, so we get our property with absolute values we want
For the last part we can consider the following diagram:
![[Integration 2025-03-13 11.33.41.excalidraw]]
#### Proof of $f(x)\geq 0\implies \int ^{b}_{a} f(x) \, dx\geq 0$ 
Set $C=f(c)$, by continuity, there exists a $\delta>0$ such that $f(x)>\frac{C}{2}$ for $\left| x-c \right|<\delta$ with this:
$$
\int ^{b}_{a} f(x) \, dx =\int_{a}^{c-\delta} \underbrace{ f(x) }_{ \geq 0 } \, dx +\int_{c-\delta}^{c+\delta} \underbrace{ f(x) }_{ \geq \frac{C}{2} } \, dx +\int_{c+\delta}^{b} \underbrace{ f(x)  }_{ \geq 0 }\, dx \geq 0+\frac{C}{2}2\delta+0=C\delta>0
$$
This does in fact require continuity, consider the function
$$
f(x)=\begin{cases}
0 & x\neq 0\\1 & x=0
\end{cases}
$$
Which is not continuous at $x=0$, and $f(x)\geq 0$, but $\int_{-1}^{1} f(x) \, dx=0$ since the step functions tend to 0

#Mathematics #Calculus #Definition