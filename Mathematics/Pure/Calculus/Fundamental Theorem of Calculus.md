The following theorem connects definite and indefinite [[Integration|integrals]]
If [[Functions|$f(x)$]] is [[Continuity|continuous]] on [[Intervals|$[a,b]$]], then the function
$$
F(x)=\int ^{x}_{a} f(t) \, dt 
$$
Defined for all points $x\in[a,b]$ is continuous on $[a,b]$, [[Differentiation|differentiable]] on $(a,b)$ and is the indefinite integral of $f(x)$ on $(a,b)$, i.e.
$$
F'(x)=\frac{d }{dx} \int ^{x}_{a} f(t) \, dt =f(x)\forall x\in (a,b)
$$
Furthermore if $\tilde{F}(x)$ is any indefinite integral of $f(x)$ on $(a,b)$, then
$$
\int ^{b}_{a} f(t) \, dt =\tilde{F}(b)-\tilde{F}(a)=[\tilde{F}(x)]^b_{a}
$$
## Proof
Important parts only (for now)
For $a\leq x<x+h<b$, we have:
$$
    F(x+h)-F(x)=\int ^{x+h}_{a} f(t) \, dt -\int ^{x}_{a} f(t) \, dt
$$
$$
= \int ^{x+h}_{a} f(t) \, dt +\int ^{a}_{x} f(t) \, dt =\int _{x}^{x+h}f(t) \, dt 
$$
Using the property $\hspace{0pt}2$ of definite integrals
Let $m(h)$ and $M(h)$ denote the min and max values of $f(x)$ on $[x,x+h]$ which must exist due to the [[Extreme Value Theorem|extreme value theorem]]. Then by the 4th property:
$$
hm(h)\leq \int _{x}^{x+h}f(t) \, dt \leq hM(h)
$$
Substituting this and dividing by $h$,
$$
m(h)\leq \frac{F(x+h)-F(x)}{h}\leq M(h)
$$
Since $f(x)$ is continuous on $[x,x+h]$, we have:
$$
\lim_{ h \to 0^+ } m(h)=f(x)=\lim_{ h \to 0^+ } M(h)
$$
And so by the [[Squeeze Theorem|squeeze theorem]],
$$
\lim_{ h \to 0^+ } \frac{F(x+h)-F(x)}{h}=f(x)
$$
To get the limit for $h\to0^-$ we can give a similar argument, so putting them together:
$$
F'(x)=\lim_{ h \to 0 } \frac{F(x+h)-F(x)}{h}=f(x)
$$
Showing $F(x)$ is an indefinite integral of $f(x)$
![[Fundamental Theorem of Calculus 2024-11-07 14.35.42.excalidraw]]
For the final part, if $\tilde{F}(x)$ is an indefinite integral of $f(x)$ in $(a,b)$, then $\tilde{F}(x)=F(x)+c$ for some $c\in\mathbb{R}$, and so
$$
[\tilde{F}(x)]_{a}^{b}=\tilde{F}(b)-\tilde{F}(a)=(F(b)+c)-(F(a)+c)=F(b)-F(a)=\int ^{b}_{a} f(t) \, dt 
$$
The FTOC gives a simple rule for differentiating a definite integral with respect to its limits
## Example
$$
\frac{d }{dx}\int ^{x}_{0} \frac{1}{1+\sin ^{2}t}  \, dt=\frac{1}{1+\sin ^{2}x}
$$
This can be combined with the [[Chain Rule|chain rule]] for more complicated expressions. For example:
$$
\frac{d }{dx} \int _{0}^{x^{2}} \frac{1}{1+e^{t}} \, dt
$$
Letting $u=x^{2}$,
$$
\frac{d }{dx} \int _{0}^{u} \frac{1}{1+e^{t}} \, dt=\left( \frac{d }{du} \int _{0}^{u} \frac{1}{1+e^{ t} } \, dt  \right)\left( \frac{d u}{dx}  \right)
$$
$$
= \frac{1}{1+e^{u}}2x=\frac{2x}{1+e^{x^{2}}}
$$

