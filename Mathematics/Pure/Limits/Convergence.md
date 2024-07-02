Let $a_{n}$ be a [[Sequences|sequence]] of real numbers and $l\in\mathbb{R}$. $a_{n}$ converges to $l$ if:
$$
\forall\epsilon>0,\exists N_{\epsilon}\in\mathbb{N}:\forall n\geq N_{\epsilon},\left|a_{n}-l\right|<\epsilon
$$
And using a proof in [[proofs with inequalities]], we know:
$$
\left|a_{n}-l\right|<\epsilon\iff l-\epsilon<a_{n}<l+\epsilon
$$
## Example 1
$a_{n}=\frac{1}{n}$, clearly $l=0$
![[Convergence 2024-07-02 09.51.22.excalidraw]]
We can take an example of $\epsilon$ to be $\epsilon=0.1$, so we are looking for:
$$
\left|a_{n}-0\right|<0.1\iff-0.1<a_{n}<0.1
$$
![[Convergence 2024-07-02 09.54.56.excalidraw]]
For $n\geq 11$, $-0.1<a_{n}<0.1$, so we can take $N_{\epsilon}=11$, however, this is also true for $n\geq 79$, so if we wanted, $N_{\epsilon}$ would be acceptible, so:
$$
N_{\epsilon}\in\{ x \in\mathbb{N}:x\geq 11 \}
$$
## Example 2
$a_{n}=1$,
If we take $\epsilon=1$, we can have $N_{\epsilon}=1$, if we take $\epsilon=0.5$ we can have $N_{\epsilon}=1$, if we take $\epsilon=0.000001$, we can have $N_{\epsilon}=1$ because it has already converged, so constant sequences clearly converge
## Example 3
For a convergent sequence such as $a_{n}=n^{2}$, we can never draw lines that bound the sequence, it always escapes:
![[Convergence 2024-07-02 10.11.07.excalidraw]]

## Example 4
$a_{n}=(-1)^{n}$
If we take $\epsilon=2$, $N_{\epsilon}=1$, so that works, as $n\geq 1$, $\left|a_{n}-0\right|<2$, but if instead we take $\epsilon=0.5$, we cannot bound the sequence by the two lines, so it doesn't converge as the definition is only true for all $\epsilon>0$