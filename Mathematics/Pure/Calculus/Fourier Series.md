You can approximate [[Periodic Functions|periodic]] [[Functions|functions]] using trigonometric functions such as $\sin$ and $\cos$ using the following method
Consider a function $f(x)$ of period $2L$ ($f(x+2L)=f(x)$) given on the interval $(-L,L)$ The functions $\cos\left( \frac{n\pi x}{L} \right),\sin\left( \frac{n\pi x}{L} \right)$, for $n\in\mathbb{N}$ are also periodic with period $2L$, so we can try to write $f(x)$ in terms of these functions
Since any constant is periodic (for any period), we can include a constant term
We therefore aim to express $f(x)$ as:
$$
f(x)=\frac{a_{0}}{2}+\sum_{ n=1} ^{\infty}  \left( a_{n}\cos\left( \frac{n\pi x}{L} \right)+b_{n}\sin\left( \frac{n\pi x}{L} \right) \right)
$$
where $a_{0},a_{n},b_{n}$ are constants labelled by the positive integer $n$, and are called the Fourier coefficients of $f(x)$
If the constants are such that the series converges, then it is called the Fourier Series of $f(x)$
## Example
$$
f(x)=2\cos ^{2}\left( \frac{\pi x}{L} \right)+3\sin\left( \frac{\pi x}{L} \right)
$$
Has period $2L$
Since $\cos(2x)=2\cos ^{2}x-1$,
$$
f(x)=1+\cos\left( \frac{2\pi x}{L} \right)+3\sin\left( \frac{\pi x}{L} \right)
$$
Is theFourier Series of $f(x)$ containing only a finite number of terms with $a_{0}=2$, $a_{2}=1$, $b_{1}=3$, and all the other coefficients are $\hspace{0pt}0$
In general, an infinite number of coefficients may be non-zero, so we need a method to find them for a given $f(x)$
## Identities :)
Let $m$ and $n$ be positive integers, then:
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{n\pi x}{L} \right) \, dx =0
$$
$$
\frac{1}{L}\int _{-L}^{L}\sin\left( \frac{n\pi x}{L} \right) \, dx =0
$$
$$
\frac{1}{L}\int _{-L}^{L} \sin\left( \frac{n\pi x}{L} \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =0
$$
$$
 \frac{1}{L}\int _{-L}^{L} \cos\left( \frac{n\pi x}{L} \right)\cos\left( \frac{m\pi x}{L} \right) \, dx =\begin{cases}
0&\text{if }m\neq n\\1&\text{if }m=n
\end{cases}
$$
$$
\frac{1}{L}\int _{-L}^{L}\sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{m\pi x}{L} \right) \, dx =\begin{cases}
0&\text{if }m\neq n\\1&\text{if }m=n
\end{cases}
$$
It is convenient to use the [[Kronecker Delta Function|Kronecker Delta function]] to rewrite the last two:


## Fourier Coefficients



