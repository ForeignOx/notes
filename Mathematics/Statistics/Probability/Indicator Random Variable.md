Let [[Sample Spaces|$A\subseteq\Omega$]], then the indicator of $A$, denoted by $\mathbb{1}_{A}$ is defined as follows:
$$
\mathbb{1}_{A}(\omega)=\begin{cases}
1&\text{if }\omega \in A\\0&\text{if }\omega \not\in A
\end{cases}
$$
The number of ways the indicator function gives $\hspace{0pt}1$ is also the [[Cardinality of Sets|cardinality]] of $A$, so
$$
\mathbb{P}(A)=\frac{|A|}{|\Omega|}
$$
$$
 |A|=\sum_{\omega \in A}\mathbb{1}_{A}(\omega)
$$
But also since the other $\omega_{i}$ will give zero, we can in fact say
$$
|A|=\sum_{\omega \in \Omega}\mathbb{1}_{A}(\omega)
$$
We can also say
$$
\mathbb{P}_{A}(\{ 1 \})=\mathbb{P}(\{ \omega\mid \mathbb{1}_{A}(\omega)=1 \})=\mathbb{P}(A)
$$
$$
\mathbb{P}_{A}(\{ 0 \})=\mathbb{P}(\{ \omega\mid \mathbb{1}_{A}(\omega)=0 \})=\mathbb{P}(A^{c})
$$
Now we will abuse notation slightly and consider these as the same:
$$
\mathbb{P}_{X}(\{ x \})=\mathbb{P}_{X}(x)
$$