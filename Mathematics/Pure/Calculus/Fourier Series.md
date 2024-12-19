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
$$
 \frac{1}{L}\int _{-L}^{L} \cos\left( \frac{n\pi x}{L} \right)\cos\left( \frac{m\pi x}{L} \right) \, dx =\delta_{mn}
$$
$$
\frac{1}{L}\int _{-L}^{L}\sin\left( \frac{n\pi x}{L} \right)\sin\left( \frac{m\pi x}{L} \right) \, dx =\delta_{mn}
$$
### Proof
For the first:
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{1}{L}\left[ \frac{L}{n\pi}\sin\left( \frac{n\pi x}{L} \right) \right]_{-L}^{L}=0
$$
For the second and third, these are immediate as they are integrals of [[Odd Functions|odd functions]] over symmetric intervals
For the fourth, recall $\cos(x\pm y)=\cos(x)\cos(y)\mp \sin(x)\sin(y)$, which can be used to obtain $\cos(x+y)+\cos(x-y)=2\cos(x)\cos(y)$
Then, first assuming $m\neq n$,
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{m\pi x}{L} \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{1}{L}\int _{-L}^{L} \cos\left( \frac{(m+n)\pi x}{L} \right)+\cos\left( \frac{(m-n)\pi x}{L} \right)\, dx 
$$
$$
= \frac{1}{2L}\left[ \frac{L}{(m+n)\pi}\sin\left( \frac{(m+n)\pi x}{L} \right)+\frac{L}{(m-n)\pi}\sin\left( \frac{(m-n)\pi x}{L} \right) \right]_{-L}^{L}=0
$$
If $m=n$,
$$
\frac{1}{L}\int _{-L}^{L}\cos\left( \frac{m\pi x}{L} \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =\frac{1}{L}\int _{-L}^{L}\cos ^{2}\left( \frac{n\pi x}{L} \right) \, dx
$$
$$
= \frac{1}{2L}\int _{-L}^{L}1+\cos\left( \frac{2n\pi x}{L} \right) \, dx =\frac{1}{2L}\left[ x+\frac{L}{2n\pi}\sin\left( \frac{2n\pi x}{L} \right) \right]^{L}_{-L}=\frac{1}{2L}(L--L)=1 
$$
For the fifth, the method is similar to above (pls do here)

In general if $f(x)$ is even on $(-L,L)$, then all $b_{n}=0$ and the Fourier series contains only $\cos$ terms (plus a constant term) we call such a series a cosine series
## Fourier Coefficients
We say that the [[sets|set]] of functions $\left\{  1,\cos\left( \frac{n\pi x}{L} \right),\sin\left( \frac{n\pi x}{L} \right)  \right\}$ form an orthogonal (or orthonormal) set on $[-L,L]$, because if $\phi,\psi$ are different elements of the set, then 
$$
\frac{1}{L}\int _{-L}^{L}\phi \psi \, dx =0
$$
We can now use these identities to determine the Fourier Coefficients, firstly by integrating the original series:
$$
\frac{1}{L}\int _{-L}^{L}f(x) \, dx =\frac{1}{L}\int _{-L}^{L} \frac{a_{0}}{2}+\sum_{n=1}^{\infty} \left[ a_{n}\cos \left( \frac{n\pi x}{L} \right)+b_{n}\sin\left( \frac{n\pi x}{L} \right) \right]  \, dx 
$$
$$
= \frac{1}{L}\left[ \frac{a_{0}x}{2} \right]_{-L}^{L}=a_{0}
$$
By idendities $\hspace{0pt}1$ and $\hspace{0pt}2$, therefore:
$$
a_{0}=\frac{1}{L}\int_{-L}^{L}f(x)  \, dx 
$$
Or $a_{0}=<1,f(x)>$ where $<f,g> =\frac{1}{L}\int _{-L}^{L}fg \, dx$
Now letting $m$ be a positive integer, and multiplying the fourier series by $\cos\left( \frac{m\pi x}{L} \right)$ and integrating,
$$
\frac{1}{L}\int _{-L}^{L}f(x)\cos\left( \frac{m\pi x}{L} \right) \, dx 
$$
$$
 =\frac{1}{L}\int _{-L}^{L} \left( \frac{a_{0}}{2}+\sum_{n=1}^{\infty}\left( a_{n}\cos\left( \frac{n\pi x}{L} \right) \right)+b_{n} \sin\left( \frac{n\pi x}{L} \right)  \right)\cos\left( \frac{n\pi x}{L} \right) \, dx =\sum_{n=1}^{\infty} a_{n}\delta_{mn}=a_{m} 
$$
By identities $1,3,4$, so
$$
a_{n}=\frac{1}{L}\int _{-L}^{L}f(x)\cos\left( \frac{n\pi x}{L} \right) \, dx 
$$
Or $a_{n}= <f,\cos\left( \frac{n\pi x}{L} \right)>$
Note htat with $n=0$, this also gives the correct expression for $a_{0}$
Similarly multiplying the fourier series by $\sin\left( \frac{m\pi x}{L} \right)$ and integrating gives
$$
\frac{1}{L}\int _{-L}^{L}f(x)\sin\left( \frac{m\pi x}{L} \right) \, dx=\frac{1}{L}\int _{-L}^{L}\left( \frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{n\pi x}{L} \right) +b_{n}\sin\left( \frac{n\pi x}{L} \right)\right) \, dx 
$$
pls finish :)

