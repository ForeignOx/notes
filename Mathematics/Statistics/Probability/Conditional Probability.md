Let $A,B\in\Omega$ be two [[Events|events]]. We define the conditional probability of $A$ given $B$, and denote it by $\mathbb{P}(A|B)$, as follows:
$$
\mathbb{P}(A|B)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
When $\mathbb{P}(B)>0$
Another way of thinking about this is to find the probability of $A$ whan we have observed $B$
## Examples
Roll of the die:
$$
A=\{ \text{score is odd} \}=\{ 1,3,5 \}
$$
$$
B=\{ \text{score is less than 4} \}=\{ 1,2,3 \}
$$
$$
\mathbb{P}(A|B)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}
$$
$$
A\cap B=\{ 1,3 \},|A|=2
$$
$$
\implies \mathbb{P}(A\cap B)=\frac{2}{6}=\frac{1}{3}
$$
$$
\mathbb{P}(B)=\frac{3}{6}=\frac{1}{2}
$$
$$
\therefore \mathbb{P}(A|B)=\frac{\frac{1}{3}}{\frac{1}{2}}=\frac{2}{3}
$$
A family has two children, both sexes are eqully likely:
$$
\Omega=\{ BB,BG,GB,GG \}
$$
Where the first element represents the sex of the first child, and the second, the sex of the younger child
Consider the following events:
$$
A_{1}:=\{ \text{both girls} \}=\{ GG \},\mathbb{P}(A_{1})=\frac{1}{4}
$$
$$
A_{2}:=\{ \text{at least one girl} \}=\{ BG,GB,GG \},\mathbb{P}(A_{2})=\frac{3}{4}
$$
$$
 A_{3}:=\{ \text{elder is a girl} \}=\{ GB,GG \},\mathbb{P}(A_{3})=\frac{1}{2}
$$
Note that:
$$
\mathbb{P}(A_{1}|A_{2})=\frac{\mathbb{P}(A_{1}\cap A_{2})}{\mathbb{P}(A_{2})}
$$
And $A_{1}\subseteq A_{2}\implies A_{1}\cap A_{2}=A_{1}$, so $\mathbb{P}(A_{1}|A_{2})=\frac{\mathbb{P}(A_{1})}{\mathbb{P}(A_{2})}=\frac{1}{3}$
Consider $\mathbb{P}(A_{2}|A_{1})$l:
$$
\mathbb{P}(A_{2}|A_{1})=\frac{\mathbb{P}\left( A_{1}\cap A_{2} \right)}{\mathbb{P}(A_{1}}= \frac{\mathbb{P}(A_{1})}{\mathbb{P}(A_{1})}=1
$$
## Properties of Conditional Probability
- Let $B$ be an event, such that $\mathbb{P}(B)>0$, then $\mathbb{P}(\cdot|B)$ (the $\cdot$ represents any set) satisfies the axioms of [[Probabilities|probability]]
- Given the event $B$, let us define:
$$
\mathbb{P}_{B}:\mathfrak{F}\to \mathbb{R}:\forall A\in \mathfrak{F},\mathbb{P}_{B}(A):=\mathbb{P}(A|B)
$$
    So $\mathbb{P}_{B}$ is a probability on $(\Omega,\mathfrak{F})$, so satisfies the axioms of probability


#Mathematics #Probability #Definition 