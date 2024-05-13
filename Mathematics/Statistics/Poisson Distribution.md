## Probability Density Function
The poisson distribution is a probability distribution. 
If you take a family of [[Binomial Distribution|binomial distributions]] with a set value of $np$, as $n\rightarrow \infty$ the probabilities seem to converge.
$$
X \sim \lim_{ n \to \infty }\left( B\left( n,\frac{\lambda}{n} \right) \right)
$$
$$
\implies P(X=r)=\lim_{ n \to \infty } \left( ^nC_{r}\left( \frac{\lambda}{n} \right)^r\left( 1- \frac{\lambda}{n}  \right)^{n-r} \right)
$$
$$
=\lim_{ n \to \infty } \left( \frac{n!}{r!(n-r!)}\left( \lambda^r\left( \frac{1}{n} \right)^r \right) \left( 1- \frac{\lambda}{n} \right)^n\left( \frac{1}{1- \frac{\lambda}{n}} \right)^r\right)
$$
$$
=\frac{\lambda^r}{r!}\lim_{ n \to \infty } \left( \frac{n!}{(n-r)!}\left( \frac{1}{n} \right)^r\left( \frac{1}{n-\frac{\lambda}{n}} \right)^r\left( 1- \frac{\lambda}{n} \right)^n \right)
$$
$$
=\frac{\lambda^r}{r!}\lim_{ n \to \infty }\left( \frac{n!}{(n-r)!}\left( \frac{1}{n-\lambda} \right)^r\left( 1- \frac{\lambda}{n} \right)^n \right) 
$$
$$
=\frac{\lambda^r}{r!}\lim_{ n \to \infty }\left( \frac{n(n-1)(n-2)\dots(n-r+1)}{(n-\lambda)^r}\left( 1-\frac{\lambda}{n} \right)^n \right) 
$$
We know:
$$
\lim_{ n \to \infty }\left(\frac{n(n-1)(n-2)\dots(n-r+1)}{(n-\lambda)^r}\right)=1 
$$
and:
$$
\lim_{ n \to \infty }\left(\left( 1-\frac{\lambda}{n} \right)^n\right)=e^{-\lambda} 
$$
Hence,
$$
P(X=r)=\frac{e^{-\lambda}\lambda^r}{r!}
$$

We write this in the following way:
$$
X \sim Po(\lambda)\iff P(X=r)=\frac{e^{-\lambda}\lambda^r}{r!}
$$

___
## Shape of the distribution

