We define the sine and cosine function by
$$
\sin(x):=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!}x^{2k+1}
$$
$$
 \cos(x):=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!}x^{2k}  
$$
By [[Ratio Test|ratio test]], (or [[Series#Comparison Test|comparison test]] with [[Exponential Functions|$\exp(x)$]]) we see that the [[Cauchy-Hadamard Theorem|radius of convergence]] is $R=\infty$
We have various properties:
## $f(0)$
$$
\sin(0)=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!}0^{2k+1}=0 
$$
$$
 \cos(0)=\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!}0^{2k}=1+0+0+\dots=1 
$$
## Odd/Even
Since each term in $\sin$ is [[Odd Functions|odd]], $\sin$ is odd. Since each term in $\cos$ is [[Even Functions|even]], $\cos$ is even
## Differentiation
Sine and cosine are infinitely [[Differentiation|differentiable]] with
$$
\sin'(x)=\cos(x),\cos'(x)=-\sin(x)
$$
This can be obtained by differentiating term-wise

## Compound Angle Formulae
We want to show
$$
\sin(x+y)=\sin(x)\cos(y)+\cos(x)\sin(y)
$$
$$
 \cos(x+y)=\cos(x)\cos(y)-\sin(x)\sin(y)
$$
We consider a function
$$
f(t)=\sin(x+t)\cos(y-t)+\cos(x+t)\sin(y-t)
$$
$$
f(0)=\sin(x)\cos(y)+\cos(x)\sin(y)
$$
$$
f(y)=\sin(x+y)\cos(0)+\cos(x+y)\sin(0)=\sin(x+y)
$$
$$
f'(t)=\cos(x+t)\sin(y-t)-\sin(x+t)
$$
## [[Pythagoras' Theorem|Pythagoras' Theorem]]
We want to show:
$$
\sin ^{2}(x)+\cos ^{2}(x)=1
$$
In particular,
$$
\left| \sin(x) \right| \leq 1,\left| \cos(x) \right| \leq 1\forall x\in \mathbb{R}
$$
If we consider $x=0$
$$
\sin ^{2}(0)+\cos ^{2}(0)=0+1=1
$$
Next we differentiate $\sin ^{2}(x)+\cos ^{2}(x)$:
$$
2\sin(x)\cos(x)-2\cos(x)\sin(x)=0
$$
So by the [[Monotonic Functions#Growth Theorem|growth theorem]], $\sin ^{2}(x)+\cos ^{2}(x)$ is constant, and since at $x=0$, it is $1$, we have that it is $1$ for all $x\in\mathbb{R}$
The second part is trivially true considering $x^{2}\geq 0\forall x$
## The Equation $\cos(x)=0$ has a Smallest Positive Solution
Consider $\cos(2)$. We have:
$$
\sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!}2^{2k}=1-2+\frac{16}{24}+\sum_{k=3}^{\infty} \frac{(-1)^{k}}{(2k)!}2^{2k}=-\frac{2}{3}+\sum_{k=3}^{\infty} \frac{(-1)^{k}}{(2k)!}2^{2k}   
$$
The tail is an [[Alternating Series|alternating series]] with decreasing terms:
$$
\frac{2^{2(k+1)}}{(2(k+1))!}=\frac{4}{(2k+2)(2k+1)} \frac{2^{2k}}{(2k)!}< \frac{2^{2k}}{(2k)!}
$$
By the alternating series test, we see that its value must be a negative number, since $\cos(0)=1>0$, by the [[Intermediate Value Theorem|intermediate value theorem]], the cosine function has a [[Roots|root]] in the [[Intervals|interval]] $(0,2)$. Hence the set
$$
X:=\left\{ x>0|\cos(x)=0 \right\}
$$
Is non-[[Empty Set|empty]] and [[Boundedness|bounded]] below. Thus $x_{0}=\text{inf}(X)$ exists. Now take a sequence $x_{n}\in X$ with $\cos(x_{n})=0$