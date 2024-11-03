[[Differentiation|Differentiating]] a multivariable [[Functions|function]] with respect to a variable (usually) means that you treat all other variables as constants and differentiate normally
The partial derivative of $f$ with respect to $x$ can be written:
$$
\frac{ \partial f }{ \partial x } =f_{x}(x,y,\dots)=\lim_{ h \to 0 } \frac{f(x+h,y,\dots)-f(x,y,\dots)}{h}
$$
We can take partial derivatives of partial derivatives, to get 2nd partial deribatives, such as:
$$
\frac{ \partial^{2}f }{ \partial x^{2} } =\frac{ \partial  }{ \partial x } \left( \frac{ \partial f }{ \partial x }  \right)=f_{xx}
$$
$$
 \frac{ \partial^{2}f }{ \partial x\partial y }=\frac{ \partial  }{ \partial x } \left( \frac{ \partial y }{ \partial y }  \right) =f_{yx}
$$
(note that notationally, some places denote it $f_{xy}$ instead)
## Two Variables
We can consider $f(x,y)$ as the height of a function over the $xy$-plane
![[Partial Differentiation 2024-11-01 15.29.51.excalidraw]]
We can now think of the rate of change of $f(x,y)$ as we vary $x$ or $y$, keeping the other fixed
## Example
Let $f(x,y)=x^{2}y^{3}-\sin x\cos y-y$, then
$$
\frac{ \partial f }{ \partial x } =2xy^{3}-\cos x\cos y
$$
$$
\frac{ \partial f }{ \partial y } =3x^{2}y^{2}+\sin x\sin y-1
$$
$$
\frac{ \partial^{2}f }{ \partial x^{2} } =2y^{3}+\sin x\cos y
$$
$$
 \frac{ \partial^{2} f }{ \partial y^{2} }=6x^{2}y+\sin x\cos y
$$
$$
 \frac{ \partial^{2}f }{ \partial x\partial y }=6xy^{2}+\cos x\sin y
$$
$$
\frac{ \partial^{2} f }{ \partial y\partial x }=6xy^{2}+\cos x\sin y
$$
Note the last two are equal, but that is not generally the case, but is true is $f$ and all 1st and 2nd partial derivatives are [[Continuity|continuous]] (Clairaut's theorem)



#Mathematics #Calculus