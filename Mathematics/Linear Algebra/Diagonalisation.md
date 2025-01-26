Let $T:\mathbb{R}^{n}\to \mathbb{R}^{n}$ be a [[Linear Maps|linear mapping]], to represent it using an $n\times n$ [[Matrices|matrix]] $M$, we need to make a choice of [[Basis|basis]] for $\mathbb{R}^{n}$, usually weith standard basis [[Standard Basis Vectors|$\vec{e}_{1},\vec{e}_{2},\dots,\vec{e}_{n}$]], in a different basis, $M$ changes
## Lemma
Suppose $\vec{x}\in\mathbb{R}^{n}$ is given with respect to a standard basis as 
$$
\vec{x}=\begin{pmatrix}
x_{1}\\x_{2}\\\vdots\\x_{n}
\end{pmatrix}=x_{1}\vec{e}_{1}+x_{2}\vec{e}_{2}+\dots+x_{n}\vec{e}_{n}
$$
And $M$ is the matrix representing a linear transformation $T$ in this basis,
$$
T(\vec{x})=M\begin{pmatrix}
x_{1}\\\vdots\\x_{n}
\end{pmatrix}
$$
Suppose we instead have a different basis $\{ \vec{v}_{1},\dots,\vec{v}_{n} \}$ is a different basis, then we could write
$$
\vec{x}=\tilde{x}_{1}\vec{v}_{1}+\tilde{x}_{2}\vec{v}_{2}+\dots+\tilde{x}_{n}\vec{v}_{n}
$$
Where $\tilde{x}_{1},\tilde{x}_{2},\dots \tilde{x}_{n}\in\mathbb{R}$ such that
$$
\begin{pmatrix}
x_{1}\\ \vdots\\x_{n}
\end{pmatrix}=P\begin{pmatrix}
\tilde{x}_{1}\\\vdots\\\tilde{x}_{n}
\end{pmatrix}
$$
And $P$ is an $n\times n$ invertible "changed basis matrix", then the matrix $N$ representing the same linear map in the new basis is $N=P^{-1}MP$
Key question: is there a basis in which the matrix representation of $T$ looks as simple as possible; the best situation would be a diagonal matrix
## Diagonalisability
$A$ is said to be diagonalisable if [[Similarity Relation|$A\sim B$]], i.e. 
$$
\exists M:M^{-1}AM=D=\begin{pmatrix}
d_{1}&0&\dots&0\\0&d_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&d_{n}
\end{pmatrix}
$$
Given $A$, is it diagnoalisable? More generally, given $A$ and $B$, it $A\sim B$, now 
$$
A\sim B\implies p_{A}(t)=p_{B}(t)
$$
so similarity matrices hae the same eigenvalues, but importantly, the converse is not necessarily true:
$$
p_{A}(t)=p_{B}(t)\nRightarrow A\sim B
$$
### Example
Say $A=I$ (e.g. in $\mathbb{R}^{2}$), then $[I]=\{ I \}$ since $M^{-1}IM=I\forall M$, now consider
$$
B=\begin{pmatrix}
1&1\\0&1
\end{pmatrix}\neq I
$$
So $B\not\in[I]$, but $p_{A}(t)=(1-t)^{2}=p_{B}(t)$
### Facts about Diagonalisation
- For $A$ and $B$ to be similar, they must have the same [[Eigenvalues|eigenvalues]]
- If $A$ and $B$ have the same eigenvalues, and both are diagonalisable, then $A\sim B$. Being diagonalisable means that $A=MD_{1}M^{-1}$ and $B=ND_{2}N^{-1}$ for some diagonal matrices $D_{1},D_{2}$. But since they have the same eigenvalues, it means that $D_{1}\sim D_{2}$, so by the transitivity of $\sim$, it follows that $A\sim B$
- If $A$ is diagonalisable, but $B$ is not, then they cannot be similar. Diagonalisability of $A$ means that $A\sim D$ for some diagonal matrix $D$; if $A$ were to be similar to $B$, this would mean, by the transitivity of $\sim$, that $B\sim D$, contradicting our hypothesis
- Not all square matrices are diagonalisable; the matrix $B$ above is an example; if it was diagonalisable, it would be similar to the identity matrix, but it wasn't
- If the eigenvalues of $A$ are distinct, then $A$ is diagonalisable
- If $A$ is a real symmetric matrix, [[Transpose|$A=A^{T}$]], then $A$ is diagonalisable
___
Key Idea: find a "smart" basis, i.e. a basis of eigenvectors
### The $n\times n$ Matrix $A$ is Diagonalisable iff it has $n$ [[Linear Independence|Linearly Independent]] [[Eigenvectors|Eigenvectors]]
#### Proof
$\impliedby$:
Suppse $\{ \lambda_{1},\dots,\lambda_{n} \}$ are the eigenvalues (not distinct) and $\{ \vec{v}_{1},\dots,\vec{v}_{n} \}$ are a set of linearly independent eigenvectors for $A$. Can we diagonalise $A$?
Consider 
$$
M=\begin{pmatrix}
\vec{v}_{1}&\dots&\vec{v}_{n}
\end{pmatrix}
$$
So an $n\times n$ matrix with the eigenvectors as its columns, and let 
$$
D=\begin{pmatrix}
\lambda_{1}&0&\dots&0\\0&\lambda_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&\lambda_{n}
\end{pmatrix}
$$
We know $A\vec{v}_{1}=\lambda_{1}\vec{v}_{1},A\vec{v}_{2}=\lambda_{2}\vec{v}_{2},\dots,A\vec{v}_{n}=\lambda_{n}\vec{v}_{n}$, so computing $AM$ we get:
$$
AM=\begin{pmatrix}
A\vec{v}_{1}&A\vec{v}_{2}&\dots&A\vec{v}_{n}
\end{pmatrix}=\begin{pmatrix}
\lambda_{1}\vec{v}_{1}&\lambda_{2}\vec{v}_{2}&\dots&\lambda_{n}\vec{v}_{n}
\end{pmatrix}
$$
$$
= \begin{pmatrix}
\vec{v}_{1}&\vec{v}_{2}&\dots&\vec{v}_{n}
\end{pmatrix}\begin{pmatrix}
\lambda_{1}&0&\dots&0\\0&\lambda_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&\lambda_{n}
\end{pmatrix}=MD
$$
So $AM=MD\implies A=MDM^{-1}$ so $A\sim D$, so $A$ is diagonalisable. We know $M^{-1}$ exists since when you form a matrix out of linearly independent vectors, then its [[Determinants|determinant]] will be non-zero
$\implies$ Suppose $M^{-1}AM=D$, then $AM=MD$. Think of $M$ column by column as 
$$
M=\begin{pmatrix}
\vec{v}_{1}&\dots&\vec{v}_{n}
\end{pmatrix}
$$
So they must be linearly independent since $M$ is [[Matrix Inverses|invertible]]
## Example
Consider a Predator-Prey model in discrete time. Let $x_{n}$ be the number of owls at the end of year $n$ and $y_{n}$ be the number of mice at the end of year $n$. Owls are predators, mice are prey
A possible equation could be:
$$
x_{n+1}=0.6x_{n}+0.5y_{n}
$$
If $y_{n}$ was $\hspace{0pt}0$, then the number of owls would decrease to $0.6$ times the previous year, so they are starving
$$
y_{n+1}=-0.1x_{n}+1.2y_{n}
$$
The negative $x_{n}$ is for the mice being eaten by owls, and the $\hspace{0pt}1.2$ $y_{n}$ is for the general growth of the population
We can represent these as a matrix equation
$$
\begin{pmatrix}
x_{n+1}\\y_{n+1}
\end{pmatrix}=\begin{pmatrix}
0.6&0.5\\-0.1&1.2
\end{pmatrix}\begin{pmatrix}
x_{n}\\y_{n}
\end{pmatrix}
$$
Which can be rewritten as
$$
\vec{v}_{n+1}=M\vec{v}_{n}
$$
What we want to find is the population after $n$ years given a starting population $\vec{v}_{0}$, 
$$
\vec{v}_{1}=M\vec{v}_{0}
$$
$$
 \vec{v}_{2}=M\vec{v}_{1}=M^{2}\vec{v}_{0}
