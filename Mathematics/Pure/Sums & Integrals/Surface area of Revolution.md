We can approximate surface area of a surface of revolution by taking surface areas of smaller frustums.
![[Pasted image 20240131183153.png]]
The formula for curved area of a frustum is:
$$
A_{F}=\pi(r_{1}+r_{2})l
$$
Let $r_{1}=y_{i-1}$, and $r_{2}=y_{i}$, $l=len(P_{i-1},P_{i})$, therefore, using the method to find length in [[Arc Length|arc length]] the area of one element is:
$$
A_{i}=\pi(f(x_{i})+f(x_{i-1}))\sqrt{ 1+f'(x_{i}^*)^{2} }\Delta x
$$
$$
A_{approx}= \sum_{i=1}^nA_{i}=\sum_{i=1}^n 2\pi f(x_{i}^*)\sqrt{ 1+f'(x_{i}^*)^{2} }\Delta x
$$
$$
\implies A=\lim_{ n \to \infty } \sum_{i=1}^n 2\pi f(x_{i}^*)\sqrt{ 1+f'(x_{i}^*)^{2} }\Delta x
$$
$$
\implies A=\int _{a}^b 2\pi f(x)\sqrt{ 1+f'(x)^{2} }\, dx  
$$
#Mathematics