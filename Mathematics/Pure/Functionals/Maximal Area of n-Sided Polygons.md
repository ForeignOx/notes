Let us consider the product of two numbers $x$, $y$, whose sum is constant; it is known that this product is a maximum when the two numbers are equal. This can be converted to geometrical language by saying that among all the rectangles which have the sum of two consecutive sides constant, and therefore have a constant perimeter, the square is the one of maimum area
We can then extend this to the ore general problem of determining, among all planar polygons of $n$ sides whose permeter is constant, the one of maximum area whill be the regular polygon of $n$ sides
If we denote the $2n$ coordinates of the $n$ vertices of the polygon by $(x_{1},y_{1}),(x_{2},y_{2}),\dots,(x_{n},y_{n})$, the quantity to be made a maximum is the area $A$, given by the expression:
$$
A=\frac{1}{2}\sum_{ i=1} ^{ n}  \left| \begin{matrix}
x_{i}&x_{i+1}\\y_{i}&y_{i+1}
\end{matrix}\right|=\frac{1}{2}\sum_{ i=1} ^{ n}  (x_{i}y_{i+1}-y_{i}x_{i+1})=\frac{1}{2}\sum_{ i=1} ^{ n}  (x_{i}(y_{i+1}-y_{i})-y_{i}(x_{i+1}-x_{i}))
$$
$$
= \frac{1}{2}\sum_{ i=1} ^{ n}  (x_{i}\Delta y_{i}-y_{i}\Delta x_{i})
$$
A function, in this case, of the $2n$ variables $x_{i},y_{i}$ with:
$$
\sum_{ i=1} ^{ n}  \sqrt{ \Delta x_{i}^{2}+\Delta y_{i}^{2} }=k,k\in \mathbb{R}
$$
And in which:
$$
x_{n+1}=x_{1}
$$
$$
y_{n+1}=y_{1}
$$
$$
\Delta x_{i}=x_{i+1}-x_{i}
$$
$$
 \Delta y_{i}=y_{i+1}-y_{i}
$$
But if we pass from the case of a polygon of constant perimeter to the more general problem of determining, among all the closed curves $C$ of a given length $l$, the one that includes the maximum area $A$ (the circle), the quantity $A$ that we have to consider is given by the formula:
$$
A=\frac{1}{2}\int _{C}(xdy-ydx)
$$
With:
$$
\int _{C}\sqrt{ dx^{2}+dy^{2} }=l,l\in n\mathbb{R}
$$
And thus no longer depends on a finite number of variables, but on the values of the coordinates of all the infinite number of points of the line $C$. Instead of a problem of the ordinary differential calculus on maxima and minima, in which we have to determine a certain finite number of unknown quantities, we have a problem of the calculus of variations, in which the unknown is a [[functions|function]] (its values for all the points of the [[intervals|interval]] considered) or a curve (the coordinates of all its points)
In the case of the polygon of $n$ sides it is sufficient to find quantities $(x_{1},y_{1}),(x,y_{2}),\dots,(x_{n},y_{n})$, depending on the index $i$, discontinuous and variable for integral values from $\hspace{0pt}1$ to $n$, in order to determine the polygon itself. In the case of any closed curve $C$, however, it will be necessary, in order to etermine it, to give the coordinates $x$ and $y$ of all its points
$$
x=x(t),y=y(t)
$$
$$
x(b)=x(a),y(b)=y(a)
$$
In which now the quantities $x,y$ depend on the parameter $t$ which varies ontinuously in a certain intervl $(a,b)$; this continuous parameter $t$ takes the place of the dicontinuous index $i$, so corresponding to the formulas containing sums with respect to the index $i$, we get instead the formulae containing integrals in which we may take the parameter $t$ as the variable of integration
