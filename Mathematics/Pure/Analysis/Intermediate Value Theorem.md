This is often abbreviated to IVT, and states that if I have a [[Functions|function]] $f(x)$ which is [[continuity|continuous]] on the [[Intervals|interval]] $[a,b]$ and $u$ is any number between $f(a)$ and $f(b)$, then ther exists some number $c\in(a,b)$ such that $f(c)=u$
![[Intermediate Value Theorem 2024-10-22 14.24.01.excalidraw]]
For example $f(x)=\sin x$ is continuous on $\left[ 0, \frac{\pi}{2} \right]$ and $f(0)<\frac{1}{2}<1=f\left( \frac{\pi}{2} \right)$, so by the intermediate value theorem there exists at least one $x\in\left( 0, \frac{\pi}{2} \right)$ such that $\sin x=\frac{1}{2}$
Note: we do require continuity for the IVT to apply, otherwise we might end up with something like this, consider the [[Sign Function|$y=\text{sign}(x)$]] 
$$
\text{sign}(x)=\begin{cases}
1&\text{if }x>0\\0&\text{if }x=0\\-1&\text{if }x<0
\end{cases}
$$
Then $f(x)=\frac{\text{sign}x}{1+x^{2}}$ has $f(-1)=-\frac{1}{2}$ and $f(1)=\frac{1}{2}$, but $\not \exists x\in(-1,1)$ such that $f(x)=\frac{1}{5}$ The IVT does not apply, as $f$ has a jump discontinuity at $x=0$
$$
L^-\lim_{ x \to 0^- }f(x) =-1
$$
$$
L^+\lim_{ x \to 0^+ } =1
$$
So $L^+\neq L^-$
One important application of the IVT is finding the zeros (roots) pf a function. If $f$ is continuous on $[a,b]$ and $f(a)<0<f(b)$ then by the IVT it must go through zero somewhere in the interval there is at least one root such that $f(x)=0$
## Example
$f(x)=x^{2}-2$ is continuos on $[1,2]$ with $f(1)=-1<0$ and $f(2)=2>0$ so the IVT tells me that there is at least one root of $x^{2}-2$ in $(1,2)$, iterating this, leads to the bisection method ooooooooOoOoOoOOooOOoOOOOoOoooooOoOoOoOOooOOOoooooooOO to find roots to arbitrary accuracy

#Mathematics #Analysis #Theorem