![[Differentiation From First Principles 2024-03-14 22.58.05.excalidraw]]
Geometrically the derivative of a [[Functions|function]] $f'(a)$ (or $\frac{df}{dx}(a)$ or $\frac{df}{dx}|_{x=a}$) is equal to the slope of the unique non-vertical tangent to the graph of $f$ at $x=a$ if it exists
This is naturally defined as the [[Limit|limit]] of the slope of a line segment joining two nearby points on the graph of $f$, i.e. at a point $(a,f(a))$, the nearby point will be $(a+h,f(a+h))$, so we use the gradient of a line equation to find the tangent like so:
$$
\frac{f(a+h)-f(a)}{a+h-a}=\frac{f(a+h)-f(a)}{h}
$$
By taking $h$ to be as small as possible, i.e. the limit as $h$ tends to 0, we will get the tangent, hence:
$$
f'(x)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}
$$
If the limit exists, we say $f$ is differentiable at $x=a$
If $f'(a)$ exists for all $a\in \text{Dom}f$, we say that $f$ is differentiable and the function $f'(x)$ is called the derivative
## Example
With $f(x)=x^{2}$, calculate $f'(a)$ using the limit definition:
$$
f'(a)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}=\lim_{ h \to 0 } \frac{(a+h)^{2}-a^{2}}{h}=\lim_{ h \to 0 } \frac{2ah+h^{2}}{h}=\lim_{ h \to 0 } 2a+h=2a
$$
___
Calculate the deribative of $f(x)=\sin x$
$$
f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}=\lim_{ h \to 0 } \frac{\sin(x+h)-\sin x}{h}=\lim_{ h \to 0 } \frac{\sin x\cos h+\cos x\sin h-\sin x}{h}
$$
$$
= \lim_{ h \to 0 } \left( \sin x\left( \frac{\cos h-1}{h} \right)+\cos x\left( \frac{\sin h}{h} \right) \right)=\cos x
$$

#Mathematics #Calculus