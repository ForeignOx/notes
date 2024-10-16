Probability is a measure of chance that we assign to [[events|events]] [[Sigma Algebra|$A\in\mathfrak{F}$]] 
Associated to [[Sample Spaces|$\Omega$]], there is a collection denoted as $\mathfrak{F}$, which is the collection of all possible events:
$$
\mathfrak{F}=\{ A|A\subseteq\Omega \}
$$
For finite $\Omega$, we can take [[Power Sets|$\mathfrak{F}=2^\Omega$]] 

## Definition of Probability
A probability $\mathbb{P}$ on a sample space $\Omega$, with $\mathfrak{F}$ is a mapping such that for every event in $\mathfrak{F}$, $\mathbb{P}(A)$ is a real number satisfying the following [[axiom|axioms]]:
$$
\mathbb{P}:\mathfrak{F}\to \mathbb{R}
$$
- $\mathbb{P}(A)\geq 0$ (Probability is always non-negative)
- $\mathbb{P}(\Omega)=1$ (Sample space has full probability)
- If $A,B\in\mathfrak{F}$ and $A$ and $B$ are disjoint, that is, $A\cap B=\emptyset$, then $\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)$ (Finite additivity)
- If you have a collection of events $A_{1},A_{2},\dots$ that are pointwise disjoint, i.e. $A_{i}\cap A_{j}=\emptyset$, for all $i\neq j$, then $\mathbb{P}\left( \bigcup_{n=1}^\infty A_{n}=\sum_{n=1}^n\mathbb{P}(A_{n}) \right)$ (Countable additivity, this is an equivalent axiom to the previous one)
$$
(\Omega,\mathfrak{F},\mathbb{P})
$$
Is the triplet known as the probability space 
## Consequences
- $A,B\in\mathfrak{F}$ then $\mathbb{P}(B\setminus A)=\mathbb{P}(B)-\mathbb{P}(A\cap B)$
### Proof
Note that:
$$
(B\setminus A)\cup(A\cap B)=B
$$
$$
\implies \mathbb{P}(B)=\mathbb{P}((B\setminus A)\cup(A\cap B))
$$
And since $B\setminus A$ and $A\cap B$ are disjoint by definition of set difference, we can use the third axiom to say:
$$
\mathbb{P}(B)=\mathbb{P}(B\setminus A)+\mathbb{P}(A\cap B)
$$
$$
\implies \mathbb{P}(B\setminus A)=\mathbb{P}(B)-\mathbb{P}(A\cap B)
$$
# 
___
- $A\in\mathfrak{F}$ then $\mathbb{P}(A^c)=1-\mathbb{P}(A)$
### Proof
Since:
$$
A\cup A^c=\Omega
$$
And $A$ and $A^c$ are disjoint, then, using the third axiom:
$$
\mathbb{P}(A\cup A^c)=\mathbb{P}(\Omega)
$$
And so using the second axiom:
$$
 \implies \mathbb{P}(A)+\mathbb{P}(A^c)=1
$$
 
$$
\implies \mathbb{P}(A^c)=1-\mathbb{P}(A)
$$
#
___
- $\mathbb{P}(\emptyset)=0$
### Proof
$$
\emptyset=\Omega^c
$$
Using the previous consequence and the second axiom,
$$
 \implies \mathbb{P}(\emptyset)=\mathbb{P}(\Omega^c)=1-\mathbb{P}(\Omega)=1-1=0
