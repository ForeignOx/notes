Let $a_{n}$ be a [[Sequences|sequence]] of real numbers and $l\in\mathbb{R}$. $a_{n}$ converges to $l$ if:
$$
\forall\epsilon>0,\exists N_{\epsilon}\in\mathbb{N}:\forall n\geq N_{\epsilon},\left|a_{n}-l\right|<\epsilon
$$
And using a proof in [[Proofs with Inequalities]], we know:
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
## Example 5
Let $a_{n}=\frac{1}{n}$. Prove that $a_{n}$ converges to 0 as $n\to \infty$
$$
n=\frac{1}{\epsilon}\iff\epsilon=\frac{1}{n}
$$
So our $N\epsilon$ will have to be greater $\frac{1}{\epsilon}$, so we use:
$$
N_\epsilon=\left\lceil  \frac{1}{\epsilon}  \right\rceil 
$$
But when $\frac{1}{\epsilon}$ is an integer, this is still too small, so we instead use:
$$
N_\epsilon =\left\lceil  \frac{1}{\epsilon}  \right\rceil +1
$$
### Proof
Given $a_{n}=\frac{1}{n}$ and $\epsilon>0$. Let $N_{\epsilon}=\left\lceil  \frac{1}{\epsilon}  \right\rceil+1$
If $n\geq N_{\epsilon}$ then:
$$
n\geq \left\lceil  \frac{1}{\epsilon}  \right\rceil +1>\left\lceil  \frac{1}{\epsilon}  \right\rceil \geq \frac{1}{\epsilon}
$$
So $n>\frac{1}{\epsilon}$ since $\epsilon>0$ and $n\geq \frac{1}{\epsilon}>0$
$$
\left|a_{n}-0\right|=\left|\frac{1}{n}\right|=\frac{1}{n}<\epsilon
$$
So $a_{n}$ converges to 0
## Example 6
Let $a_{n}=\frac{(-1)^{n}}{2n^{2}}$. Prove that $a_{n}$ converges to 0 as $n\to \infty$
$$
\left| \frac{(-1)^{n}}{2n^{2}}-0\right|=\frac{1}{2n^{2}}<\epsilon 
$$
$$
\implies \frac{1}{2\epsilon}<n^{2}
$$
$$
\implies \sqrt{ \frac{1}{2\epsilon} }<n
$$
$$
\therefore N_{\epsilon}=\left\lceil  \sqrt{ \frac{1}{2\epsilon} }  \right\rceil +1
$$
### Proof
Let $\epsilon>0$
Let $N_{\epsilon}=\left\lceil  \sqrt{ \frac{1}{2\epsilon} }  \right\rceil +1$
 If $n\geq N_{\epsilon}$ then:
 $$
n\geq \left\lceil  \sqrt{ \frac{1}{2\epsilon} }  \right\rceil +1>\left\lceil  \sqrt{ \frac{1}{2\epsilon} }  \right\rceil \geq \sqrt{ \frac{1}{2\epsilon} }
$$
$$
\implies n>\sqrt{ \frac{1}{2\epsilon} }
$$
$$
\implies n^{2}>\frac{1}{2\epsilon}
$$
$$
\implies \epsilon>\frac{1}{2n^{2}}
$$
as $n>0$
$$
\left|a_{n}-0\right|=\left| \frac{(-1)^{n}}{2n^{2}}-0\right|=\frac{1}{2n^{2}}<\epsilon
$$
So $a_{n}$ converges to 0
## Example 7
Let $a_{n}=\frac{\sin n}{n}$. Prove that $a_{n}$ converges to 0 as $n \to \infty$
$$
\left| \frac{\sin n}{n}-0\right|<\epsilon 
$$
$$
\left| \frac{\sin n}{n}\right|=\frac{\left|\sin n\right|}{n}\leq \frac{1}{n}
$$
$$
\therefore N_{\epsilon}=\left\lceil  \frac{1}{\epsilon}  \right\rceil +1
$$

