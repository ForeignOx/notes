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
Have a unique solution iff the [[Scalar Triple Product|scalar triple product]] is non-zero from what we know about [[Lines in R3|lines in $\mathbb{R}^3$]], so iff
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
