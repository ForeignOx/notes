A [[Series|series]] $\sum_{k=1}^{\infty} a_{k}$ is called alternating, if $a_{2k}\geq 0$ and $a_{2k+1}\leq 0$  or if $a_{2k}\leq 0$ and $a_{2k+1}\geq 0$ for all $k\in\mathbb{N}$
## Alternating Sign Test
Let $(a_{k})_{k\in\mathbb{N}}$ be a monotonically decreasing [[Sequences|sequence]] (cannot be alternating) of positive numbers, with $\lim_{ k \to \infty }a_{k}=0$, then the alternating series:
$$
\sum_{ k=1} ^{ n}(-1)^{k+1}a_{k}
$$
Then this alternating
For the squence of partial sums $(s_{n})n\in\mathbb{N}$ 
$$
s_{2}\leq s_{n}\leq\dots \leq s_{2n}\leq\dots \leq \sum_{ k=1} ^{\infty}  (-1)^{k+1}a_{k}\leq\dots \leq s_{2n-1}\leq\dots \leq s_{3}\leq s_{1}
$$
and:
$$
\left|s_{n}-\sum_{ k=1} ^{\infty}  (-1)^{k+1}a_{k}\right|\leq a_{n+1}
$$
## Proof
Since the $a_{k}$ are monotonically decreasing, we hve $a_{k}-a_{k+1}\geq 0$. Hence, 
$$
s_{2n+2}=s_{2n}+a_{2n+1}-a_{2n+2}\leq s_{2n}
$$
Similalarly:
$$
s_{2n+1}=s_{2n-1}-a_{2n}+a_{2n+1}\leq s_{2n-1}
$$
So $(s_{2n})_{n\in\mathbb{N}}$ is monotonically increeasing, and the even terms are monotonically decreasing, so we get $s_{2}\leq s_{2n}\leq s_{2n-1}\leq s_{1}$, so sequences are bounded, hence convergent
Write
$$
s ^{e}=\lim_{ n \to \infty } s_{2n}
$$
Note $s_{2n}=s_{2n-1}-a_{2n}$, that is $a_{2n}=s_{2n-1}-s_{2n}$, by colt