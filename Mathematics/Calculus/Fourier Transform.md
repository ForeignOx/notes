The Fourier Transform is a tool that does “[[Frequency|frequency]] analysis” similar to [[Fourier Series|fourier series]], but for non-[[Periodic Functions|periodic]] [[Functions|functions]]
If we consider a fourier series of a function of periodicity $2\pi M$, for $M\in\mathbb{N}$
![[Fourier Transform 2025-03-11 14.18.25.excalidraw]]
Then this has a fourier series:
$$
f(x)=\frac{a_{0}}{2}+{\sum_{n=1}^{\infty}}a_{n}\cos\left( \frac{nx}{M} \right)+\sum_{n=1}^{\infty}b_{n}\sin\left( \frac{nx}{M} \right)=\sum_{n=-\infty}^{\infty}d_{n}e^{ inx/M }
$$
Which needs angular frequencies $\frac{1}{M},\frac{2}{M},\frac{3}{M},\dots$
As $M\to \infty$, the function becomes non-periodic, but we need all angular frequencies to describe it, so the equation becomes:
$$
f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde{f}(p)  e^{ ipx } \, dp 
$$
Which is the Fourier transform
___
Let $f(x)$ be a (non)-periodic function on $\mathbb{R}$:
![[Fourier Transform 2025-03-11 14.31.17.excalidraw]]
For each integer $M>0$, construct a function $f_{M}(x)$ or periodicity $2\pi M$ as follows, $f_{M}(x)=f(x)$ for $-\pi M\leq x\leq \pi M$, $f_{M}(x+2\pi M)=f_{M}(x)$, so we can construct the fourer series as follows:
$$
f_{M}(x)=\sum_{n=-\infty}^{\infty}d_{n}e^{ inx/M }
$$
Where
$$
d_{n}=\frac{1}{2\pi M}\int_{-\pi M}^{\pi M} f_{M}(x)e^{ -inx/M } \, dx =\frac{1}{2\pi M}\int_{-\pi M}^{\pi M} f(x)e^{ -inx/M } \, dx 
$$
But $d_{n}$ is not a good thing to use, since the label $n$ is no longer the same as the angular frequency $\frac{n}{M}$, and $d_{n}\to0$ as $M\to \infty$ as it is roughly proportional to $\frac{1}{M}$
Instead we will define
$$
\tilde{f}\left( \frac{n}{M} \right)=d_{n}2\pi M=\int_{-\pi M}^{\pi M} f(x)e^{ -inx/M } \, dx 
$$
So the Fourier series becomes:
$$
f_{M}(x)=\sum_{n=-\infty}^{\infty}d_{n}e^{ inx/M }=\sum_{n=-\infty}^{\infty} \frac{1}{2\pi M}\tilde{f}\left( \frac{n}{M} \right)e^{ inx/M }=\frac{1}{2\pi}\sum_{n=-\infty}^{\infty}\Delta p\tilde{f}(p)e^{ ipx }
$$
Where $p=\frac{n}{M},\Delta p=\frac{1}{M}$, and $\Delta p$ is the difference between neighbouring values of angular frequency in series
We can represent this graphically:
![[Fourier Transform 2025-03-11 14.43.11.excalidraw]]
In the limit as $M\to \infty,\Delta p\to  0$ and the [[Riemann Sum|riemann sum]] of the rectangles tends to an [[Integration|integral]], so
$$
f_{M}(x)\to f(x)=\frac{1}{2\pi}\int_{-\infty}^{\infty} \tilde{f}(p)e^{ ipx } \, dx 
$$
Where
$$
\tilde{f}(p)=\int_{-\infty}^{\infty} f(x)e^{ -ipx } \, dx
$$
Note that $\tilde{f}(p)$ is the fourier transform of $f(x)$
## Example
Find the Fourier transform of
$$
F(x)=\begin{cases}
1 & \left| x \right| <1\\0 & \text{otherwise}
\end{cases}
$$
![[Fourier Transform 2025-03-11 14.49.37.excalidraw]]
$$
\tilde{F}(p)=\int_{-\infty}^{\infty} F(x)e^{ -ipx } \, dx =\int_{-1}^{1} e^{ -ipx } \, dx=\left[ \frac{e^{ -ipx }}{-ip} \right]_{-1}^{1}=\frac{2(e^{ ip }-e^{ -ip })}{2ip}=\frac{2\sin(p)}{p} 
$$
Which looks like:
![[Fourier Transform 2025-03-11 14.52.10.excalidraw]]