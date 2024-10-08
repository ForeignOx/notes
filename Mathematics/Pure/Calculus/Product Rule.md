Consider a function $h(x)=f(x)g(x)$, such that $f(x)$ and $g(x)$ are differentiable at $x$, by [[Differentiation From First Principles|first principles]]:
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


#Mathematics