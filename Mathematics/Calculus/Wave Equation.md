The wave equation is a [[Second Order Partial Differential Equations|second order]] [[Linear Partial Differential Equations|linear PDE]] of the form
$$
u_{tt}=c^{2}u_{x x}
$$
$$
\implies c^{2}u_{ x x}-u_{tt}=0
$$
$$
\implies M=\begin{pmatrix}
c^{2}&0\\0&-1
\end{pmatrix}
$$
$$
\implies \det(M)=-c^{2}<0
$$
So the Wave equation is a hyperbolic PDE
On the whole line, the general solution is:
$$
u(x,t)=f(x-ct)+g(x+ct)
$$
We can think of this as having two lumps $f$ and $g$, moving along a line at speed $c$ towards each other:
![[Wave Equation 2025-02-27 14.53.07.excalidraw]]