A determinant is a [[Functions|funciton]]:
$$
\det:M_{n}(\mathbb{R})\to \mathbb{R}
$$
$$
 A\mapsto \det(A)=|A|
$$
This determines whether a [[Matrices|matrix]] is [[Matrix Inverses|invertible]]:
$A$ is invertible "non-singular" iff $\det(A)\neq 0$
## Guess the Definition :)
If $n=1$, we can guess:
$$
\det((a))=a
$$
___
$n=2$ we can show that if
$$
A=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}
$$
is invertible iff $ad-bc\neq 0$
So:
$$
\det \begin{pmatrix}
a&b\\c&d
\end{pmatrix}=ad-bc
$$
___
$n=3$, suppose we write:
$$
A=\begin{pmatrix}
a_{1}&a_{2}&a_{3}\\b_{1}&b_{2}&b_{3}\\c_{1}&c_{2}&c_{3}
\end{pmatrix}
$$
Say we have:
$$
\vec{a}=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix},\vec{b}=\begin{pmatrix}
b_{1}\\b_{2}\\b_{3}
\end{pmatrix},\vec{c}=\begin{pmatrix}
c_{1}\\c_{2}\\c_{3}
\end{pmatrix}
$$
$A$ is invertible iff $A\vec{x}=\vec{0}$ as shown in this [[Gauss-Jordan Elimination#Theorem|theorem]], so it is invertible iff:
$$
a_{1}x+a_{2}y+a_{3}z=0
$$
$$
 b_{1}x+b_{2}y+b_{3}z=0
$$
$$
c_{1}x+c_{2}y+c_{3}z=0
$$
Have a unique solution iff the [[Scalar Triple Product|scalar triple product]] is non-zero from what we know about [[Points in R3|points in $\mathbb{R}^3$]], so iff
$$
\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix}\cdot \begin{pmatrix}
b_{2}c_{3}-b_{3}c_{2}\\b_{3}c_{1}-b_{1}c_{3}\\b_{1}c_{2}-b_{2}c_{1}
\end{pmatrix}\neq 0
$$
$$
 \iff a_{1}\det \begin{pmatrix}
b_{2}&b_{3}\\c_{2}&c_{3}
\end{pmatrix}-a_{2}\det \begin{pmatrix}
b_{1}&b_{3}\\c_{1}&c_{3}
\end{pmatrix}+a_{3}\det \begin{pmatrix}
b_{1}&b_{2}\\c_{1}&c_{2}
\end{pmatrix}\neq 0
$$
___
## Recursive Definition
We can see that these are sort of following a pattern, that for the first row, you multiply the first element by the determinant of the matrix you obtain by ignoring the row and column of that element, then alternate negatives and positives
Based on this, we can give an inductive definition of a determinant:
Let $A=(a_{ij})\in M_{n}(\mathbb{R})$
For $1\leq r,s\leq n$, we let $A_{r,s}$ be the $(r,s)$th minor of $A$, which is the $(n-1)\times (n-1)$ matrix obtained by deleting the $r$th row and $s$th column of $A$
Let $\det(A_{r,s})$ be the $(r,s)$th unsigned cofactor of $A$, then $(-1)^{r+s}\det(A_{r,s})$ is the signed cofactor
Using this we can inductively define $\det A$ by setting:
$$
\det A=\sum_{ j=1} ^{ n} (-1)^{1+j} a_{1j}\det(A_{1,j})
$$
### Proposition
If $A\in M_{n}(\mathbb{R})$ and $1\leq i\leq n$, then we can in fact expand on any row (not just the first)
$$
\det(A)=\sum_{ j=1} ^{ n}  (-1)^{i+j}a_{ij}\det(A_{i,j})
$$
#### Proof
Nasty (see notes)
## Fundamenta Poperties of the Determinant
The determinant is the unique function that satisfies these properties
Let $A\in M_{n}(\mathbb{R})$, let $\vec{a_{r}}$ be the $r$th row vector of $A$:
$$
\vec{a_{r}}=\begin{pmatrix}
a_{r_{1}}&a_{r_{2}}&\dots&a_{rn}
\end{pmatrix}
$$
So
$$
A=\begin{pmatrix}
\vec{a_{1}}\\\vec{a_{2}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}
$$
The properties are:
- $\det(I_{n})=1$
- $\det(M_{r}(\lambda)A)=\lambda \det(A)$, where $M_{r}(\lambda)$ is the [[Gauss-Jordan Elimination|ERO]] 
 $$
\det(M_{r}(\lambda)A)=\det \begin{pmatrix}
\vec{a_{1}}\\\vdots\\\lambda\vec{a_{r}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}=\lambda \det\begin{pmatrix}
\vec{a_{1}}\\\vdots\\\vec{a_{r}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}=\lambda \det(A)
$$
- For any vector $\vec{b_{r}}$, we have
$$
\det\begin{pmatrix}
\vec{a_{1}}\\\vdots\\\vec{a_{r}}+\vec{b_{r}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}=\det\begin{pmatrix}
\vec{a_{1}}\\\vdots\\\vec{a_{r}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}+\det\begin{pmatrix}
\vec{a_{1}}\\\vdots\\\vec{b_{r}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}
$$
    Combining this with the previous one we have linearity in each row
- $\det(P_{rs}A)=-\det A$ where $P_{rs}$ is the ERO swapping $r$th and $s$th rows of $A$
- If $A$ has two equal (or even collinear) rows then $\det (A)=0$
- $\det(A)=0$ if $A$ has a row of zeroes
- $\det(A_{rs}(\lambda)A)=\det A$:
$$
\det(A_{rs}(\lambda)A)=\det\begin{pmatrix}
\vec{a_{1}}\\\vdots\\\vec{a_{r}}\\\vdots\\\vec{a_{s}}+\lambda  \vec{a_{r}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}=\det\begin{pmatrix}
\vec{a_{1}}\\\vdots\\\vec{a_{r}}\\\vdots\\\vec{a_{s}}\\\vdots\\\vec{a_{n}}
\end{pmatrix}=\det(A)
$$
### Proof
#### First Property:
Induction on $n$
Let $n=1$, $\det(1)=1$ so base case is true
Also, expanding $\det(I_{n})$ along the top row gives:
$$
\det(I_{n})=(I_{n})_{11}(-1)^{1+1}\det(I_{n-1})=\det(I_{n-1})
$$
Since all other terms are $\hspace{0pt}0$, so proved by induction
#### Second Property
Expand along $r$th row:
$$
\det(M_{r}(\lambda)A)=\sum_{ j=1} ^{ n}  (-1)^{r+j}\lambda a_{rj}\det(A_{r,j})
$$
And note that deleting the $r$th row of the matrix $M_{r}(\lambda)A$ gives the same matrix as doing the same to $A$,