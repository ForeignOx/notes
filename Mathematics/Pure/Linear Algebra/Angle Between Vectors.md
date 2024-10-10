Suppose $\vec{u},\vec{v}\in\mathbb{R}^n$ with $\vec{u},\vec{v}\neq \vec{0}$ then we define the angle between them to be the unique $0\leq\theta \leq \pi$ such that $\vec{u}\cdot \vec{v}=|u| |v|\cos\theta$ 
Note for $\vec{u},\vec{v}\in\mathbb{R}^n$, $\vec{u},\vec{v}\neq 0$ if $\vec{v}\cdot \vec{u}=0$, we call $\vec{u}$, $\vec{v}$ orthogonal
## Example
FInd all unit vectors $\vec{w}\in\mathbb{R}^3$ that make an angle of $\frac{\pi}{4}$ with both:
$$
\vec{u}=\begin{pmatrix}
1\\-1\\0
\end{pmatrix},\vec{v}=\begin{pmatrix}
1\\0\\1
\end{pmatrix}
$$
![[Angle Between Vectors 2024-10-10 10.45.34.excalidraw]]
Each vector will have a 'circle' of vectors around them in a cone that are $\frac{\pi}{4}$ around them, so to find the intersection of two sets of vectors, we sort of want to find the intersection of two circles, so we expect to find $\hspace{0pt}1$ vector, $\hspace{0pt}2$ vectors or no vectors (unless both vectors are the same in which case all vectors in the cone satisfy)

Suppose a solution takes the form:
$$
\vec{w}=\begin{pmatrix}
w_{1}\\w_{2}\\w_{3}
\end{pmatrix}
$$
First note:
$$
|\vec{u}|=\sqrt{ 1^{2}+(-1)^{2} }=\sqrt{ 2 },|\vec{v}|=\sqrt{ 1^{2}+1^{2} }=\sqrt{ 2 }
$$
Now
$$
\vec{u}\cdot \vec{w}=|\vec{u}| |\vec{w}|\cos\left( \frac{\pi}{4} \right)=\sqrt{ 2 }\times 1\times \frac{1}{\sqrt{ 2 }}=1
$$
$$
\vec{v}\cdot \vec{w}=|\vec{v}| |\vec{w}|\cos\left( \frac{\pi}{4} \right)=1
$$
So $w_{1}-w_{2}=1$ and $w_{1}+w_{3}=1$, $w_{1}^{2}+w_{2}^{2}+w_{3}^{2}=1$
Hence
$$
w_{1}^{2}+(w_{1}-1)^{2}+(1-w_{1})^{2}=1
$$
Solve for $w_{1}$ (it's a quadratic), then we can get $w_{2}$ and $w_{3}$
