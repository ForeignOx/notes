Consider $n\in\mathbb{N}$, $a,b\in\mathbb{R}$, then:
$$
(a+b)^{n}=\sum_{ r=0} ^{ n}  \begin{pmatrix}
n\\r
\end{pmatrix}a^rb^{n-r}
$$
## Proof
By [[Proof by Mathematical Induction!!!!!|mathematical induction]]
For $n=1$:
$$
\sum_{r=0}^{1}\begin{pmatrix}
1\\r
\end{pmatrix}a^{1-r}b^{r}=a+b
$$
So is true for $n=1$ 
Assume true for $n\in\mathbb{N}$:
$$
(a+b)^{n+1}=(a+b)(a+b)^{n}=(a+b)\sum_{ k=0}^{ n} \begin{pmatrix}
n\\k
\end{pmatrix}  a^{n-k}b^{k}
$$
$$
= \sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}a^{n+1-k}b^{k}+\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}a^{n-k}b^{k+1}
$$
$$
 = a^{n+1}+b^{n+1}+\sum_{ k=1} ^{ n}a^{n+1-k}b^{k}+  \sum_{ k=1} ^{ n}  \begin{pmatrix}
n\\k-1
\end{pmatrix}a^{n+1-k}b^{k}
$$
$$
=a^{n+1}+b^{n+1} \sum_{ k=1} ^{ n}  \left( \begin{pmatrix}
n\\ k
\end{pmatrix}+\begin{pmatrix}
n\\k-1
\end{pmatrix} \right)a^{n+1-k}b^{k}
$$
$$
= \sum_{ k=0} ^{ n+1}  \begin{pmatrix}
n+1\\k
\end{pmatrix}a^{n+1-k}b^{k}
$$
## Examples
Prove for integer $n\geq 0$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}=2^{n}  
$$
For $n\geq 1$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}(-1)^{k}=0
$$
For $n\geq 0$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}2^{k}=3^{n}  
$$
$$
\sum_{ k=0} ^{ n}\begin{pmatrix}
n\\k
\end{pmatrix}k=n\times 2^{n-1}
$$
To solve these, we can consider the binomial theorem in the form:
$$
(1+x)^{n}=\sum_{k=0}^{n}\begin{pmatrix}
n\\k
\end{pmatrix}x^{k}
$$
For the first one, let $x=1$,
$$
(1+1)^{n}=\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}=2^{n}
$$
For the second, let $x=-1$
$$
(1-1)^{n}=\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}(-1)^{k}=0
$$
For the third, let $x=2$
$$
(1+2)^{n}=\sum_{ k=0} ^{ n}  \begin{pmatrix}
n\\k
\end{pmatrix}2^{k}=3^{n}
$$
For the fourth, the trick is to differentiate both sides with respect to $n$:
$$
n(1+x)^{n-1}=\sum_{k=0}^{n}\begin{pmatrix}
n\\k
\end{pmatrix}kx^{k-1}
$$
Now let $x=1$
$$
n(1+1)^{n-1}=\sum_{k=0}^{n}\begin{pmatrix}
n\\k
\end{pmatrix}k=n 2^{n-1}
$$
