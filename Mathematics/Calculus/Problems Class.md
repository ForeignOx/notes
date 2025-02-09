## Directional Derivative
Find the directional derivative of $f=\frac{x^{2}y^{2}}{4}-2y$ in the direction $\underline{\hat{n}}=\left( \frac{3}{5},-\frac{4}{5} \right)$ at $(x,y)=(2,1)$
We need to donsider $\underline{\nabla f}\cdot  \underline{\hat{n}}$,
$$
\underline{\nabla f} =\begin{pmatrix}
f_{x}\\f_{y}
\end{pmatrix}=\begin{pmatrix}
\frac{2xy^{2}}{4}\\ \frac{2x^{2}y}{4}-2
\end{pmatrix}
$$
At $(2,1)$, $\underline{\nabla f}=(1,0)$, so
$$
\underline{\nabla f} \cdot  \underline{\hat{n}}=\begin{pmatrix}
1\\0
\end{pmatrix}\cdot \begin{pmatrix}
\frac{3}{5}\\-\frac{4}{5}
\end{pmatrix}=\frac{3}{5}
$$
## Changing Coordinates
A change of coordinates $(x,y)\to(u,v)$ is given by the relations:
$$
u=\frac{1}{2}(x^{2}+y^{2}),v=\frac{1}{2}(x^{2}-y^{2})
$$
Where $x,y>0$ and $u>v$. For an arbitrary differentiable function $f$, find expressions for $f_{x},f_{y}$ and $f_{xx}$ expressed entirely in $u$ and $v$
$$
f_{x}=\frac{ \partial f }{ \partial x }=\frac{ \partial u }{ \partial x } \frac{ \partial f }{ \partial u } +\frac{ \partial v }{ \partial x } \frac{ \partial f }{ \partial v }=x\frac{ \partial f }{ \partial u } +x\frac{ \partial f }{ \partial v } =x(f_{u}+f_{v})=\sqrt{ u+v }(f_{u}+f_{v}) 
$$
$$
f_{y}=\frac{ \partial f }{ \partial y } =\frac{ \partial u }{ \partial y } \frac{ \partial f }{ \partial u } +\frac{ \partial v }{ \partial y } \frac{ \partial f }{ \partial v } =yf_{u}-yf_{v}=\sqrt{ u-v }(f_{u}-f_{v})
$$
$$
f_{x x}=x\frac{ \partial  }{ \partial u } f_{x}+x\frac{ \partial  }{ \partial v } f_{x}=x\left( \frac{ \partial  }{ \partial u } +\frac{ \partial  }{ \partial v }  \right)f_{x}=\sqrt{ u+v }\left( \frac{ \partial  }{ \partial u } +\frac{ \partial  }{ \partial v }  \right)(\sqrt{ u+v }(f_{u}+f_{v}))
$$
$$
= \sqrt{ u+v }\left( \left(  \frac{1}{2\sqrt{ u+v }}(f_{u}+f_{v})+\sqrt{ u+v }(f_{uu}+f_{vu}) \right) +\left( \frac{1}{2\sqrt{ u+v }}(f_{u}+f_{v})+\sqrt{ u+v }(f_{uv}+f_{vv}) \right) \right)
$$
$$
\implies f_{x x}=f_{u}+f_{v}+(u+v)(f_{uu}+2f_{uv}+f_{vv})
$$
## Tangent Planes
Define the gradient $\underline{\nabla f}$ of the function $f(x,y,z)$. Calculate $\underline{\nabla f}$ in the case that 
$$
f(x,y,z)=8x^{3}y+6xy+4y^{2}z+\ln(x+y+2z)
$$
And use your answer to find the tangent plane to the surface $f(x,y,z)=2$ at the point $(x,y,z)=\left( \frac{1}{2},\frac{1}{2},0 \right)$
$$
\underline{\nabla f} =\begin{pmatrix}
24x^{2}y+6y+ \frac{1}{x+y+2z}\\8x^{3}+6x+8yz+\frac{1}{x+y+2z}\\4y^{2}+\frac{2}{x+y+2z}
\end{pmatrix}
$$
Now $\underline{\nabla f}$ is normal to the surface $f=2$ and tangent plane, what is $\underline{\nabla f}$ at the point $\left( \frac{1}{2},\frac{1}{2},0 \right)$:
$$
\underline{\nabla f} =\begin{pmatrix}
3+3+1\\1+3+1\\1+2
\end{pmatrix}=\begin{pmatrix}
7\\5\\3
\end{pmatrix}
$$
So plane with normal $(7,5,3)$ has equation $7x+5y+3z=C$, we know that $\left( \frac{1}{2},\frac{1}{2},0 \right)$ lies on the tangent plane, so
$$
\frac{7}{2}+\frac{5}{2}+0=C=6
$$
So
$$
7x+5y+3z=6
$$
## Taylor Series
Find the Taylor series for the function $f(x,y)=\frac{\ln(1+x)}{1+y}$ around the point $(2,3)$ to quadratic order
$$
f(2,3)=\frac{\ln3}{4}
$$
$$
f_{x}=\frac{1}{(1+x)(1+y)}=\frac{1}{3\times 4}=\frac{1}{12}
$$
$$
 f_{y}=-\frac{\ln(1+x)}{(1+y)^{2}}=-\frac{\ln 3}{16}
