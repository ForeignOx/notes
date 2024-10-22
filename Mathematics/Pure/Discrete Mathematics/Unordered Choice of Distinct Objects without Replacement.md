If you have $n$ objects, and you want to choose $r\leq m$ without replacement, then number of distinct subsets that we can form is:
$$
\begin{pmatrix}
n\\r
\end{pmatrix}= \,^nC_{r}=C(n,r)=C^r_{n}:=\frac{n(n-1)(n-2)\dots(n-r+1)}{r!}=\frac{n!}{r!(n-r)!}
$$
In this case ordering of the $r$ objects does not matter, so we can arrange them in $r!$ ways, and the numerator is obtained by [[Permutations|permuting]] the numbers
Note that:
$$
\begin{pmatrix}
n\\r
\end{pmatrix}=\begin{pmatrix}
n\\n-r
\end{pmatrix}=\begin{pmatrix}
n-1\\r-1
\end{pmatrix}+\begin{pmatrix}
n-1\\r
\end{pmatrix}
$$
The second equality is also known as Pascal's formula
Also note that $^nC_{r}$ is also a binomial coefficient, and appears in the binomial expansion of $(1+x)^{n}$, this is our first hint of a connection between counting problems and power series

#Mathematics #Discrete 