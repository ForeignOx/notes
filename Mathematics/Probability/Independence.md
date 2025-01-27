Let $A$, $B$ be $\hspace{0pt}2$ [[Events|events]], $A$ and $B$ are said to be independent if:
$$
\mathbb{P}(A\cap B)=\mathbb{P}(A)\mathbb{P}(B)
$$
Using the formula for [[Conditional Probability|conditional probability]]:
$$
\mathbb{P}(A\cap B)=\mathbb{P}(A|B)\mathbb{P}(B)
$$
So if two events are independent, then:
$$
\mathbb{P}(A|B)=\mathbb{P}(A)
$$
In other words, learning about $B$ will not tell us anything new about $A$, and similarly, learinning about $A$ will not tell us anything new about $B$
Note that independence cannot be observed on a Venn Diagram
## Multiple Events
A (possibily infinite) collection of events $\mathcal{A}\subseteq \mathfrak{F}$ are mutually independent if for every finite non-empty $\mathcal{C}\subseteq \mathcal{A}$, that is, $\mathcal{B}$ is a finite subcollection of the events in question,
$$
\mathbb{P}\left( \bigcap_{A\in \mathcal{C}}A \right)=\prod_{A\in \mathcal{C}}\mathbb{P}(A)
$$

## Complement
Show that if $A$ and $B$ are independent, then $A$ and $B^{c}$ are also independent
### Proof
We know that $\mathbb{P}(A\cap B)=\mathbb{P}(A)\mathbb{P}(B)$, we have to also show that $\mathbb{P}(A\cap B^{c})=\mathbb{P}(A)\mathbb{P}(B^{c})$
Observe that $A=(A\cap B)\cup (A\cap B^{c})$, so:
$$
\mathbb{P}(A)=\mathbb{P}(A\cap B)+\mathbb{P}(A\cap B^{c})
$$
Since $(A\cap B)\cap(A\cap B^{c})=\emptyset$
So
$$
\mathbb{P}(A)=\mathbb{P}(A)\mathbb{P}(B)+\mathbb{P}(A\cap B^{c})
$$
$$
\implies \mathbb{P}(A\cap B^{c})
$$
## Example
Roll a fair die:
$$
A_{1}=\{ 2,4,6 \},A_{2}=\{ 3,6 \},A_{3}=\{ 4,5,6\}
$$
$$
\mathbb{P}(A_{1}\cap A_{2})=\mathbb{P}(\{ 6 \})=\frac{1}{6}
$$
$$
\mathbb{P}(A_{1})\mathbb{P}(A_{2})=\frac{3}{6}\times \frac{2}{6}=\frac{1}{6}=\mathbb{P}(A_{1}\cap A_{2})
$$
So $A_{1}$ and $A_{2}$ are independent
## Multiple [[Random Variables|Radom Variables:]]
$\hspace{0pt}2$ random variables $X$ and $Y$ are [[Independence|independent]] iff:
$$
\mathbb{P}(X \in C,Y\in D)=\mathbb{P}(X \in C)\mathbb{P}(Y\in D)
$$
For all $C,D$ such that $C\subseteq \chi,D\subseteq\Gamma$, known as the product of the marginals, or marginal split
This can be rewritten for [[Discrete Random Variables|discrete variables]] as:
$$
p_{(X,Y)}(x,y)=p_{X}(x)p_{Y}(y)
$$
And [[Continuous Random Variables|continuous variables]] as:
$$
f(x,y)=f_{X}(x)f_{Y}(y)
$$
## [[Expectation|Expectation]]
If $X$ and $Y$ are independent, then $E(XY)=E(X)E(Y)$ and more generally, 
$$
E(g(X)h(Y))=E(g(X))E(h(Y))
$$
### Proof
Let us assume that $(X,Y)$ is jointly discrete with pmf $p(x,y)$
$$
E(g(X)h(Y))=\sum_{x}\sum_{y}g(x)h(y)p(x,y)
$$
Since $X$ and $Y$ are independent, $p(x,y)=p_{X}(x)p_{Y}(y)$, which can be put into our sum as:
$$
=\sum_{x}\sum_{y}g(x)h(y)p_{X}(x)p_{Y}(y)=\left( \sum_{x}g(x)p_{X}(x) \right)\left( \sum_{y}h(y)p_{Y}(y) \right)
$$
$$
=E(g(X))E(h(Y))
$$



#Mathematics #Probability #Definition