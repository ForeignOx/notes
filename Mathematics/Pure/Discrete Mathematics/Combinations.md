A combination from a [[Sets|set]] of objects is an unordered selection of elements of that set. Repeats may be allowed
So $STOAT$ and $TOAST$ are different [[Arrangements|arrangements]], but the same combinations
Formally a combination on set $S$ is identified by factors $m_{i}$, $i\in S$, where $m_{i}=$ number of times element $i$ appears
In our example, $A:1,O:1,S:1,T:2$ 
The size at combination is the total number of selections we call a combination of size $k$ a $k$-combination
How many $k$-combinations without repetitions do we have from a set of size $n$
If we start with $n$ distinct objects, each selection, or combination, of $r$ of these objects, with no reference to order, corresponds to $r!$ [[Permutations|permutations]] of a size $r$ from the $n$ objects. Thus the number of combinations of size $r$ forom a collection of size $n$, denoted $C(n,r)$, where $0\leq r\leq n$ satisfies $(r!)C(n,r)=P(n,r)$, so:
$$
C(n,r)=\, ^nC_{r}=C^r_{n}=\begin{pmatrix}
n\\r
\end{pmatrix}:=\frac{P(n,r)}{r!}=\frac{n!}{r!(n-r)!}=\frac{n(n-1)(n-2)\dots(n-r+1)}{r!}
$$
Note that:
$$

$$
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
Also note that $^nC_{r}$ is also a binomial coefficient, and appears in the [[Binomial Theorem|binomial expansion]] of $(1+x)^{n}$
## Example
From the letters $P,Q,R,S$, find the number of combinations of $\hspace{0pt}2$ distinct letters, then $\hspace{0pt}3$ distinct letters
Solution: for the first case there are $\hspace{0pt}6$ combinations, for the second there are $\hspace{0pt}4$, 

#Mathematics #Discrete 