$$
$$
 f_{x x}=- \frac{1}{(1+x)^{2}(1+y)}=-\frac{1}{3^{2}\times 4}=-\frac{1}{36}
$$
$$
 f_{xy}=-\frac{1}{(1+x)(1+y)^{2}}=-\frac{1}{3\times 4^{2}}=-\frac{1}{48}
$$
$$
 f_{yy}=\frac{2\ln(1+x)}{(1+y)^{3}}=\frac{\ln 3}{32}
$$
So
$$
f(x,y)=f(x_{0},y_{0})+f_{x}(x-x_{0})+f_{y}(y-y_{0})+\frac{1}{2}(f_{xx}(x-x_{0})^{2}+2f_{xy}(y-y_{0})(x-x_{0})+f_{yy}(y-y_{0})^{2})+\dots 
$$
$$
\therefore  \frac{\ln(1+x)}{1+y}= \frac{\ln3}{4}+\frac{1}{12}(x-2)-\frac{\ln 3}{16}(y-3)+\frac{1}{2}\left( -\frac{1}{36}(x-2)^{2}-\frac{1}{24}(x-2)(y-3)+ \frac{\ln(3)}{32}(y-3)^{2} \right)+\dots
$$
![[Pasted image 20250207153716.png]]
Stationary points when
$$
f_{x}=3x^{2}-2xy+y^{2}-9=0
$$
$$
 f_{y}=-x^{2}+2xy=x(2y-x)=0
$$
From $f_{y}$, we have $x=0$ or $x=2y$. If $x=0$, from $f_{x}$:
$$
y^{2}-9=0
$$
$$
\implies y=\pm 3
$$
If $x=2y$, then
$$
12y^{2}-4y^{2}+y^{2}-9=0\implies 9y^{2}-9=0
$$
$$
\implies y=\pm 1
$$
So all stationary points at $(0,3),(0,-3),(2,1)(-2,-1)$
Now we classify
$$
H=\begin{pmatrix}
f_{x x}&f_{xy}\\f_{xy}&f_{yy}
\end{pmatrix}=\begin{pmatrix}
6x-2y&2y-2x\\2y-2x&2x
\end{pmatrix}
$$
$$
 \det(H)=(6x-2y)2x-(2y-2x)^{2}=12x^{2}-4yx-4x^{2}-4y^{2}+8xy
$$
$$
= 8x^{2}+4yx-4y^{2}
$$
At $(0,\pm 3)$, 
$$
\det(H)=-4(\pm 3)^{2}=-36<0
$$
So saddle points
At $(2,1)$,
$$
\det(H)=32+8-4=36>0
$$
$$
f_{ x x}=6x-2y=12-2=10>0
$$
So minimum point
At $(-2,-1)$, since $H$ is linear in $x$ and $y$, flipping the sign of both will just flip the sign of everything, so only $f_{  x x}=-10\leq$ so maximum is different
![[Pasted image 20250207154710.png]]
Note that since this is circle, we could use $x=\cos\theta,y=\sin\theta$ and differentiate wrt $\theta$, but we shan't
$$
f(x,y)=\ln(5+x)-\ln(5-y)
$$
$$
 g(x,y)=x^{2}+y^{2}-1=0
$$
$$
\phi=f-\lambda g=\ln(5+x)-\ln(5-y)-\lambda(x^{2}+y^{2}-1)
$$
$$
 0=\phi_{x}=\frac{1}{5+x}-2\lambda x
$$
$$
 0=\phi_{y}=\frac{1}{5-y}-2\lambda y
$$
And we have
$$
x^{2}+y^{2}=1
$$
The $\phi _x$  equation multiplies by $y$ subtract the $\phi_{y}$ equation multiplied by $x$ gives:
$$
\frac{y}{5+x}-\frac{x}{5-y}=0
$$
$$
\implies y(5-y)=x(5+x)
$$
$$
 \implies 5y-y^{2}=5x+x^{2}
$$
$$
\implies 5y-5x=x^{2}+y^{2}=1
$$
$$
 y=x+\frac{1}{5}
$$
Substituting this into the constraint:
$$
x^{2}+\left( x+\frac{1}{5} \right)^{2}=1
$$
$$
 2x^{2}+\frac{2}{5}x+\frac{1}{25}=1
$$
$$
\implies 50x^{2}+10x-24=0
$$
$$
\implies 25x^{2}+5x-12=0
$$
$$
 \implies (5x+4)(5x-3)=0
$$
So $\left( -\frac{4}{5},-\frac{3}{5} \right)$ and $\left( \frac{3}{5}, \frac{4}{5} \right)$, now
$$
f\left( -\frac{4}{5},-\frac{3}{5} \right)=\ln\left(  \frac{5+x}{5-y} \right)=\ln\left(  \frac{5-\frac{4}{5}}{5+\frac{3}{5}} \right)=\ln \left( \frac{\frac{21}{25}}{\frac{28}{25}} \right)=-\ln\left( \frac{4}{3} \right)
$$
$$
f\left( \frac{3}{5}, \frac{4}{5} \right)=\ln\left(  \frac{5+\frac{3}{5}}{5-\frac{4}{5}} \right)=\ln\left( \frac{4}{3} \right)
$$
So 
$$
-\ln\left( \frac{4}{3} \right)\leq f(x,y)\leq \ln\left( \frac{4}{3} \right)
$$
