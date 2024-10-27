The partin theorem is also known as the law of total probability
Let $E_{1},E_{2},\dots$ be a [[Partition|partition]] or [[Sample Spaces|$\Omega$]], then for any [[Events|event]] $A$, we have:
$$
\mathbb{P}(A)=\sum_{ i=1} ^{ k}\mathbb{P}(E_{i})\mathbb{P}(A|E_{i})  
$$
## Proof
![[Partition Theorem 2024-10-25 14.15.24.excalidraw]]
Since $E_{i}$'s form a partition, $(A\cap E_{i})\cap(A\cap E_{j})=\emptyset$ for all $i\neq j$, so we can use the third axiom of probability to get:
$$
\mathbb{P}(A)=\sum_{ i=1} ^{ k} \mathbb{P}(A\cap E_{i}) 
$$
Using $\mathbb{P}(A\cap B)=\mathbb{P}(B)\mathbb{P}(A|B)$, we can get:
$$
\mathbb{P}(A)=\sum_{ i=1} ^{ k}\mathbb{P}(E_{i})\mathbb{P}(A|E_{i})  
$$
## Example
There are $\hspace{0pt}3$ machines $A$, $B$, and $C$, $10\%$ of the components produced by $A$ are faulty, $20\%$ of the components produced by $B$ are faulty, $30\%$ of the components produced by $C$ are faulty
Equal number of components are collected from each machine. One pomponent is selected at random. Find $\mathbb{P}(\text{component is faulty})$
Let $F:=\{ \text{the component is fauly} \}$, $M_{A}:=\{ \text{component comes from }A \}$, similarly define $M_{B},M_{C}$
$$
\mathbb{P}(M_{A})=\mathbb{P}(M_{B})=\mathbb{P}(M_{C})=\frac{1}{3}
$$
$$
\mathbb{P}(F|M_{A})=\frac{10}{100}, \mathbb{P}(F|M_{B})=\frac{20}{100}, \mathbb{P}(F|M_{C})=\frac{30}{100}
$$
By partition theorem:
$$
\mathbb{P}(F)=\mathbb{P}(M_{A})\mathbb{P}(F|M_{A})+\mathbb{P}(M_{B})\mathbb{P}(F|M_{B})+\mathbb{P}(M_{C})\mathbb{P}(F|M_{C})
$$
$$
= \frac{1}{3}\left( \frac{10+20+30}{100} \right)=0.2
$$

#Mathematics #Probability #Theorem  