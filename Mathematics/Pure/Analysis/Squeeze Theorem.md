If $g(x)\leq f(x)\leq h(x)$ for all $x\neq a$ in some [[Intervals|open interval]] containing $a$ and:
$$
\lim_{ x \to a } g(x)=\lim_{ x \to a } h(x)=L\implies \lim_{ x \to a } f(x)=L
$$
## Examples
Calculate $\lim_{ x \to 0 }x^{2}\sin\left( \frac{1}{x} \right)$
As $-1\leq \sin\left( \frac{1}{x} \right)\leq 1$, then $-x^{2}\leq x^{2}\sin\left( \frac{1}{x} \right)\leq x^{2}$
![[Pasted image 20241018153130.png]]
So by using the squeeze theorem, 
$$
\lim_{ x \to 0 } x^{2}\sin\left( \frac{1}{x} \right)=0
$$
FInd $\lim_{ x \to 0 } \frac{\sin x}{x}$
![[Squeeze Theorem 2024-10-18 15.38.57.excalidraw]]
Let $T_{1}$ be the area of the triangle OAB, $T_{2}$ be the area of triangle OAC, let $S$ be the area of sector OAB
Clearly $T_{1}<S<T_{2}$
$$
T_{1}=\frac{1}{2}\sin x,T_{2}=\frac{1}{2}\tan x,S=\frac{x}{2\pi}\times \pi=\frac{x}{2}
$$
Therefore $\sin x<x<\tan x$ (as $0< x< \frac{\pi}{2}$)
Now for $x\in\left( 0, \frac{\pi}{2} \right)$:
$$
1=\frac{\sin x}{\sin x}<\frac{x}{\sin x}<\frac{\tan x}{\sin x}=\sec x
$$
And since all these functions are [[Even Functions|even]], the same set of relations holds on $\left( -\frac{\pi}{2},0 \right)$
We also have:
$$
\lim_{ x \to 0 } 1=1,\lim_{ x \to 0 } \frac{1}{\cos x}=1
$$
So by the squeeze theorem,
$$
\lim_{ x \to 0 } \frac{x}{\sin x}=1
$$
And therefore:
$$
\lim_{ x \to 0 } \frac{\sin x}{x}=1 
$$
By the Calculus of [[limit|Limits]] theorem
We can use this result to prove:
$$
\lim_{ x \to 0 }  \frac{1-\cos x}{x}=\lim_{ x \to 0 }  \frac{(1-\cos x)(1+\cos x)}{x(1+\cos x)}=\lim_{ x \to 0 }  \frac{\sin ^{2}x}{x(1+\cos x)}=\lim_{ x \to 0 } \left( \frac{\sin x}{x} \right)\left( \frac{\sin x}{1+\cos x} \right)=0
$$
As $\lim_{ x \to 0 } \frac{\sin x}{1+\cos x}=0$