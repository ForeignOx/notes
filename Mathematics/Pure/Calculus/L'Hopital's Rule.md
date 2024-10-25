If [[Limit|$\lim_{ x \to a }f=L$]], and $\lim_{ x \to a }g(x)=M\neq 0$, then:
$$
\lim_{ x \to a } \frac{f(x)}{g(x)}=\frac{L}{M}
$$
By the calculus of limits theorem
If $L\neq 0$ and $M=0$, then $\lim_{ x \to a } \frac{f(x)}{g(x)}$ does not exist
If $L=M=0$, we say the limit is of indeterminant form, this means the limit might or might not have a well-defined value, but we can't tell simply by knowing $L$ and $M$
Limits of the following form are all indeterminant:
$$
\frac{L}{M}=\frac{0}{0}, \frac{\infty}{\infty}, 0\times \infty,0^{0}, 1^{\infty},\infty^0
$$
L'Hopital's rule applies to the first two cases
If $f(x)$ and $g(x)$ are [[Differentiation|differentiable]] on $I=(a-h,a)\cup(a,a+h)$, i.e. $0<|a|<h$ for some $h>0$ with:
$$
\lim_{ x \to a } f(x)=\lim_{ x \to a } g(x)=0
$$
And if:
$$
\lim_{ x \to a } \frac{f'(x)}{g'(x)}
$$
Exists, with $g'(x)\neq 0,\forall x\in I$, then:
$$
\lim_{ x \to a }  \frac{f(x)}{g(x)}=\lim_{ x \to a } \frac{f'(x)}{g'(x)}
$$
If applying L'Hopital's rule gives another indeterminant form, then we can apply it again, and so on 
## Mini fake proof
For the case where $f'(a)$ and $g'(a)$ both exist and and are differentiable at $a$ and are [[Continuity|continuous]] and $g'(x)\neq 0$, then
$$
\lim_{ x \to a } \frac{f(x)}{g(x)}=\underbrace{ \lim_{ x \to a } \frac{f(x)-f(a)}{g(x)-g(a)} }_{ \text{since }g(a)=f(a)=0 }=\lim_{ x \to a } \frac{\frac{f(x)-f(a)}{x-a}}{\frac{g(x)-g(a)}{x-a}}=\frac{\lim_{ x \to a } \frac{f(x)-f(a)}{x-a}}{\lim_{ x \to a } \frac{g(x)-g(a)}{x-a}}=\frac{f'(a)}{g'(a)}=\lim_{ x \to a } \frac{f'(x)}{g'(x)}
$$
We can show the last part thus:
$$
f'(a)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}
$$
Let $x=a+h$:
$$
f'(a)=\lim_{ x \to a } \frac{f(x)-f(a)}{x-a}
$$
## Example
$$
\lim_{ x \to 0 } \frac{2\sin x-\sin(2x)}{x-\sin x}=\lim_{ x \to 0 } \frac{2\cos x-2\cos(2x)}{1-\cos x}=\lim_{ x \to 0 }  \frac{-2\sin x+4\sin(2x)}{\sin x}=\lim_{ h \to 0 } \frac{-2\cos x+8\cos(2x)}{\cos x}
$$
$$
= \frac{-2+8}{1}=6 
$$

#Mathematics #Calculus #Theorem 