$$
#
___
- $A\in\mathfrak{F},\mathbb{P}(A)\leq 1$
### Proof#
Since $\mathbb{P}(A)\geq 0$ and $\mathbb{P}(A)+\mathbb{P}(A^c)=1$, we are adding two probabilites greater than $\hspace{0pt}0$ that sum to $\hspace{0pt}1$, so each must be less than or equal to $\hspace{0pt}1$, so $0\leq\mathbb{P}(A)\leq 1$
# 
___
- If $A\subseteq B$, then $\mathbb{P}(A)\leq \mathbb{P}(B)$, known as monotonicity
### Proof
If $A\subseteq B$ then 
# 
___
- For any two events $A$ and $B$, $\mathbb{P}(A\cup B)=\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B)$
### Proof
# 
___
- If events $A_{1},A_{2},\dots,A_{k}$ are pairwise disjoint (so $A_{i}\cap A_{j}=\emptyset$ if $i\neq j$) then we call finite additivity the property that:
$$
\mathbb{P}\left( \bigcup_{i=1}^kA_{i} \right)=\sum_{i=1}^{k}\mathbb{P}(A_{i})
$$
### Proof
Consider the case when $k=2$, then
$$
\mathbb{P}\left( \bigcup_{i=1}^2A_{i} \right)=\mathbb{P}(A_{1}\cup A_{2})=\mathbb{P}(A_{1})+\mathbb{P}(A_{2})=\sum_{i=1}^2\mathbb{P}(A_{i})
$$
Using the third axiom, since $A_{1}$ and $A_{2}$ are disjoint
Assume the proposition is true for $k=n$, then
$$
\mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)=\sum_{i=1}^n\mathbb{P}(A_{i})
$$
Consider an even $A_{n+1}$ that is pairwise disjoint with all other $A_{1},A_{2},\dots,A_{n}$, then
$$
\mathbb{P}\left( \left( \bigcup_{i=1}^n A_{i} \right)\cup A_{n+1} \right)=\mathbb{P}\left( \bigcup_{i=1}^n A_{i} \right)+\mathbb{P}(A_{n+1})=\sum_{i=1}^n\mathbb{P}(A_{i})+\mathbb{P}(A_{n+1})
$$
$$
\therefore \mathbb{P}\left( \bigcup_{i=1}^{n+1}A_{i} \right)=\sum_{i=1}^{n+1}\mathbb{P}(A_{i})
$$
So if it is true for $k=n$ it is also true for $k=n+1$, and since it is true for $k=2$, it is true for all $k=2,3,4,\dots$ by mathematical induction
# 
___
- Boole's inequality: For any events $A_{1},A_{2},\dots$ (they need not be disjoint):
$$
\mathbb{P}\left( \bigcup_{i=1}^\infty A_{i} \right)\leq \sum_{i=1}^\infty \mathbb{P}(A_{i})
$$
- It is also valid in the finite case for events $A_{1},A_{2},\dots,A_{k}$:
$$
\mathbb{P}\left( \bigcup_{i=1}^k A_{i} \right)\leq \sum_{i=1}^k \mathbb{P}(A_{i})
$$
### Proof

For the finite case, we can use induction. Let $k=2$

# 
___
- Boole's other inequality: For any events $A_{1},A_{2},\dots$:
$$
\mathbb{P}\left( \bigcap_{i=1}^\infty \right)\geq 1-\sum_{i=1}^\infty \mathbb{P}(A^c_{i})
$$
### Proof

# 
___
- Continuity along monotone limits. If $A_{1}\subseteq A_{2}\subseteq\dots$ is an increasing sequence of events, then:
$$
\mathbb{P}\left( \bigcup_{i=1}^\infty A_{i} \right)=\lim_{ i \to \infty }\mathbb{P}(A_{i}) 
$$
- If $A_{1} \supseteq A_{2} \supseteq\dots$ is a decreasing sequence of events, then
$$
\mathbb{P}\left( \bigcap_{i=1}^\infty A_{i} \right)=\lim_{ i \to \infty } \mathbb{P}(A_{i})
$$
## Example
$$
\Omega=\{ \omega_{1},\omega_{2},\dots,\omega_{m} \}
$$
Let $\omega_{i},1\leq i\leq m$ be distinct
$$
A=\{ \omega_{1},\omega_{2},\omega_{3} \}\subseteq\Omega
$$
Since they are distinct, by the third axiom, and since:
$$
\{ \omega_{1} \}\subseteq\Omega,\{ \omega_{2} \}\subseteq\Omega,\{ \omega_{3} \}\subseteq\Omega
$$
Then
$$
\mathbb{P}(A)=\mathbb{P}(\{ \omega_{1} \}\cup \{ \omega_{2} \}\cup \{ \omega_{3} \})=\sum_{i=1}^3\mathbb{P}(\{ \omega_{i} \})
$$
So if $\mathbb{P}(\{ \omega_{i} \})=p_{i}\geq 0$ ($1\leq i\leq m$), such that $\sum_{i=1}^mp_{i}=1$, 
$$
\Omega=\bigcup_{i=1}^m\{ \omega_{i} \}
$$
Therefore
$$
\mathbb{P}(\Omega)=\sum_{i=1}^m\mathbb{P}(\{ \omega_{i} \})=1
$$
Then $A\subseteq\Omega$, 
$$
\mathbb{P}(A)=\sum_{i|w_{i}\in A}p_{i}
$$
### Equally Likely Outcomes
If an experiment has equally likely outcomes, it means that $p_{i}$ are all equal and, in this example, $p_{1}=p_{2}=\dots=p_{m}=\frac{1}{m}$ 
### Throwing a Fair Die (A D6)
$$
\Omega=\{ 1,2,\dots,6 \}
$$
In this case, Fair$\equiv$equally likely, so
$$
\mathbb{P}(\{ 1 \})=\mathbb{P}(\{ 2 \})=\dots=\mathbb{P}(\{ 6 \})=\frac{1}{6}
$$
$$
A=\{ \text{even score} \}=\{ 2,4,6 \}
$$
$$
\mathbb{P}(A)=\sum_{i|\omega_{i}\in A}p_{i}=\frac{1}{6}|A|=\frac{3}{6}=\frac{1}{2}
$$


#Mathematics #Probability 
