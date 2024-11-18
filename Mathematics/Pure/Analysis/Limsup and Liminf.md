Given a [[Boundedness|bounded]] [[Sequences|sequence]] $(x_{n})_{n\in\mathbb{N}}$ define two related sequences (note these are not necessarily [[Subsequences|subsequences]]) $(\overline{x_{n}})_{n\in\mathbb{N}}$ and $(\underline{x_{n}})_{n\in\mathbb{N}}$ related to [[Supremum and Infimum|supremum and infimum]] as follows:
$$
\overline{x_{n}}=\text{sup}\{ x_{m} \in \mathbb{R}\mid m\geq n \}
$$
$$
\underline{x_{n}}=\text{inf}\{ x_{m}\in \mathbb{R} \mid m\geq n\}
$$
## Lemma
Let $(x_{n})_{n\in\mathbb{N}}$ be a bounded sequence, then $(\overline{x_{n}})_{n\in\mathbb{N}}$ is monotonically decreasing and bounded, and $(\underline{x_{n}})_{n\in\mathbb{N}}$ is monotonically increasing and bounded. Furthermore:
$$
\lim_{ n \to \infty } \underline{x_{n}}\leq \lim_{ n \to \infty } \overline{x_{n}}
$$
### Proof
$(x_{n})_{n\in\mathbb{N}}$ is bounded, so there exists $c\in\mathbb{R}^{+}$, with $-c\leq x_{n}\leq c$ for all $n\in\mathbb{N}$, we define:
$$
X_{n}=\{ x_{m}\in \mathbb{R}\mid m\geq n \}\subseteq[-c,c]
$$
This is a bounded, non-empty set. Infimum and supremum exist, and
$$
-c\leq  \underline{x_{n}}\leq\overline{x_{n}}\leq c
$$
So both sequences are bounded
Note $X_{n+1}\subset X_{n}$, as we are decreasing the number of candidates from the definition, so $\overline{x_{n}}$ is an upper bound for $X_{n+1}$, so $\overline{x_{n+1}}\leq\overline{x_{n}}$, for all $n\in\mathbb{N}$, so it is a monotonically decreasing sequence
Similarly, $\underline{x_{n}}$ is a lower bound for $X_{n+1}$ which implies $\underline{x_{n}}\leq  \underline{x_{n+1}}$, so is a monotonically increasing sequence
Together, these imply:
$$
\overline{x_{n}}-\underline{x_{n}}\geq 0
$$
Taking limits, this gives:
$$
\lim_{ n \to \infty } \overline{x_{n}}-\lim_{ n \to \infty } \underline{x_{n}}\geq 0
$$
Which gives the required result
## Example
Let $x_{n}=(-1)^{n}\left( 1+\frac{1}{n} \right)$, let $n\in\mathbb{N}$ be even, then:
$$
x_{n}=1+\frac{1}{n}
$$
$$
 x_{n+1}=-1-\frac{1}{n+1}
$$
$$
 x_{n+2}=1+\frac{1}{n+2}
$$
So:
$$
\overline{x_{n}}=\text{sup}\left\{  1+\frac{1}{n},-\left( 1+\frac{1}{n+1} \right),1+\frac{1}{n+2},\dots  \right\}
$$
Letting $n$ be odd, we find:
$$
\overline{x_{n}}=\text{sup}\left\{  -\left( 1+\frac{1}{n} \right),1+\frac{1}{n+1},\dots  \right\}
$$
So $\overline{x_{n}}=1+\frac{1}{n+1}$. Note $1\leq \overline{x_{n}}\leq 1+\frac{1}{n}$ for all $n\in\mathbb{N}$
So by the [[Squeeze Theorem|squeeze theorem]], $\lim_{ n \to \infty } \overline{x_{n}}=1$
Let $y_{n}=(-1)^{n}\left( 1-\frac{1}{n} \right)$, here
$$
\overline{y_{n}}=\text{sup}\left\{  1-\frac{1}{n},-\left( 1-\frac{1}{n_{1}} \right),1-\frac{1}{n+2},\dots  \right\}=1
$$
Also for $n$ odd