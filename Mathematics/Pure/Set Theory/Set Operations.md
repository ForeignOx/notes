Given several [[sets|sets]], there are a few important ways of combining them to make further sets using set operations
Given sets $A$ and $B$, $A\cup B$ is the union of $A$ and $B$, which is the set consisting of those elements that are in $A$ or in $B$ (or in both). For example,
$$
\{ -2,-1,0 \}\cup \{ 0,1,2 \}=\{ -1,-2,0,1,2 \}
$$
$A\cap B$ is the intersection of sets $A$ and $B$, whichis the set of those elements thjat are in both $A$ and $B$. For example,
$$
\{ -2,-1,0 \}\cap \{ 0,1,2 \}=\{ 0 \}
$$
From the definitions, we can see that $A\cup B=B\cup A$, so $\cup$ is commutative, and $A\cap B=B\cap A$ so $\cap$ is also commutative
We also have $A\cup \emptyset=A$ and $A\cap \emptyset=\emptyset$
![[Set Operations 2024-09-21 13.31.26.excalidraw]]
The set difference between $A$ and $B$, sometimes called $A$ minus $B$, is the set consisting of the elements of $A$ which are not also in $B$. We write:
$$
A\setminus B=\{ x \in A:x \not\in B \}
$$
For example, $\mathbb{Z}\setminus \mathbb{N}=\{ 0,-1,-2,\dots \}$
![[Set Operations 2024-09-21 13.48.08.excalidraw]]
## Many sets
When we want to take the union or intersection of several sets, we can use more compact notation: instead of writing
$$
A_{1}\cap A_{2}\cap A_{3}\cap\dots \cap A_{n}
$$
We instead write
$$
\bigcap_{i=1}^nA_{i}=\{ x:x \in A_{i} \text{ for every } i\}
$$
Similarly we can write
$$
\bigcup_{i=1}^nA_{i}=A_{1}\cup A_{2}\cup A_{3}\cup\dots \cup A_{n}=\{ x : x \in A_{i} \text{ for at least one }i \}
$$
