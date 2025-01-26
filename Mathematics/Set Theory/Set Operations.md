Given several [[Sets|Sets]], there are a few important ways of combining them to make further sets using set operations, in probability they are known as [[Events|event]] calculus 
## Union
Given sets $A$ and $B$, $A\cup B$ is the union of $A$ and $B$, which is the set consisting of those elements that are in $A$ or in $B$ (or in both)
$$
A\cup B=\{ x|x\in A \text{ or }x\in B\text{ or }x\in \text{both} \}
$$

For example,
$$
\{ -2,-1,0 \}\cup \{ 0,1,2 \}=\{ -1,-2,0,1,2 \}
$$
![[Set Operations 2024-10-07 15.48.18.excalidraw]]
## Intersection
$A\cap B$ is the intersection of sets $A$ and $B$, whichis the set of those elements that are in both $A$ and $B$
$$
A\cap B=\{ x|x\in A\text{ and }x\in B \}
$$
For example,
$$
\{ -2,-1,0 \}\cap \{ 0,1,2 \}=\{ 0 \}
$$
From the definitions, we can see that $A\cup B=B\cup A$, so $\cup$ is commutative, and $A\cap B=B\cap A$ so $\cap$ is also commutative
We also have $A\cup \emptyset=A$ and $A\cap \emptyset=\emptyset$
![[Set Operations 2024-09-21 13.31.26.excalidraw]]
## Set Difference
The set difference between $A$ and $B$, sometimes called $A$ minus $B$, is the set consisting of the elements of $A$ which are not also in $B$. We write:
$$
A\setminus B=\{ x \in A|x \not\in B \}
$$
For example, $\mathbb{Z}\setminus \mathbb{N}=\{ 0,-1,-2,\dots \}$
![[Set Operations 2024-09-21 13.48.08.excalidraw]]
## Complement
The complement of set $A$ is written $A^c$, which means all elements not in the set $A$
$$
A^c=\{ x|x \not\in A \}
$$
We often use complement in the context of sets being [[Subsets|subsets]]; if $A\subset S$, $A^c$ will be all other elements in $S$, rather than any elements possible at all; it is a different way of writing the set difference
Note that $(A^c)^c=A$
## Cartesian Product
The cartesian product of two sets $X,Y$ is given by:
$$
X\times Y=\{ (x,y)|x\in X,y\in Y \}
$$
Where $(x,y)$ is an [[Ordered Pairs|ordered pair]] of elements in each set
For example if $X=\{ 1,2,3 \}$, and $Y=\{ a,b \}$:
$$
X\times Y=\{ (1,a),(2,a),(3,a),(1,b),(2,b),(3,b) \}
$$
Note the notation $X\times X=X^{2}$ and in general $X^{n}=X\times X\times \dots \times X$ $n$ times
$$
X^n=\{ (x_{1},x_{2},\dots,x_{n})|x_{i}\in X\forall i \}
$$
Let $X$ and $Y$ be finite sets, then $|X\times Y|=|X||Y|$, and hence $|X^{n}|=|X|^{n}$
## Many sets
When we want to take the union or intersection of several sets, we can use more compact notation: instead of writing
$$
A_{1}\cap A_{2}\cap A_{3}\cap\dots \cap A_{n}
$$
We instead write
$$
\bigcap_{i=1}^nA_{i}=\{ x|x \in A_{i} \text{ for every } i\}
$$
Similarly we can write
$$
\bigcup_{i=1}^nA_{i}=A_{1}\cup A_{2}\cup A_{3}\cup\dots \cup A_{n}=\{ x | x \in A_{i} \text{ for at least one }i \}
$$
## Probability Analogues

| Notation                   | Set Theory Language                 | Probability Analogue | Meaning as Events                |
| -------------------------- | ----------------------------------- | -------------------- | -------------------------------- |
| $A\cup B$                  | $A$ union $B$                       | $A$ or $B$ (or both) | $A$ or $B$ occurs, or both occur |
| $A\cap B$                  | $A$ intersection $B$                | $A$ and $B$          | Both $A$ and $B$ occur           |
| $A^c$                      | $A$ complement                      | Not $A$              | $A$ does not occur               |
| $A\setminus B$             | $A$ 'setminus' $B$                  | $A$ but not $B$      | $A$ occurs, but $B$ does not     |
| $A\subseteq B$             | $A$ is a [[Subsets\|subset]] of $B$ | $A$ implies $B$      | If $A$ occurs, $B$ also occurs   |
| [[Empty Set\|$\emptyset$]] | Null Set                            | Impossible event     | <-                               |



#Mathematics #Set