## Examples
The function $f(x)$ has period $\hspace{0pt}2$ i.e. $f(x+2)=f(x)$ and is given by $f(x)=|x|$ for $-1<x<1$, so looks like:
![[Fourier Series 2024-12-10 14.40.53.excalidraw]]
To calculate the Fourier series of $f(x)$, we compute the Fourier coefficients using our previous results with $L=1$
$$
a_{0}=\int _{-1}^{1}f(x) \, dx =\int _{-1}^{1}\left| x \right|  \, dx =2\int _{0}^{1}x \, dx =[x^{2}]_{0}^{1}=1
$$
For $n>0$:
$$
a_{n}=\int _{-1}^{1}f(x)\cos(n\pi x) \, dx =\int _{-1}^{1}\left| x \right| \cos(n\pi x) \, dx 
$$
$$
= 2\int _{0}^{1}x\cos(n\pi x) \, dx =2\left( \underbrace{ \left[ \frac{1}{n\pi}\sin(n\pi x) \right]_{0}^{1} }_{ =0 }-\int _{0}^{1} \frac{1}{n\pi}\sin (n\pi x) \, dx  \right)
$$
$$
= \frac{2}{n^{2}\pi^{2}}[\cos(n\pi x)]_{0}^{1}=\frac{2}{n^{2}\pi^{2}}(\cos(n\pi)-1=\frac{2}{n^{2}\pi^{2}}((-1)^{n}-1)
$$
$$
b_{n}=\int _{-1}^{1}\left| x \right| \sin(n\pi x) \, dx =0
$$
Since this is the integral of an odd function over a symmetric interval
Putting the above together, we have the Fourier cosine series for $f(x)$
$$
f(x)=\frac{a_{0}}{2}+\sum_{n=1}^{\infty} a_{n}\cos\left( \frac{n\pi x}{L} \right)+b_{n}\left( \frac{n\pi x}{L} \right) 
$$
$$
\implies \left| x \right| =\frac{1}{2}+\sum_{n=1}^{\infty} \frac{2((-1)-1)}{n^{2}\pi^{2}}\cos(n\pi x)
$$
$$
= \frac{1}{2}-\frac{4}{\pi^{2}}\left( \cos(\pi x)+\frac{1}{9}\cos(3\pi x)+\dots \right)
$$
Note that in this example $a_{2n}=0$, and $a_{2n-1}=-\frac{4}{(2n+1)^{2}\pi^{2}}$
So we can also write the Fourier series as:
$$
f(x)=
$$


#Mathematics #Calculus 