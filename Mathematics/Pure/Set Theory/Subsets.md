If $R$ and $S$ are [[Sets|sets]], then $R\subset S$ means $R$ is a proper subset of $S$, so every element of $R$ is also an element of $S$, but there are elements in $S$ that are not in $R$
$$
x\in R\implies x\in S
$$
If $R$ and $S$ are sets, then $R\subseteq S$ means $R$ is an improper subset of $S$, so every element of $R$ is also an element of $S$, so we have $\emptyset\subseteq S$ and $S\subseteq S$. We also have for example $\mathbb{N}\subset \mathbb{Z}\subset \mathbb{R}$
## Problem
Let $A=\{ 1,2,3,4,5,6 \}$. How many subsets does $A$ have?
We know $A$ and $\emptyset$ are two, then we have $\{ 1 \},\{2  \},\dots,\{ 1,2 \},\dots$ this is quite a tedious process. The answer? $2^6$
## Proof
Let $I=\{ 0,1 \}$. Consider $I^6=\{ (a_{1},a_{2},\dots,a_{6})|a_{i}\in I \}$, $|I^{6}|=2^6$
We then construct a $\hspace{0pt}1$ to $\hspace{0pt}1$ bijection between $I^6$ and the set of subsets:
$$
A\leftrightarrow (1,1,1,1,1,A)
$$
$$
\{ 1,4,5 \}\leftrightarrow 
$$


#Mathematics #Set