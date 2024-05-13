To convert axes we use:
$$
J(u,v)=\frac{ \partial (x,y) }{ \partial (u,v) } =\det\left(
\begin{matrix}
\frac{ \partial x }{ \partial u } &\frac{ \partial x }{ \partial v } \\
\frac{ \partial y }{ \partial u } & \frac{ \partial y }{ \partial v } 
\end{matrix} \right)=\frac{ \partial x }{ \partial y } \cdot \frac{ \partial y }{ \partial v } -\frac{ \partial x }{ \partial v } \cdot \frac{ \partial y }{ \partial u } 
$$

## Converting to polar
It is often useful to use polar coordinates instead of cartesian coordinates
$x=r\cos\theta$, $y=r\sin\theta$, $r^{2}=x^{2}+y^{2}$, $\frac{ \partial x }{ \partial \theta }=r\sin\theta$, $\frac{ \partial x }{ \partial r }=\cos\theta$, $\frac{ \partial y }{ \partial \theta }=r\cos\theta$, $\frac{ \partial y }{ \partial r }=\sin\theta$
$$
J(\theta,r)=r\sin ^{2}\theta -r\cos ^{2}\theta=-r(\sin ^{2}\theta+\cos ^{2}\theta)=-r
$$

