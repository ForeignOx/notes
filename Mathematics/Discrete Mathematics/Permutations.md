A permutation on a [[Sets|set]] $S$ is a list of elements of $S$ using each element exactly once
Given a collection of $n$ distinct objects, any linear [[Arrangements|arrangement]] of these objects is called a permutation of the collection 
A permutation of a set $X$ is a bijective mapping $\sigma:X\to X$ (one-to-one and onto)
The set of permutations of $n$ objects is $S_{n}$ and it has $n!$ elements
In general, if there are $n$ distinct objects, denoted $a_{1},a_{2},\dots,a_{n}$, and $r$ is an integer, with $1\leq r\leq n$, then by the [[Rule of Product|rule of product]], the number of permutations of size $r$ for the $n$ objects is:
$$
n\times(n-1)\times(n-2)\times\dots \times(n-r+1)=\frac{n!}{(n-r)!}
$$
We denote this number $P(n,r)$. For $r=0$, $P(n,0)=1$
Another way of thinking about this is ordered choice of distinct objects with replacement; if you have $n$ distinct ojects, choose $r$ of them without replacement, then the number of choices can be denoted by $(n)_{r}=P(n,r)$
When permuting all the $n$ objects in the collection, we have $r=n$ and find that $P(n,n)=n!$
## Examples
The permutations on set $\{ M,A,T,H \}$ are:
MATH,MAHT,MHTA,... ($\hspace{0pt}24$ total)
___
### The Birthday Problem
This is part of a large class of problems called the mattching probems
In a room there are $n<365$ people, a year has $\hspace{0pt}365$ days and:
$$
B:=\{ \text{At least two people have the same birthday} \}
$$
Find $\mathbb{P}(B)$
We can write $B$ as an $n$-tuple:
$$
(D_{1},D_{2},\dots,D_{n})
$$
Where $D_{i}$ represents the $i$th person's birthday. $\Omega$ is the collection of all such tuples, so $|\Omega|=365^n$ since each of the $n$ people can be born on any of the $\hspace{0pt}365$ days
$$
B^c=\{ \text{No two people have the same birthday} \}
$$
We can see that:
$$
B=\{ \text{Exactly $\hspace{0pt}2$ poeple have the same birthday} \}\cup \{ \text{Exactly $\hspace{0pt}3$ people have the same birthday} \}
$$
$$
\cup\dots  \cup \{ \text{All people have the same birthday} \}
$$
Let $B_{i}=\{ \text{Exactly }i+1\text{ people have the same birthday} \}$, then:
$$
B=\bigcup_{i=1}^{n-1}B_{i}
$$
Then by [[De Morgan's Laws|De Morgan's Laws]], we get:
$$
B^{c}=\bigcap_{i=1}^{n-1}B_{i}^{c}
$$
And we can work out $|B^{c}|=(365)_{n}$ because the first person would have $\hspace{0pt}365$ choices, then the second would have $\hspace{0pt}364$ and so on as each person cannot choose a day that has come before therefore, since $|A|+|A^{c}|=|\Omega|$, and $\mathbb{P}(B)=1-\mathbb{P}(B^{c})$:
$$
\mathbb{P}(B)=1-\frac{(365)_{n}}{365^{n}}
$$
## Permutations with Repetitions
Given a list of $n$ objects of $r$ different types, in which objects of type $i$ occur $n_{i}$ times (with $n_{1}+n_{2}+\dots+n_{r}=n$), the number of arrangements of the list is:
$$
P(n;n_{1},n_{2},\dots n_{r})=\frac{n!}{n_{1}!n_{2}!\dots n_{r}!}
$$
The reason for this is to think that there are $n!$ permutations of the list, but objects of type $i$ could be permuted with no consequence, since they are indistinct. So for each $i$, there are $n_{i}!$ identical permutations, so to remove them we simply divide 
Note the special case of two types $r$ objects of type $\hspace{0pt}1$, there are left $n-r$ objects of type 2, the number of distinct ordered choices is:
$$
P(n; r,n-r)=\begin{pmatrix}
m\\r
\end{pmatrix}
$$



#Mathematics #Discrete #Definition