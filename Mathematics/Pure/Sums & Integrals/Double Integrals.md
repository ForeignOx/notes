Double integrals can be used to find volumes, so instead of integrating over an interval, you integrate over a region (such as the x-y plane), we write this like so:
$$
\iint_{R}f(x,y)dydx=\iint_{R}f(x,y)dA
$$
![[Double Integrals 2024-02-21 15.22.15.excalidraw]]
To find a volume you essentially take a sum of areas and take the limit of these areas, which is an integral

$$
A_{i}=\int _{f_{l}(x_{i})}^{f_{u}(x_{i})}f(x,y) \, dy 
$$
$$
V=\lim_{ \Delta x \to 0 } \sum_{ i=1} ^{ n}  A_{i}\Delta x=\lim_{ \Delta x \to 0 } \sum_{ i=1} ^{ n}  \int _{f_{l}(x_{i})}^{f_{u}(x_{i})}f(x,y) \, dy \Delta x
$$
Since $\Delta x=\frac{b-a}{2}$
$$
=\int ^{b}_{a} \int _{f_{l}(x_{i})}^{f_{u}(x_{i})}f(x,y) \, dy  \, dx =\iint_{R}f(x,y)dA
$$

Note that:
$$
\int ^{b}_{a} \int _{c}^{d}f(x,y) \, dy  \, dx =\int _{c}^d \int ^{b}_{a} f(x,y) \, dx  \, dy   
$$
## Examples of Regions
### Rectangular regions
![[Double Integrals 2024-02-21 15.33.49.excalidraw]]
$$
V=\iint_{R}f(x,y)dA , R=\{(x,y):a\leq x\leq b, c\leq y\leq d\}=\int ^{b}_{a} \int _{c}^d f(x,y) \, dy  \, dx
$$
#### Example
$$
V=\iint_{R}2y-3x^{2}y^{2} dA, R= \{(x,y)|0\leq x\leq 1, 0\leq y\leq 2\}
$$
![[Pasted image 20240221173822.png]]
$$
V=\int _{0}^{2}\int _{0}^{1}2y-3x^2y^{2} \, dx  \, dy=\int_{0}^{2} [2yx-y^{2}x^{3}]^{1}_{0} \, dy  
$$
$$
=\int _{0}^{2}2y-y^{2} \, dy= \left[ y^{2}-\frac{y^{3}}{3} \right]_{0}^{2}=4-\frac{8}{3}=\frac{4}{3}
$$
### Bounded by 1 function
![[Double Integrals 2024-02-21 17.34.29.excalidraw]]
$$
V=\iint_{R}f(x,y)dA , R=\{(x,y):a\leq x\leq b, c\leq y\leq f(x)\}=\int ^{b}_{a} \int _{c}^{f(x)} f(x,y) \, dy  \, dx
$$
#### Example
$$
V=\iint_{R}4+2x-y^{2}\, dA, R=\left\{ (x,y):1\leq x\leq 3, 0\leq y\leq \left( x-\frac{3}{2}\right)^{2}+2  \right\}=\int _{1}^{3}\int_{0}^{ \left( x-\frac{3}{2}\right)^{2}+2} 4+2x-y^{2} \, dy  \, dx
$$
![[Pasted image 20240221180919.png]]
$$
=\int _{1}^{3}[(4+2x)y-y^{2}]_{0}^{\left( x-\frac{3}{2}\right)^{2}+2} \, dx =\int _{1}^{3}(4+2x)\left(\left( x-\frac{3}{2}\right)^{2}+2\right)-\left( \left( x-\frac{3}{2}\right)^{2}+2\right)^{2} \, dx 
$$
$$
=\frac{1139}{40}
$$

### Bounded by 2 functions
![[Double Integrals 2024-02-21 18.18.20.excalidraw]]
$$
V=\iint_{R}f(x,y)dA, R=\{(x,y):f_{l}(y)\leq x\leq f_{u}(y), a\leq y\leq b\} = \int ^{b}_{a} \int _{f_{l}(y)}^{f_{u}(y)}f(x,y) \, dx  \, dy  
$$
#### Example
$$
V=\iint_{R}e^x+y-x^3+2\,dA, R=\left\{ (x,y):0\leq x\leq 4, \frac{1}{2}x\leq y\leq \frac{3}{2}x \right\}
$$
$$
=\int _{0}^{4}\int _{\frac{1}{2}x}^{\frac{3}{2}x}e^{x}+y-x^{3}+2 \, dy  \, dx 
$$
![[Pasted image 20240221184336.png]]
$$
=\int _{0}^{4}\left[ (e^{ x }-x^{3})y+\frac{y^{2}}{2} \right]_{\frac{1}{2}x}^{3/2x} \, dx 
$$
$$
=\int _{0}^{4} \left( \frac{3}{2}x(e^{ x }-x^{3})+\frac{\left( \frac{3}{2}x \right)^{2}}{2} \right)-\left( \frac{1}{2}x(e^{ x }-x^{3})+\frac{\left( \frac{1}{2}x \right)^{2}}{2} \right) \, dx =3e^{ 4 }-\frac{2737}{15}
$$
### Bounded by 4 functions
![[Double Integrals 2024-02-21 20.00.20.excalidraw]]
This is not possible using the above methods, so you need to re-write the axes so that they are linear, to do this you need to use the [[Jacobian Transformation]]:
$$
\iint_{R}f(x,y) \, dA_{(x,y)}=\iint_{S}f(x(u,v),y(u,v)) |J(u,v)| \, dA_{u,v}
$$
### Example
$$
V=\iint_{R} e^{ xy }dA, R=\text{Bounded by}\begin{cases}
y=\frac{1}{2}x \\ y=x \\y=\frac{1}{x} \\y=\frac{2}{x}
\end{cases}
$$
![[Pasted image 20240221201443.png]]
Let $v=xy$, $u=\frac{y}{x}$, $\therefore y=\sqrt{ uv }$, $x=\sqrt{ \frac{v}{u} }$, $\frac{ \partial x }{ \partial u }=-\frac{v}{2u^{2}\sqrt{ \frac{v}{u} }}$, $\frac{ \partial x }{ \partial v }=\frac{1}{2u\sqrt{ \frac{v}{u} }}$, $\frac{ \partial y }{ \partial u }=\frac{v}{2\sqrt{ uv }}$, $\frac{ \partial y }{ \partial v }=\frac{u}{2\sqrt{ uv }}$
$$
\implies J(u,v)=-\frac{1}{4u}-\frac{1}{4u}=-\frac{1}{2u}
$$
$$
\implies V=\iint_{S}e^{ xy } \, |J(u,v)|\,dA_{u,v}
$$
New bounds, $\frac{1}{2}\leq u\leq 1, 1\leq v\leq 2$
$$
\implies V=\int _{\frac{1}{2}}^{1}\int _{1}^{2} \frac{e^{ v }}{2u} \, dv  \, du =\frac{\ln 2}{2}(e^{2}-e)
$$

#Mathematics