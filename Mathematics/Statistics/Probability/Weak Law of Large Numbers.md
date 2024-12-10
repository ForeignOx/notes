Idea: if we consider a sample of size $n$, $X_{1},X_{2},\dots,X_{n}$, then the sample mean:
$$
\overline{X}_{n}=\frac{1}{n}\sum_{ i=1} ^{ n}X_{i}
$$
Then $\overline{X}_{n}$ converges to [[E(X)|E(X)]]
___
Theorem:
Let $X_{1},X_{2},\dots$ be an [[Independence|independent]] sequence of [[Random Variables|random variables]], with [[E(X)|$E(X_{i})=\mu$]] and [[Var(X)|$Var(X_{i})=\sigma^{2}$]] for all $i\geq 1$, 
Let $\overline{X}_{n}=\frac{1}{n}\sum_{i=1}^{n}X_{i}$, then for any $\epsilon>0$, the sequence will converge in probability, i.e.
$$
\lim_{ n \to \infty } \mathbb{P}(| \overline{X}_{n}-\mu|>\epsilon)=0
$$
In the most general case, we need not know $\sigma^{2}$, here in our case, we wanted to use Chebyshev's inequality and hence we needed it, this is known as the advances Kolmogorov Law of Large Numbers
## Example
Let $X$ denote the number of heads in $n$ tosses of coin with probability of success $p$
$$
X\sim Bin(n,p)
$$
$$
 E(X)=np,Var(X)=np(1-p)
$$
Define $B_{n}=\frac{1}{n}X$, 
$$
E(B_{n})=E\left( \frac{1}{n}X \right)=\frac{1}{n}E(X)
$$
$$
Var(B_{n})=\frac{1}{n^{2}}Var(X)
$$
Now we can apply Chebyshev's inequality, for any $\epsilon>0$, 
$$
\mathbb{P}(|B_{n}-E(B_{n})|>\epsilon)=\mathbb{P}(|B_{n}-p|>\epsilon)\leq \frac{1}{\epsilon^{2}}Var(B_{n})=\frac{p(1-p)}{\epsilon^{2}n}\to 0
$$
As $n\to \infty$
So $B_{n}$ will be very cose to $p$ with a very high probablity
## Proof
$$
E(\overline{X}_{n})=\frac{1}{n}\sum_{ i=1} ^{ n}E(X_{i})=\frac{1}{n}\times n \mu=\mu
$$
$$
Var( \overline{X}_{n})=\frac{1}{n^{2}}\left( \sum_{ i=1} ^{ n}  Var(X_{i})+2\underbrace{ \sum_{ i<j} ^{ n} Cov(X_{i},X_{j}) }_{ =0\text{ (independent)} }  \right)
$$
$$
= \frac{1}{n^{2}}\sum_{ i=1} ^{ n}  Var(X_{i})=\frac{1}{n^{2}}\times n\sigma^{2}=\frac{\sigma^{2}}{n}
$$
Now apply Chebyshev's inequality to get $\forall\epsilon>0$,
$$
\mathbb{P}(| \overline{X}_{n}-E(\overline{X}_{n})|>0)=\mathbb{P}(\left| \overline{X}_{n}-\mu \right|>\epsilon )\leq \frac{1}{\epsilon^{2}}Var(\overline{X}_{n})=\frac{\sigma^{2}}{\epsilon^{2}n}
$$
Equivalently
$$
\lim_{ n \to \infty } \mathbb{P}(\left| \overline{X}_{n}-\mu \right| \leq\epsilon)=1
$$
$$
\implies \mathbb{P}(\left| X_{n}-\mu \right|>\epsilon )=1-\mathbb{P}(\left| \overline{X}_{n}-u \right|\leq\epsilon)
$$
## Example
Let us collect a sample of size $n$ of heights of individuals, let $H_{i}$ denote the height of the $i$th individual
Suppose we know that $E(H_{i})=\mu$
Suppose we know that $E(H_{i})=\mu$ and $Var(H_{i})=\sigma^{2}$. Then if $\overline{X}_{n}=\frac{1}{n}\sum_{ i=1} ^{ n} H_{i}$, then $\forall\epsilon>0$, $\mathbb{P}(\left| \overline{X}_{n}-\mu \right|>\epsilon)\to 0$ as $n\to \infty$, that is, with high probability that $\overline{X}_{n}$ is very close to $\mu$