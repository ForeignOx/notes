If $f(x)$ and $g(x)$ are both [[Differentiation|differentiable]] [[Functions|functions]], that are differentiable $n$ times, then so is the product $(fg)(x)$
Denote this function$h(x)=f(x)g(x)$:
$$
h'(x)=\lim_{ \delta x \to 0 } \frac{h(x+\delta x)-h(x)}{\delta x}
$$
$$
=\lim_{ \delta x \to 0 } \frac{f(x+\delta x)g(x+\delta x)-f(x)g(x)}{\delta x}
$$
$$
=\lim_{ \delta x \to 0 } \frac{f(x+\delta x)g(x+\delta x)-f(x)g(x+\delta x)+f(x)g(x+\delta x)-f(x)g(x)}{\delta x}
$$
$$
=\lim_{ \delta x \to 0} \frac{(f(x+\delta x)-f(x))g(x+\delta x)+f(x)(g(x+\delta x)-g(x)))}{\delta x}
$$
$$
=\lim_{ \delta x \to 0 } \frac{g(x+\delta x)(f(x+\delta x)-f(x))}{\delta x}+\lim_{ \delta x \to 0 } \frac{f(x)(g(x+\delta x)-g(x))}{\delta x}
$$
$$
=(\lim_{ h \to 0 } g(x+\delta x))\left( \lim_{ \delta x \to 0 } \frac{f(x+\delta x)-f(x)}{\delta x} \right)+(\lim_{ \delta x \to 0 } f(x))\left( \lim_{ \delta x \to 0 } \frac{g(x+\delta x)-g(x)}{\delta x} \right)
$$
$$
g(x)f'(x)+f(x)g'(x)
$$
Hence:
$$
\frac{d }{dx} f(x)g(x)=g(x)f'(x)+f(x)g'(x) 
$$
Another way of writing this is:
$$
D(fg)=(Df)g+f(Dg)
$$
Then this can be applied again for the second derivative:
$$
D^{2}(fg)=(D^{2}f)g+(Df)(Dg)+(Df)(Dg)+f(D^{2}g)=(D^{2}f)g+2(Df)(Dg)+f(D^{2}g)
$$
This looks a lot like the [[Binomial Theorem|binomial expansion]], and we can in fact expand upon this and say:
$$
D^{n}(fg)=\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}(D^{k}f)(D^{n-k}g)  
$$
## Examples
Calculate $D^{3}(x^{2}\sin x)$, we know:
$$
D^{3}(fg)=(D^{3}f)g+3(D^{2}f)(Dg)+3(Df)(D^{2}g)+f(D^{3}g)
$$
Letting $f(x)=x^{2}$, $Df=2x$, $D^{2}f=2$, $D^{3}f=0$, $g(x)=\sin x$, $Dg=\cos x$, $D^{2}g=-\sin x$, $D^{3}g=-\cos x$, so:
$$
D^{3}(x^{2}\sin x)=3(2)\cos x+3(2x)(-\sin x)+x^{2}(-\cos x)=(6-x^{2})\cos x=6x\sin x
$$




#Mathematics #Calculus 