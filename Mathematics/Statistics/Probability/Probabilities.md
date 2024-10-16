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
# <br>
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
# <br>
___
- $\mathbb{P}(\emptyset)=0$
### Proof#



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
