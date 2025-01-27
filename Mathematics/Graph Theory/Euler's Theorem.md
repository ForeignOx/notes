Let $G=(V,E,\phi)$ be a finite [[Connectedness|connected]] [[Graphs|graph]] with $\left| V \right|>1$. Then $G$ has an [[Euler Circuits|Euler]] [[Trails#Circuits|circuit]] iff all vertices of $G$ have even [[Degree of Vertices|degree]]
## Lemma 
If a graph $G=(V,E,\phi)$ is finite and connected, with $\left| V \right|>1$ and all vertices of even degree, then $G$ is a finite union of edge-disjoint [[Paths#Cycle|cycles]] (where no two cycles $C_{1},C_{2}$ in $G$ having edge $(e_{j}),(f_{j})$ respectively are edge-disjoint if no $e_{j}$ is 
equal to any $f_{k}$); that is, there are cycles $C_{1},C_{2},..,C_{n}$ such that the union of the vertices of these cycles is eual to $V$ and the union of edges is equal to $E$
### Proof
Since $G$ is conected, it has no isolated vertices (vertices of degree 0). So all vertices have degree $\geq 2$. So by [[Cycles#Lemma|this lemma]], there is a cycle $C_{1}$ in $G$. We form a new graph from $G$ by removing all edges in $C_{1}$. The vertices in $C_{1}$ have their decreased by $2$ in this new graph and the degrees of all other vertices are unchanged. We next discard any vertices which are now isolated in this new graph. We are left with a graph in which all vertices have even degree $\geq 2$, so using the same lemma, we can find another cycle $C_{2}$, and repeat the process. Since $G$ is finite, eventually the degrees of all vertices have decreased to $\hspace{0pt}0$. Thus, every edge and vertex of $G$ belongs to some cycle, and therefore we have decomposed $G$ into disjoint cycles as required 
## Proof of Euler's Theorem
$\implies$ direction:
Since one enters each vertex as often as one leaves it and the degree of each vertex is even, so $G$ has an Euler circuit if all vertices of $G$ have an even degree
$\impliedby$ direction:
