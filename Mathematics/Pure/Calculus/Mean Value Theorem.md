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

