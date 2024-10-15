Given a [[Bijective Functions|bijective]] [[Real Functions|function]] $f$ with domain $S$ and [[Image and Pre-Image|image]] $I$, an inverse function is a unique function $g$ with domain $I$ and image $S$ such that, for every $y\in I$,
$$
f(g(y))=y
$$
Usually we use the notation $f^{-1}$ for the inverse function, so:
$$
(f\cdot f^{-1})(x)=x=(f^{-1}\cdot f)(x)
$$
![[Inverses of Functions 2024-10-15 14.13.37.excalidraw]]
Note that $\text{Ran}f^{-1}=\text{Dom}f,\text{Dom}f^{-1}=\text{Ran}f$, equivalently, $i=f^{-1}(x)\iff f(y)=x$
For example, if
$$
f(x)=\frac{1}{3x-4}
$$
(which has domain $S=\mathbb{R}\setminus \{ \frac{4}{3}\}$) then
The graph of the inverse of a funciton $f^{-1}(x)$ is found by reflecting the graph of $f(x)$ in the line $y=x$

$$
f^{-1}(y)=\frac{1+4y}{3y}
$$
Often, we can find the inverse function by writing 
$$
y=f(x)
$$
and then rearranging so that $x$ is the subject
We can't always find the inverse of a function over a given domainl. For example, $f(x)=x^{2}$ does not have an inverse over the whole real line, because there are two $x$-values for each $y$-value. On the other hand, if we only look at the positive part of the real line, we can find an inverse: $f^{-1}(x)=\sqrt{ x }$

#Mathematics #Functions #Definition