The rough idea behind a limit is that a [[Functions|function]] $f(x)$ las a limit $L$ at a point $x=a$ if $f(x)$ is close to $L$ whenever $x$ is close to $a$. More precisely, how can we check if $f$ is close to $L$ if $x$ is close to $a$? If we have an acceptable error $\epsilon$ ($\epsilon>0$) betewen $f$ and $L$, then I would need the distance $|f(x)-L|<\epsilon$ for all $x$ in some interval around $a$. So if I can always (for any $\epsilon>0$) I can find some distance $\delta,\delta>0$ such that $|f(x)-L|<\epsilon \forall 0<|x-a|<\delta$ then we say that $f(x)$ has a limit $L$ as $x$ tends to $a$, or: $\lim_{ x \to a }f(x)=L$
![[Limit 2024-10-15 14.31.22.excalidraw]]
We essentially need to find a certain $\delta$ for a given $\epsilon$ such that this is true
## Definition
The formal definition is thus:
$$
\lim_{ x \to a } f(x)=L\iff \forall\epsilon>0\exists\delta>0:|f(x)-L|<\epsilon \forall x :0<|x-a|<\delta
$$
If there is no such $L$ then the limit does not exist
Note we do not require $f(a)=L$ or for $f(a)$ to even exist, as we only consider the interval $0<|x-a|<\delta$
## Facts About Limits
You can use the following facts without proof:
- The limit is unique at any point
- If $f(x)=g(x)$ (except possiby at $x=a$) in some [[intervals|interval]] containing $a$, then they have the same limit at $x=a$; $\lim_{ x \to a }f(x)=\lim_{ x \to a }g(x)$
- If $f(x)$ is [[Boundedness|bounded]] from below, $f(x)\geq k$ on either some interval $(a,b)$ or $(c,a)$ and if $\lim_{ x \to a }f(x)=L$ then $L\leq k$
- If $f(x)$ is bounded from above, $f(x)\leq k$ on either some interval $(a,b)$ or $(c,a)$ and if $\lim_{ x \to a }f(x)=L$ then $L\geq k$
- Calculus of Limits theorem (CoLT): If $\lim_{ x \to a }f(x)=L$ and $\lim_{ x \to a }g(x)=M$, then:
    - $\lim_{ x \to a }(f(x)+g(x))=L+M$, 
    - $\lim_{ x \to a }(f(x)g(x))=LM$, 
    - if $M\neq 0$, $\lim_{ x \to a }\left( \frac{f(x)}{g(x)} \right)=\frac{L}{M}$
## Examples
$$
\lim_{ x \to 0 } \frac{1}{x^{2}}
$$
Does not exist as limits must be real numbers and $\infty$ is not a real number
We can use the calculus of limits theorem here:
$$
\lim_{ x \to \frac{\pi}{2} } x^{2}\sin x=\left( \lim_{ x \to \frac{\pi}{2} }x^{2}  \right)\times\left( \lim_{ x \to \frac{\pi}{2} } \sin x \right)=\frac{\pi^{2}}{4}\times 1=\frac{\pi^{2}}{4}
$$
And we know that the limit if the function is defined at a point $a$ is $f(a)$
Here is a trickier case:
$$
\lim_{ x \to 3 } \frac{2x^{2}-18}{x-3}=\lim_{ x \to 3 } \frac{2(x-3)(x+3)}{x-3}=\lim_{ x \to 3 } 2(x+3)=12
$$
We can perfom the simplification with factorising when doing limits, as they are defined arount $x=3$, but the functions are in fact different as $x=3$ is not in the domain of the first function
### Two Trigonometric Limits
Two important limits are:
$$
\lim_{ x \to 0 } \frac{\sin x}{x}=1,\lim_{ x \to 0 } \frac{1-\cos x}{x}=0
$$
These can be proven usen the squeeze theorem

#Mathematics #Analysis #Definition