The scalar triple product is a function in [[Vectorspace Rn|$\mathbb{R}^3$]]:
$$
\mathbb{R}^3\times \mathbb{R}^3\times \mathbb{R}^3\to \mathbb{R}
$$
$$
 (\vec{a},\vec{b},\vec{c})\mapsto[\vec{a},\vec{b},\vec{c}]
$$
Where:
$$
[\vec{a},\vec{b},\vec{c}]:=\vec{a}\cdot(\vec{b}\times \vec{c})
$$
So if:
$$
\vec{a}=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix},\vec{b}=\begin{pmatrix}
b_{1}\\b_{2}\\b_{3}
\end{pmatrix},\vec{c}=\begin{pmatrix}
c_{1}\\c_{2}\\c_{3}
\end{pmatrix}\in \mathbb{R}^3,l_{1},l_{2},l_{3}\in \mathbb{R}
$$
Then the [[Systems of Linear Equations|system of equations]]:
$$
a_{1}x+a_{2}y+a_{3}z=l_{1}
$$
$$
 b_{1}x+b_{2}y+b_{3}z=l_{2}
$$
$$
 c_{1}x+c_{2}y+c_{3}z=l_{3}
$$
Has a unique solution iff $[\vec{a},\vec{b},\vec{c}]\neq 0$
## Note
$$
[\vec{a},\vec{b},\vec{c}]=\det(\vec{a}\,\vec{b}\,\vec{c})
$$
where $(\vec{a}\,\vec{b}\,\vec{c})$ is a $3\times 3$ [[Matrices|matrix]]
## Invariance Under Cyclic Permutation
If $\vec{a},\vec{b},\vec{c}\in\mathbb{R}^3$ then:
$$
[\vec{a},\vec{b},\vec{c}]=[\vec{b},\vec{c},\vec{a}]=[\vec{c},\vec{a},\vec{b}]
$$
$$
 =-[\vec{b},\vec{a},\vec{c}]=-[\vec{a},\vec{c},\vec{b}]=-[\vec{c},\vec{b},\vec{a}]
$$
### Proof
$$
[\vec{a},\vec{b},\vec{c}]=\vec{a}\cdot \left( \begin{pmatrix}
b_{1}\\ b_{2}\\b_{3}
\end{pmatrix}\times \begin{pmatrix}
c_{1}\\c_{2}\\c_{3}
\end{pmatrix} \right)=\begin{pmatrix}
a_{1}\\a_{2}\\a_{3}
\end{pmatrix}\cdot \begin{pmatrix}
b_{2}c_{3}-b_{3}c_{2}\\b_{3}c_{1}-b_{1}c_{3}\\b_{1}c_{2}-b_{2}c_{1}
\end{pmatrix}
$$
$$
= a_{1}b_{2}c_{3}+a_{2}b_{3}c_{1}+a_{3}b_{1}c_{2}-a_{1}b_{3}c_{2}-a_{2}b_{1}c_{3}-a_{3}b_{2}c_{1}
$$
We can see that the subscripts are in fact undergoing cyclic permutation, so we can see that there will be invariance if you interchange the $a$'s, $b$'s and $c$'s cyclically, then if you change the order, then we are using the second half of the equation and the negative signs switch
