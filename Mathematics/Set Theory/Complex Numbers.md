Whenever $x\in\mathbb{R}$, $x^{2}\geq 0$. This means the equation $x^{2}+1=0$ does not have a solution in [[Real Numbers|$\mathbb{R}$]]. Historically, complex numbers arose by adding an 'imaginary' number $i$ to the reals which satisfies $i^{2}=-1$, and then calculate as if we just dealt with real numbers. A formal approach that justifies this method can be descrived as follows. We define the set $\mathbb{C}$ of complex numbers to be the [[Set Operations#Cartesian Product|cartesian product]] of $\mathbb{R}$ with itself. That is, a complex number $z\in\mathbb{C}$ is an ordered pair of real numbers
$$
z=(x,y)\in \mathbb{R}^{2}
$$
We can think of $\mathbb{R}$ as sitting inside $\mathbb{C}$ by identifying $x\in\mathbb{R}$ with $(x,0)\in\mathbb{C}$
In order to calculate with complex numbers, we need to define how to add and multiply them. This should of course extend the addtition and multiplication of real numbers via our identification. For this, let $(x_{1},y_{1}),(x_{2},y_{2})\in\mathbb{C}$ and set
$$
(x_{1},y_{1})+(x_{2},y_{2})=(x_{1}+x_{2},y_{1}+y_{2})\in \mathbb{C}
$$
And
$$
(x_{1},y_{1})\cdot(x_{2},y_{2})=(x_{1}x_{2}-y_{1}y_{2},x_{1}y_{2}+y_{1}x_{2})\in \mathbb{C}
$$
In particular, addition is defined coordinate wise, whereas multiplication is not
One can show that $\mathbb{C}$ with this addition and multiplication satisfies the axioms of addition, multiplication and distributivity of the real numbers
One can now also check that
$$
(0,1)\cdot(0,1)=(-1,0)=(0,-1)\cdot(0,-1)
$$
And now also introducd the more usual notation
$$
(x,y)=x+iy
$$
And hence
$$
i^{2}=-1=(-i)^{2}
$$
## Complex Conjugate
Let $z=x+iy\in\mathbb{C}$. THe complex conjugate of $z$, denoted $\overline{z}$, is defined as:
$$
\overline{z}=x-iy
$$
Let $z,w\in\mathbb{C}$ with $z=x+iy$. Then
- $\overline{z+w}=\overline{z}+\overline{w}$
- $\overline{z\cdot w}=\overline{z}\cdot\overline{w}$
- $\overline{\overline{z}}=z$
- $\overline{z}=z$ iff $z=x$
- $\overline{z}=-z$ iff $z=iy$
- $z\cdot\overline{z}=x^{2}+y^{2}\geq 0$, since $x$ and $y$ are real numbers
