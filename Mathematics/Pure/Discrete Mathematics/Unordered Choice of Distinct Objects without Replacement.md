If you have $n$ objects, and you want to choose $r\leq m$ without replacement, then number of distinct subsets that we can form is:
$$
\begin{pmatrix}
n\\r
\end{pmatrix}= \,^nC_{r}=C(n,r)=C^r_{n}:=\frac{n(n-1)(n-2)\dots(n-r+1)}{r!}=\frac{n!}{r!(n-r)!}
$$
In this case ordering of the $r$ objects does not matter, so we can arrange them in $r!$ ways, and the numerator is obtained by [[Permutations|permuting]] the numbers


#Mathematics #Discrete 