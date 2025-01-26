A logarithm is the [[Inverses of Functions|inverse]] of an [[Exponential Functions|exponential]] [[Real Functions|function]]: if $y=b^{x}$, then $x=\log_{b}(y)$. As with exponential functions, we have to specify the base of the logarithm
The domain of a logarithm function is the image of an exponential function and hence is $(0,\infty)$. The image of a logarithm function is the domain of an exponential function and thus is $\mathbb{R}$
When the base of a logarithm is $e$, we call our function the natural logarithm denoted by $\ln (x)$ 
A logarithm grows very slowly as $x$ grows large and positive (more slowly than a linear function) and has a vertical asymptote at $x=0$
Some important properties of logarithms are:
- $\log_{b}1=0$ (this follows from $b^{0}=1$)
- $\log_{b}b^{x}=x$
- $\log_{b}\alpha\beta=\log_{b}\alpha+\log_{b}\beta$
- $\log_{b} \frac{\alpha}{\beta}=\log_{b}\alpha-\log_{b}\beta$
- $\log_{b}(x^{r})=r\log_{b}x$
___
## The $\ln$ function
Let $a>0$, then there exists a unique $x\in\mathbb{R}$ with $\exp(x)=a$
### Proof
Consider $X=\{ y\in\mathbb{R}\mid \exp(y)<a \}$, for $n\in\mathbb{N}$,
$$
\exp(n)=e^{ n }>1^{n}=1
$$
So it is unbounded, so $e^{ n }$ is an [[Boundedness|unbounded]] [[Sequences|sequence]]
So there is [[Natural Numbers|$n\in\mathbb{N}$]] with $e^{ n }>a$ also if $x>n$, $e^{ n }<e^{ x }$ as $e^{ x }$ is monotonically increasing, so $n$ is an upper bound for $X$
Look at $e^{ -n }=\frac{1}{e^{n}}\to 0$, then there is $n\in\mathbb{N}$ with $e^{ -n }<a$, so $-n\in X$, so $X$ is not empty
Now we can use [[Supremum and Infimum|$x=\sup(X)$]] from the [[Real Numbers#Completeness Axiom|completeness axiom]]
Now we want to show that $\exp(x)<a$ or $\exp(a)>a$ is not true:
Assume $\exp(x)>a$, look at $\exp\left( x-\frac{1}{n} \right)$ with $n\in\mathbb{N}$
$$
\exp\left( x-\frac{1}{n} \right)=\frac{\exp(x)}{\exp\left( \frac{1}{n} \right)}
$$
Recall $1+x\leq e^{ x }\leq \frac{1}{1-x}$, using this in the denominator, we get
$$
\exp\left( x-\frac{1}{x} \right)\geq \frac{\exp(x)}{\frac{1}{1-\frac{1}{n}}}=\exp(x)\left( 1-\frac{1}{n} \right)
$$
So
$$
\exp\left( x-\frac{1}{n} \right)\geq \exp(x)-\frac{\exp(x)}{n}
$$
We want this to be $>a$, so chose $n$ so large that
$$
\frac{\exp(x)}{n}<\exp(x)-a
$$
By the [[Theorem of Archimedes|theorem of Archimedes]], with such $n$ we have
$$
\exp\left( x-\frac{1}{n} \right)>\exp(x)-\exp(x-a)=a
$$
So $x-\frac{1}{n}$ is an upper bound for $X$, contradicting that $x$ was the supremum, so $\exp(x)\leq a$
Next you'd have to show that $\exp(a)\not<a$
___
Now we can define the logarithm:
$$
\ln:(0,\infty)\to \mathbb{R}
$$
Defined by $\ln x=a$, where $a\in\mathbb{R}$ is such that $\exp(a)=x$
___
## Other Bases
For $a>0$, $a\neq 1$, define
$$
\log_{a}(x)=\frac{\ln(x)}{\ln (a)}
$$
### Properties
Let $a,b>0$ with $b\neq 1$ and $x,y\in\mathbb{R}$, then
- $\log_{b}(xy)=\log_{b}(x)+\log_{b}(y)$ for $x,y>0$
- $\log_{b}(x^{y})=y\log_{b}(x)$ for $x>0$
## Useful [[Inequalities|Inequality]]
$$
\frac{x-1}{x}\leq \ln x\leq x-1
$$
proof laters jeez
### Example
For $k\in\mathbb{N}$, we have
$$
\lim_{ n \to \infty } \frac{n^{k}}{e^{ n }}=0
$$

#Mathematics #Functions 