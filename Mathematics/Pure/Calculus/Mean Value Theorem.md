If [[Functions|$f(x)$]] is [[Continuity|continuous]] on [[Intervals|$[a,b]$]] and [[Differentiation|differrentiable]] on $(a,b)$, then $\exists c\in(a,b)$ such that:
$$
f'(c)=\frac{f(b)-f(a)}{b-a}
$$
Geometrically, this means there is at least one point at which the tangent is parallel to the line joining the end points
## Proooooooooooooooooooooooooooooooooof
Let 
$$
g(x)=(b-a)(f(x)-f(a))-(x-a)(f(b)-f(a))
$$
(the shear of $f(x)$), then $g(a)=0=g(b)$ and $g(x)$ satisfies the requirements of [[Rolle's Theorem|Rolle's theorem]], so $\exists c\in(a,b)$ such that $g'(c)=0$, but
$$
g'(x)=(b-a)f'(x)-(f(b)-f(a))
$$
So
$$
g'(c)=(b-a)f'(c)-(f(b)-f(a))=0
$$
implies
$$
f'(c)=\frac{f(b)-f(a)}{b-a}
$$

___
We can use the mean value theorem to prove results relating monoticity to the sign of the derivative
Suppose $f(x)$ is continuous on $[a,b]$, and differentiable on $(a,b)$ with $f'(x)\geq 0\forall x\in(a,b)$, then $f(x)$ is monotonic increasing
## Proof
If $a\leq x_{1}<x_{2}\leq b$, then by the MVT,
$$
\exists c\in(x_{1},x_{2}):f'(c)=\frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}
$$
Since $f'(x)\geq 0\forall x\in(x_{1},x_{2})$, then we must have $f(x_{2})\geq f(x_{1})$, so $f(x)$ is monotonic increasing
We can show similar results for monotonic decreasing and strictly monotonic increasing/decreasing