$$
Which can be extended to
$$
M^{n}\vec{v}_{n}
$$
But if $M$ were diagonal, that is easy since 
$$
M^{n}=\begin{pmatrix}
a^{n}&0\\0&b^{n}
\end{pmatrix}
$$
___
We want to solve a system of ODEs
$$
\dot{x}(t)=-x(t)+4y(t)
$$
$$
 \dot{y}(t)=-2x(t)+5y(t)
$$
Which we can write as a matrix equation:
$$
\frac{d }{dx} \begin{pmatrix}
x\\y
\end{pmatrix}=\begin{pmatrix}
-1&4\\-2&5
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
If $A$ were instead diagonal, say 
$$
A=\begin{pmatrix}
-2&0\\0&3
\end{pmatrix}
$$
The system is 
$$
\dot{x}=-2x
$$
$$
 \dot{y}=3y
$$
The solution is de-coupled and the solution is pretty easy to find as $x(t)=x_{0}e^{-2t}$, $y(t)=y_{0}e^{ 3t }$
___
If $A$ is diagonal, 
$$
A=\begin{pmatrix}
a_{1}&0&\dots&0\\0&a_{2}&\dots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\dots&a_{n}
\end{pmatrix}
$$
Then
$$
A\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}=\begin{pmatrix}
a_{1}\\0\\\vdots\\0
\end{pmatrix}=a_{1}\begin{pmatrix}
1\\0\\\vdots\\0
\end{pmatrix}
$$
$$
A\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}=\begin{pmatrix}
0\\a_{2}\\\vdots\\0
\end{pmatrix}=a_{2}\begin{pmatrix}
0\\1\\\vdots\\0
\end{pmatrix}
$$
___
If possible, diagonalise 
$$
A=\begin{pmatrix}
-1&4\\-2&5
\end{pmatrix}
$$
$$
p_{A}(t)=\det \begin{pmatrix}
-1-t&4\\-2&5-t
\end{pmatrix}=(-1-t)(5-t)+8
$$
$$
= t^{2}-4t+3=(t-1)^{1}(t-3)^{1}
$$
So $t=1$ and $t=3$ are our eigenvalues:
$$
\lambda_{1}=1,k_{1}=1
$$
$$
 \lambda_{2}=3,k_{2}=1