### Proof
Given $a_{n}=\frac{\sin n}{n}$, $\epsilon>0$. Let $N_{\epsilon}=\left\lceil  \frac{1}{\epsilon}  \right\rceil+1$
If $n\geq N_{\epsilon}$ then
$$
n\geq \left\lceil  \frac{1}{\epsilon}  \right\rceil +1>\left\lceil  \frac{1}{\epsilon}  \right\rceil \geq \frac{1}{\epsilon}
$$
$$
\left|a_{n}-0\right|=\left| \frac{\sin n}{n}-0\right|=\frac{\left|\sin n\right|}{n}\leq \frac{1}{n}<\epsilon
$$
So $a_{n}$ converges to 0
## Example 8
Let $a_{n}=\frac{n^{2}}{1+n^{2}}$. Prove that $a_{n}$ converges to 1 as $n\to \infty$
$$
\left| \frac{n^{2}}{1+n^{2}}-1\right|=\left| \frac{n^{2}-(1+n^{2})}{1+n^{2}}\right|=\left| \frac{-1}{1+n^{2}}\right|=\frac{1}{1+n^{2}}<\epsilon 
$$
$$
\implies \frac{1}{\epsilon}<1+n^{2}
$$
$$
\implies \sqrt{ \frac{1-\epsilon}{\epsilon} }<n
$$
If $\epsilon \leq 1$
### Proof
Given $a_{n}=\frac{n^{2}}{1+n^{2}}$ and $\epsilon>0$ 
If $\epsilon \leq 1$
Let $N_{\epsilon}=\left\lceil  \sqrt{ \frac{1-\epsilon}{\epsilon} }  \right\rceil+1$
If $n\geq N_{\epsilon}$ then
$$
n\geq \left\lceil  \sqrt{\frac{1-\epsilon}{\epsilon}}  \right\rceil +1>\left\lceil  \sqrt{ \frac{1-\epsilon}{\epsilon} }  \right\rceil \geq \sqrt{ \frac{1-\epsilon}{\epsilon} }
$$
$$
\implies n>\sqrt{ \frac{1-\epsilon}{\epsilon} }
$$
$$
\implies n^{2}+1>\frac{1}{\epsilon}
$$
$$
\implies \epsilon>\frac{1}{1+n^{2}}
$$
$$
\left|a_{n}-l\right|=\left| \frac{n^{2}}{1+n^{2}}-1\right|=\left| \frac{-1}{1+n^{2}}\right|=\frac{1}{1+n^{2}}<\epsilon
$$
so $a_{n}$ converges to 1
If $\epsilon>1$
Let $N_{\epsilon}=1$
If $n\geq N_{\epsilon}=1\implies n^{2}+1\geq 2$
$$
\left| \frac{n^{2}}{1+n^{2}}-1 \right|=\frac{1}{1+n^{2}}\leq \frac{1}{2}<\epsilon
$$
So $a_{n}$ converges to 1
## Example 9???
Let $a_{n}=\frac{4n^{2}-1}{n^{2}+1}$. Prove that $a_{n}$ converges to 4 as $n\to \infty$
$$
\left| \frac{4n^{2}-1}{n^{2}+1}-4 \right|=\left| \frac{4n^{2}-n^{2}-4(n^{2}+1)}{n^{2}+1} \right|=\left| \frac{-5}{n^{2}+1} \right|=\frac{5}{n^{2}+1}
$$
$$
\frac{5}{n^{2}+1}<\frac{5}{n^{2}}<\epsilon 
$$
$$
\implies n>\sqrt{ \frac{5}{\epsilon} }
$$
### Proof
Given $a_{n}=\frac{4n^{2}-1}{n^{2}+1}$ and $\epsilon>0$
Let $N_{\epsilon}=\left\lceil  \sqrt{ \frac{5}{\epsilon} }  \right\rceil+1$
If $n\geq N_{\epsilon}$ then
$$
n\geq \left\lceil  \sqrt{ \frac{5}{\epsilon} }  \right\rceil +1>\left\lceil  \sqrt{ \frac{5}{\epsilon} }  \right\rceil \geq \sqrt{ \frac{5}{\epsilon} }
$$
$$
\implies n>\sqrt{ \frac{5}{\epsilon} }
$$
$$
\implies \epsilon>\frac{5}{n^{2}}
$$
Since $n>0$
$$
\left| a_{n}-l \right|=\left| \frac{4n^{2}-1}{n^{2}+1}-4 \right|=\left| -\frac{5}{n^{2}+1} \right|=\frac{5}{n^{2}+1}<\frac{5}{n^{2}}<\epsilon
$$
So $a_{n}$ converges to 4

#Mathematics #Analysis  #Definition 