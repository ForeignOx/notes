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
