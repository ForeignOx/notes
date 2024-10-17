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


#Mathematics #Analysis #Definition