$$
Since the geometric multiplicities satisfy $1\leq p_{i}\leq k_{i}$, each $p_{i}$ must also be $\hspace{0pt}1$. We can also check this normally:
$$
p_{1}=\dim(V_{\lambda_{1}})=\dim(\text{ker}(A-\lambda_{1}I))=1
$$
$$
p_{2}=\dim(V_{\lambda_{2}})=\dim(\text{ker}(A-\lambda_{2}I))=1
$$
Note that this links to the [[Sums and Intersections of Vectorspaces#Direct Sums|direct sum]]:
$$
\dim(V_{\lambda_{1}})+\dim(V_{\lambda_{2}})=2=\dim(\mathbb{R}^{2})
$$
$$
\mathbb{R}^{2}=V_{\lambda_{1}}\oplus V_{\lambda_{2}}
$$
We find the eigenvectors one-by-one. Take $\lambda_{1}=1$:
$$
(A-I)\vec{v}_{1}=\vec{0}
$$
$$
\implies \begin{pmatrix}
-2&4\\-2&4
\end{pmatrix}\begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
$$
\implies -2a+4b=0
$$
So we can pick 
$$
\vec{v}_{1}=\begin{pmatrix}
2\\1
\end{pmatrix}
$$
But this is not the only choice
$$
V_{\lambda_{1}=1}=\text{ker}(A-I)=\left< \begin{pmatrix}
2\\1
\end{pmatrix} \right> 
$$
Now for the next eigenvector, take $\lambda_{2}=3$:
$$
(A-3I)\vec{v}_{2}=\vec{0}
$$
$$
\implies \begin{pmatrix}
-4&4\\-2&2
\end{pmatrix}\begin{pmatrix}
a\\b
\end{pmatrix}=\begin{pmatrix}
0\\0
\end{pmatrix}
$$
$$
\implies -4a+4b=0
$$
So we can pick:
$$
\vec{v}_{2}=\begin{pmatrix}
1\\1
\end{pmatrix}
$$
$$
V_{\lambda_{2}=3}=\text{ker}(A-3I)=\left< \begin{pmatrix}
1\\1
\end{pmatrix} \right> 
$$
Low and behold the eigenvectors are linearly independent :)
Now we diagnoalise, set
$$
M=\begin{pmatrix}
\vec{v}_{1}&\vec{v}_{2}
\end{pmatrix}=\begin{pmatrix}
2&1\\1&1
\end{pmatrix}
$$
$$
\implies M^{-1}=\begin{pmatrix}
1&-1\\-1&2
\end{pmatrix}
$$
And now we can check
$$
M^{-1}AM=\begin{pmatrix}
1&0\\0&3
\end{pmatrix}
$$
___
Solve the system of ODEs:
$$
\dot{x}=-x+4y
$$
$$
 \dot{y}=-2x+5y
$$
$$
\begin{pmatrix}
\dot{x}\\\dot{y}
\end{pmatrix}=\begin{pmatrix}
-1&4\\-2&5
\end{pmatrix}\begin{pmatrix}
x\\y
\end{pmatrix}=A\begin{pmatrix}
x\\y
\end{pmatrix}
$$
This is the same matrix as above. so let's say
$$
\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}=M^{-1}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
$$
\implies \begin{pmatrix}
x\\y
\end{pmatrix}=M\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
So we are shifting to a basis of eigenvectors of $A$
$$
\vec{x}=x\begin{pmatrix}
1\\0
\end{pmatrix}+y\begin{pmatrix}
0\\1
\end{pmatrix}=w_{1}\vec{v}_{1}+w_{2}\vec{v}_{2}
$$
Then
$$
\begin{pmatrix}
\dot{w}_{1}\\\dot{w}_{2}
\end{pmatrix}=M^{-1}\begin{pmatrix}
\dot{x}\\\dot{y}
\end{pmatrix}=MA\begin{pmatrix}
x\\y
\end{pmatrix}=M^{-1}AMM^{-1}\begin{pmatrix}
x\\y
\end{pmatrix}
$$
$$
= D\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
So our ODE has decoupled, i.e.
$$
\begin{pmatrix}
\dot{w}_{1}\\\dot{w}_{2}
\end{pmatrix}=\begin{pmatrix}
1&0\\0&3
\end{pmatrix}\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
$$
\implies \dot{w}_{1}=w_{1},\dot{w}_{2}=3w_{2}
$$
$$
 \implies w_{1}(t)=c_{1}e^{ t },w_{2}(t)=c_{2}e^{ 3t },c_{1},c_{2}\in \mathbb{R}
$$
Back to $x$ and $y$:
$$
\begin{pmatrix}
x\\y
\end{pmatrix}=M\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}=\begin{pmatrix}
\vec{v}_{1}&\vec{v}_{2}
\end{pmatrix}\begin{pmatrix}
w_{1}\\w_{2}
\end{pmatrix}
$$
$$
\implies x(t)=2c_{1}e^{ t }+c_{2}e^{ 3t },y(t)=c_{1}e^{ t }+c_{2}e^{ 3t }
$$







## Applications


#Mathematics #LinAlg 