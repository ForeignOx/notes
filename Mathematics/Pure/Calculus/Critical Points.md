We say that a [[Functions|function]] $f$ has a local minimum at a point $x=a$ if:
$$
\exists h>0:f(a)\geq f(x)\forall x\in (a-h,a+h)
$$
Or a local maximum at a point $x=a$ if:
$$
\exists h>0:f(a)\leq f(x)\forall x\in (a-h,a+h)
$$
A local extremum is either a local maximum or a local minimum
If $f(x)$ has a local maximum (or minimum) at $x=a$, and if it is [[Differentiation|differentiable]] at $x=a$, then $f'(a)=0$
We say $f(x)$ has a stationary point at $x=a$, if it is differentiable at $x=a$ and $f'(a)=0$
An interior point $x=a$ of the domain of $f(x)$ is a critical point if either $f'(a)=0$ or doesn't exist, hence all stationary points are critical, but not the other way
If $f(x)$ is twice differentiable in an open interval around $x=a$ with $f''(a)=0$ and changes sign at $x=a$, then we say that $x=a$ is a point of inflection
If $c\in \text{Dom}f$ and if $\exists h>0$ such that $f(x)$ is defined on $[c,c+h)$, but not $(c-h,c]$ (or vice-versa), then $x=c$ is an endpoint of $f(x)$
If $x=c$ is an endpoint of $f(x)$, then $f(x)$ has an endpoint maximum (or minimum) at $x=c$ if $f(x)\leq f(c)$ (or $f(x)\geq f(c)$) for $x$ close to $c$
## Proof
Since $f(x)$ is differentiable at $x=a$:
$$
\lim_{ x \to a^- } \frac{f(x)-f(a)}{x-a}=\lim_{ x \to a^+ } \frac{f(x)-f(a)}{x-a}=f'(a)
$$
If $f(x)$ has a local maximum at $x=a$, then $\frac{f(x)-f(a)}{x-a}\leq 0$ for $x\in(a,a+h)$, as the numerator is negative, and the denominator is positive, and if the expression is always negative, the limit is also:
$$
 \lim_{ x \to a^+ } \frac{f(x)-f(a)}{x-a}=f'(a)\leq 0
$$
But also $\frac{f(x)-f(a)}{x-a}\geq 0$, for $x\in(a-h,a)$, then the numerator and denominators are both negative, so is positive, and if an expression is always positive, the limit is also:
$$
\lim_{ x \to a^- } \frac{f(x)-f(a)}{x-a}=f'(a)\geq 0
$$
So:
$$
0\leq f'(a)\leq 0\implies f'(a)=0
$$
## Example
$f(x)=x^{3}$ has $f'(0)=0$, so $x=a$ is a stationary point (& critical point), but not a local extremum, since $f(x)>f(0)\forall x\in(0,h)$, but $f(x)<f(0)\forall x\in(-h,0)$, but $f''(x)=6x$, so $f''(0)=0$ and since $f''(x)<0$ for $x<0$ and $f''(x)>0$ for $x>0$, then $x=0$ is a point of inflection
## First Derivative Test
Suppose $f(x)$ is [[Continuity|continuous]] at a critical point $x=a$
- If $\exists h>0:f'(x)<0\forall x\in(a-h,a),f'(x)>0\forall x\in(a,a+h)$, then $x=a$ is a local minimum
- If $\exists h>0:f'(x)>0\forall x\in(a-h,a),f'(x)<0\forall x\in(a,a+h)$, then $x=a$ is a local maximum
- If $\exists h>0:f'(x)$ has constant sign $\forall x\neq a$ in $(a-h,a+h)$, then $x=a$ is not a local extremum
### Example
$f(x)=|x|$ is a continuous function, but $f'(x)\neq 0$, so $\not\exists$ stationary point. $x=a$ is a critical point (as the first derivative doesn't exist here)
$$
f(x)<0\forall x\in (-1,0)\,\&\,f'(x)>0\forall x\in (0,1)
$$
So $x=0$ is a local minimum
## Second Derivative Test
Suppose $f(x)$ is twice differentiable at $x=a$, with $f'(a)=0$
- If $f''(a)>0$ then $x=a$ is a local minimum
- If $f''(a)<0$ then $x=a$ is a local maximum
- If $f''(a)=0$, then the second derivative test doesn't say anything :(
___
For a 3D curve, a stationary point is a point $P$ where the tangent plane is horizontal, so normal is parallel to:
$$
\begin{pmatrix}
0\\0\\1
\end{pmatrix}
$$
And hence for $y=f(x,y)$, 
$$
\frac{ \partial f }{ \partial x } \Bigr{|}_{\substack{P}}=0 \text{ and } \frac{ \partial f }{ \partial y } \Bigr{|}_{P}=0
$$
These are some classifications for stationary points in 3D:
![[Pasted image 20240311125832.png]]

#Mathematics #Calculus