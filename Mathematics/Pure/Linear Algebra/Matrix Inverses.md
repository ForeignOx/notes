Let [[Matrices|$A\in M_{n}(\mathbb{R})$]], we say that $A$ is invertible iff there exists $B\in M_{m}(\mathbb{R})$ such that:
$$
AB=I=BA
$$
If such a $B$ exists, we call it the inverse of $A$, and denote it $A^{-1}$
## Properties
- A matrix has at most $\hspace{0pt}1$ inverse, so if an inverse exists, it must be unique
### Proof
Suppose $B,C$ are inverrses for a matrix $A\in M_{n}(\mathbb{R})$, so
$$
B=BI_{n}=B(AC)=(BA)C=I_{n}C=C
$$
So $B$ and $C$ must be equal
# 
___
- If $A,B \in M_{n}(\mathbb{R})$ are invertible, then $AB$ is also invertible: $(AB)^{-1}=B^{-1}A^{-1}$
- If $A\in M_{n}(\mathbb{R})$ is invertible, then so is [[Transpose|$A^{t}$]]: $(A^{t})^{-1}=(A^{-1})^{t}$
### Proof
$$
A^{t}(A^{-1})^{t}=(A^{-1}A)^{t}=(I_{n})^{t}=I_{n}
$$
And
$$
(A^{-1})^{t}A^{t}=(AA^{-1})^{t}=(I_{n})^{t}=I_{n}
$$
So $(A^{-1})^{t}=(A^{t})^{-1}$
# 
___
- If $A,B\in M_{n}(\mathbb{R})$ and $AB=I_{n}$, then $BA=I_{n}$, $B=A^{-1}$ and $A=B^{-1}$

## More Stuff
Consider the [[Systems of Linear Equations|linear system]] $A\vec{x}=\vec{b}$, $A\in M_{m\times n}(\mathbb{R})$


#Mathematics #LinAlg #Definition