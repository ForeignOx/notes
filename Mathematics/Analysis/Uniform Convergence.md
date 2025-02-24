A [[Sequences of Functions|sequence of functions]] $f_{n}$ [[Convergence|converges]] to a [[Functions|function]], $f$ on an [[Intervals|interval]] $I$, if
$$
\forall\varepsilon>0\exists N>0:\forall x\in I\forall n\geq N,\left| f_{n}(x)-f(x) \right|<\varepsilon 
$$
The difference between this and [[Pointwise Limit|pointwise limit]] is that the for all $x$ has been brought inside, so $N$ cannot depend on $x$
If you have uniform convergence, you have pointwise convergence, uniform convergence is stricter
![[Uniform Convergence 2025-02-24 16.27.18.excalidraw]]
So $f_{n}(x)$ is uniformly convergent if for all $n\geq N$ all $f_{n}(x)$ lie in a strip of $f(x)\pm\varepsilon$ 
The contradiction to this definition, $f_{n}(x)$ doesn't converge uniformly if:
$$
\exists\varepsilon>0:\forall N>0\exists n\geq N:\exists x=x_{n}\in I:\left| f_{n}(x_{n})-f(x) \right|\geq\varepsilon 
$$
## Examples
Consider $f_{n}(x)=x^{n}$ on $I=[0,1]$, we have already shown that it does have pointwise convergence to
$$
f(x)=\begin{cases}
0&x\in [0,1)\\1&x=1
\end{cases}
$$
But we will show that it doesn't converge uniformly
Pick $x_{n}=\sqrt[n]{ \frac{1}{2} }$ (note $x_{n}\to 1$ as $n\to \infty$)
Then 
$$
f_{n}(x_{n})=\left( \sqrt[n]{ \frac{1}{2} } \right)^{n}=\frac{1}{2}
$$
So
$$
\left| f(x_{n})-f_{n}(x_{n}) \right| =\left| 0-\frac{1}{2} \right| =\frac{1}{2}
$$
So we can pick $\varepsilon=\frac{1}{2}$, so there exists an epsilon such that for all $N$ there exist $n\geq N$ and some $x$ with $\left| f_{n}(x_{n})-f(x_{n}) \right|\geq\varepsilon$ which is what we want
Instead restrict in a region from $[0,r]$ with $r<1$
We claim that $x^{n}$ converes uniformly to $\hspace{0pt}0$ on $[0,1]$ for any $r<1$, indeed
$$
\left| f_{n}(x)-f(x) \right| =\left| x^{n}-0 \right| =\left| x^{n} \right| \leq r^{n}\forall x\in [0,1]
$$
And $r^{n}\to 0$ as $n\to \infty$ independently of $x$, so given $\varepsilon>0$, find $N$ such that $r^{n}<\varepsilon \forall n\geq N$, meaning yeah
___
Consider
$$
f_{n}(x)=3x^{3}+ \frac{\cos(nx)}{n}
$$
This will have pointwise limit $f(x)=3x^{3}$ since 
$$
0\leq\left|  \frac{\cos(nx)}{n} \right|\leq \frac{1}{n} 
$$
So by [[Squeeze Theorem|squeezing]], $\lim_{ n \to \infty } \frac{\cos(nx)}{n}=0$
Does it converge uniformly on $\mathbb{R}$?
$$
\left| f_{n}(x)-f(x) \right|=\left| \frac{\cos(nx)}{n} \right| \leq \frac{1}{n}
$$
And $\frac{1}{n}$ is independent of $x$, and tends to $\hspace{0pt}0$, so...
Pick $\varepsilon>0$, let $N=\frac{1}{\varepsilon}$, then $\left| f_{n}(x)-f(x) \right|<\frac{1}{n}\leq \frac{1}{N}=\varepsilon$ for $n\geq N$
## Uniform Convergence on Compact [[Subsets|Subsets]] (Subintervals)
This is more strict than pointwise convergence, but less strict than uniform convergence, it is the goldilocks
    If $f_{n}:I\to \mathbb{R}$ tends to $f$ uniformly in compact subintervals if $f_{n}\to f$ on all $[a,b]\subseteq I$