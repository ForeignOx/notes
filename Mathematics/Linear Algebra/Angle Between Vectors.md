Suppose $\underline{u},\underline{v}\in\mathbb{R}^n$ with $\underline{u},\underline{v}\neq \underline{0}$ then we define the angle between them to be the unique $0\leq\theta \leq \pi$ such that $\underline{u}\cdot \underline{v}=|u| |v|\cos\theta$ 
Note for $\underline{u},\underline{v}\in\mathbb{R}^n$, $\underline{u},\underline{v}\neq 0$ if $\underline{v}\cdot \underline{u}=0$, we call $\underline{u}$, $\underline{v}$ orthogonal
## Example
FInd all unit vectors $\underline{w}\in\mathbb{R}^3$ that make an angle of $\frac{\pi}{4}$ with both:
$$
\underline{u}=\begin{pmatrix}
1\\-1\\0
\end{pmatrix},\underline{v}=\begin{pmatrix}
1\\0\\1
\end{pmatrix}
$$
![[Angle Between Vectors 2024-10-10 10.45.34.excalidraw]]
Each vector will have a 'circle' of vectors around them in a cone that are $\frac{\pi}{4}$ around them, so to find the intersection of two sets of vectors, we sort of want to find the intersection of two circles, so we expect to find $\hspace{0pt}1$ vector, $\hspace{0pt}2$ vectors or no vectors (unless both vectors are the same in which case all vectors in the cone satisfy)

Suppose a solution takes the form:
$$
\underline{w}=\begin{pmatrix}
w_{1}\\w_{2}\\w_{3}
\end{pmatrix}
$$
First note:
$$
|\underline{u}|=\sqrt{ 1^{2}+(-1)^{2} }=\sqrt{ 2 },|\underline{v}|=\sqrt{ 1^{2}+1^{2} }=\sqrt{ 2 }
$$
Now
$$
\underline{u}\cdot \underline{w}=|\underline{u}| |\underline{w}|\cos\left( \frac{\pi}{4} \right)=\sqrt{ 2 }\times 1\times \frac{1}{\sqrt{ 2 }}=1
$$
$$
\underline{v}\cdot \underline{w}=|\underline{v}| |\underline{w}|\cos\left( \frac{\pi}{4} \right)=1
$$
So $w_{1}-w_{2}=1$ and $w_{1}+w_{3}=1$, $w_{1}^{2}+w_{2}^{2}+w_{3}^{2}=1$
Hence
$$
w_{1}^{2}+(w_{1}-1)^{2}+(1-w_{1})^{2}=1
$$
Solve for $w_{1}$ (it's a quadratic), then we can get $w_{2}$ and $w_{3}$

#Mathematics #LinAlg 