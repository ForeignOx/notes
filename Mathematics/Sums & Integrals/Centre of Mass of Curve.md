For a uniform lamina enclosed by $y-f(x)$ on $x \in[a,b]$, the CoM is given by:
$$
\bar{x}=\frac{\int ^a_{b}xf(x) \, dx}{\int ^{a}_{b}f(x) \, dx }
$$
$$
\bar{y}=\frac{ \int ^{a}_{b}(f(x))^{2} \, dx  }{2\int ^{a}_{b}f(x) \, dx }
$$
## Proof
![[Centre of Mass of Curve 2024-02-16 12.54.38.excalidraw]]
$\bar{x}$: Element 'moment' from y-axis
$$
=x f(x)\delta x
$$
Sum and let $\delta x\to0$:
$$
\bar{x}\int ^{b}_{a}f(x) \, dx =\int ^{b}_{a}xf(x) \, dx 
$$
$\bar{y}$: Element moment from x-axis (mass half way up function)
$$
=\frac{1}{2}f(x)f(x)\delta x
$$
Sum and let $\delta x\to 0$:
$$
\bar{y}\int ^{b}_{a}f(x) \, dx=\int ^{b}_{a}\frac{1}{2}(f(x))^{2} \, dx 
$$
## Example
Find the CoM of a uniformly dense cone
![[Centre of Mass of Curve 2024-02-16 14.16.14.excalidraw]]
CoM is at $(\bar{x},0,0)$, total volume $=\frac{1}{3}\pi r^{2}h$
Each element 'moment' $=x\pi\left( \frac{r}{h}x \right)^{2}\delta x=\frac{r^{2}\pi}{h^{2}}x^{3}\delta x$
$$
\implies \frac{1}{3}\pi r^{2}h \bar{x}=\int_{0}^{h} \frac{r^{2}\pi}{h}x^{3} \, dx=\frac{r^{2}\pi}{h^{2}}\left[ \frac{1}{4}x^{4} \right]^{h}_{0}=\frac{1}{4}\pi r^{2}h^{2} 
$$
$$
\implies \bar{x}=\frac{3}{4}h
$$
#Mathematics 