```tikz
\usepackage{pgfplots}
\pgfmathdeclarefunction{poiss}{1}{%
  \pgfmathparse{(#1^x)*exp(-#1)/(x!)}%
  }
\begin{document}
        \begin{tikzpicture}
            \begin{axis}[
              axis x line=center,
              axis y line=center,
              xtick={0,2,...,19},
              ytick={0.1,0.2,...,0.4},
                domain = 0:18,
                samples = 19,
                xlabel={$k$},
                ylabel={$P[k]$},
                xlabel style={right},
                ylabel style={above left},
                ymax=0.5,
                xmax=20,
                x post scale=1.4
                ]
                \addplot+[ycomb,blue,thick] {poiss(1))};
                \addlegendentry{$\lambda = 1$}
                \addplot+[ycomb,red,thick] {poiss(5))};
                 \addlegendentry{$\lambda = 5$}
                \addplot+[ycomb,brown,thick] {poiss(9))};
                 \addlegendentry{$\lambda = 9$};
            \end{axis}
        \end{tikzpicture}
\end{document}
```
The distribution is skewed, but with larger values of $\lambda$, it becomes more symmetrical.
___
## Probability Distribution Properties
For this to be a probability distribution, the probabilities must sum to 1:
$$
\sum_{r=0}^\infty P(X=r)=\sum_{r=0}^\infty \frac{e^{-\lambda}\lambda^r}{r!}=e^{-\lambda}\sum_{r=0}^\infty \frac{\lambda^r}{r!}
$$
$$
=e^{-\lambda}\left( 1+\lambda+\frac{\lambda^{2}}{2}+\frac{\lambda^{3}}{3}+\dots \right)
$$
From the [[Maclaurin series]]:
$$
1+\lambda+\frac{\lambda^{2}}{2}+\frac{\lambda^{3}}{3}+\dots=e^{\lambda}
$$
Hence,
$$
\sum_{r=0}^\infty P(X=r)=e^{-\lambda}e^\lambda=1
$$
So the probabilities do indeed sum to 1.
___
## Expectation
Find $E(X)$:
$$
E(X)=\sum_{r=0}^\infty\left( r\left( \frac{e^{-\lambda}\lambda^r}{r!} \right) \right)=e^{-\lambda}\sum_{r=1}^\infty\left( \frac{\lambda^r}{(r-1)!} \right) 
$$
$$
=e^{-\lambda}\lambda \sum_{r=1}^\infty\frac{\lambda^{r-1}}{(r-1)!} =e^{-\lambda}e^\lambda\lambda=\lambda
$$
Therefore $E(X)=\lambda$
___
## Variance
Find $Var(X)$:
$$
E(X^{2})-E(X)=E(X(X-1))=\sum_{r=0}^\infty\left( r(r-1) \frac{e^{-\lambda}\lambda^r}{r!} \right)
$$
$$
=e^{-\lambda}\sum_{r=2}^\infty \frac{\lambda^{r}}{(r-2)!}=\lambda^2e^{-\lambda}\sum_{r=2}^\infty \frac{\lambda^{r-2}}{(r-2)!}=\lambda^{2}e^{-\lambda}e^\lambda=\lambda^{2}
$$
$$
\implies E(X^{2})=\lambda^{2}+\lambda
$$
Hence,
$$
Var(X)=E(X^{2})-E(X)^{2}=\lambda^{2}+\lambda-\lambda^{2}=\lambda
$$
Therefore $Var(X)=\lambda$
___
## Requirements
Requirements for a variable to be represented by the poisson distribution:
* The event will happen singly (one at a time)
* The event will happen [[Independence|independently]]
* The event occurs at a constant average rate $\lambda$
An indication that data may be modelled well by a poisson distribution is in $\lambda \approx E(X)\approx Var(X)$
___
## Modal Value
Consider a variable $X\sim Po(\lambda)$, by considering $\frac{P(X=r+1)}{P(X=r)}$, find the modal value for this distribution.
$$
\frac{P(X=r+1)}{P(X=r)}=\frac{\left( \frac{e^{-\lambda}\lambda^{r+1}}{(r+1)!} \right)}{\frac{e^{-\lambda}\lambda^r}{r!}}=\frac{\lambda}{r+1}
$$
This is $\geq1$ for $r=\lambda-1$, and $\leq 1$ for $r=\lambda$ , so hence we can find the mode. 
___
## X+Y
Let $X \sim Po(\lambda)$ and $Y \sim Po(\mu)$ be two independent random variables, we want to investigate the distribution of $X+Y$. 
We know $E(X+Y)=E(X)+E(Y)=\lambda+\mu$. 
We also know $Var(X+Y)=Var(X)+Var(Y)=\lambda+\mu$.
Conjecture: $X+Y \sim Po(\lambda+\mu)$
$$
P(X+Y=r)=P(X=r)P(Y=0)+P(X=r-1)P(Y=1)+\dots+P(X=0)P(Y=r)
$$
$$
=\sum_{k=0}^rP(X=r-k)P(Y=k)=\sum_{k=0}^r \frac{e^{-\lambda}\lambda^{r-k}}{(r-k)!} \frac{e^{-\mu}\mu^k}{k!}
$$
$$
e^{\lambda+\mu} \sum_{k=0}^r \frac{1}{k!(r-k)!}\lambda^{r-k}\mu^k=\frac{e^{\lambda+\mu}}{r!}\sum_{k=0}^r \frac{r!}{k!(r-k)!}\lambda^{r-k}\mu^r
$$
We know $\frac{r!}{k!(r-k)!}$is $^rC_{k}$, we can use binomial expansion to show:
$$
P(X+Y=r)=\frac{e^{\lambda+\mu}(\lambda+\mu)^r}{r!}
$$
so  $X+Y\sim Po(X+Y)$ as expected.
___
## Similarity to binomial
```tikz
\usepackage{pgfplots}
\pgfmathdeclarefunction{poiss}{1}{%
  \pgfmathparse{(#1^x)*exp(-#1)/(x!)}%
  }


\begin{document}
        \begin{tikzpicture}[
declare function={binom(\k,\n,\p)=\n!/(\k!*(\n-\k)!)*\p^\k*(1-\p)^(\n-\k);}
]
            \begin{axis}[
              axis x line=center,
              axis y line=center,
              xtick={0,10,...,100},
              ytick={0.05,0.1,...,1},
                domain = 0:100,
                samples = 20,
                xlabel={$k$},
                ylabel={$P[k]$},
                xlabel style={right},
                ylabel style={above left},
                ymax=1,
                xmax=110,
                ]
                \addplot+[ycomb,blue,thick] {poiss(50))};
                \addlegendentry{$\lambda = 1$}
                
\addplot [only marks, cyan] {binom(x,500,0.1)}; \addlegendentry{$p=0.1$}
            \end{axis}
        \end{tikzpicture}
\end{document}
```
$X\sim B(n,p)$ can be approximated with $Y\sim Po(np)$, since $Var(Y)=np$ and $Var(X)=np(1-p)$, so the approximation is better the smaller the value of $p$

