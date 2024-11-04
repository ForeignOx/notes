We consider a [[Systems of Linear Equations|system of linear equations]] with $m$ equations in $n$ unkowns ($x_{i}$'s are the unknowns)
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n}=b_{1}
$$
$$
a_{21}x_{1}+a_{22}x_{2}+\dots+a_{2n}x_{n}=b_{2}
$$
$$
\vdots
$$
$$
a_{m1}x_{1}+a_{m2}x_{2}+\dots+a_{mn}x_{n}=b_{m}
$$
Which can be written:
$$
\sum_{ j=1} ^{ n}   a_{ij}x_{j}=b_{i}
$$
For $i=1,\dots,m$
The way to solve this is to epress the system as an [[Augmented Matrices|augmented matrix]], then perform operations known as ERO's (Elementary Row Operations) to the matrix without changing the solution set, which will turn the augmented matrix into RREF (Row Reduced Echolon Form) using the Gauss-Jordan algorithm, which allows us to then read off the solution set
Note that non-leading 1's correspond to free variables
If $A=(a_{ij})_{m\times n}$, then $A$ is known as the matrix of coefficients:
$$
A=\begin{pmatrix}
a_{11}&a_{12}&\dots&a_{1j}&\dots& a_{1n}\\a_{21}&a_{22}&\dots&a_{2j}&\dots& a_{2n}\\\vdots&\vdots&&\vdots& & \vdots\\a_{i1}&a_{i2}&\dots&a_{ij}&\dots& a_{in}\\\vdots&\vdots&&\vdots& & \vdots\\a_{n1}&a_{m2}&\dots&a_{mj}&\dots& a_{mn}
\end{pmatrix}
$$
$$
\vec{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\x_{i}\\\vdots\\x_{n}
\end{pmatrix},\vec{b}=\begin{pmatrix}
b_{1}\\b_{2}\\\vdots\\b_{i}\\\vdots\\b_{n}
\end{pmatrix}
$$
The system of equations is:
$$
A\vec{x}=\vec{b} 
$$
We are thus looking for 
$$
\{ \vec{x}\in \mathbb{R}^{n}\mid A\vec{x}=\vec{b} \}
$$
If $\vec{b}=\vec{0}$, we call the system homogeneous, if $\vec{b}\neq  \vec{0}$, we call it inhomogeneous, if $\vec{b}$ is homogeneous, there is always a solution $\vec{x}=0$
So we make the augmented matrix of the system is $(A|\vec{b})$:
$$
(A|\vec{b})=\left(\begin{array}{cccccc|c}
a_{11}&a_{12}&\dots&a_{1j}&\dots& a_{1n}&b_{1}\\a_{21}&a_{22}&\dots&a_{2j}&\dots& a_{2n}&b_{2}\\\vdots&\vdots&&\vdots& & \vdots&\vdots\\a_{i1}&a_{i2}&\dots&a_{ij}&\dots& a_{in}&b_{i}\\\vdots&\vdots&&\vdots& & \vdots&\vdots\\a_{n1}&a_{m2}&\dots&a_{mj}&\dots& a_{mn}&b_{n}
\end{array}\right)
$$
## Example
$$
x+y+w=1
$$
$$
x-w=0
$$
$$
x+y+z-w=2
$$
$$
x+z+w=3
$$
Is a system of equations which can be written as:
$$
1\times x+1\times y+0\times z+1\times w=1
$$
$$
1\times x+0\times y+0\times z+(-1)\times w=0
$$
$$
1\times x+1\times y+1\times z+(-1)\times w=2
$$
$$
1\times x+0\times y+1\times z+1\times w=3
$$
Which can be written as the augmented matrix:
$$
\left(
\begin{array}{cccc|c}
1&1&0&1&1\\
1&0&0&-1&0\\
1&1&1&-1&2\\
1&0&1&1&3
\end{array}
\right)
$$
## Lemma
Let $A\in M_{n}(\mathbb{R})$ and $\vec{v}\in\mathbb{R}^{n},\vec{v}\neq 0$ such that $A\vec{v}=\vec{0}$, then $A$ is not [[Matrix Inverses|invertible]] i.e. is singular
If $A\in M_{n}(\mathbb{R})$ is invertible, then the system $A\vec{x}=\vec{b}$ has a unique solution
### Proof
Assume $A^{-1}$ exists, then:
$$
\vec{v}=I_{n}\vec{v}=A^{-1}(A\vec{v})=A^{-1}\vec{0}=\vec{0}
$$
Which is a contradiction to $\vec{v}\neq  \vec{0}$
$$
A\vec{x}=\vec{b}\iff A^{-1}A\vec{x}=A^{-1}\vec{b}\iff \vec{x}=A^{-1}\vec{b}
$$
And $A^{-1}\vec{b}$ exists and is unique
## Gauss-Jordan Algorithm
### EROs
Each ERO is a function:
$$
M_{m\times n}(\mathbb{R})\to M_{m\times n}(\mathbb{R})
$$
They are:
- $P_{rs}$ interchanges row $r$ with row $s$ (the $P$ stands for 'permute')
- $M_{r}(\lambda)$ multiplies the elements in the $r$th row by $\lambda \neq 0$
- $A_{rs}(\lambda)$ adds $\lambda \in\mathbb{R}$ times the $r$th row to the $s$th row

#Mathematics #LinAlg 