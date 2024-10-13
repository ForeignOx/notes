If we have some curve $y=f(x)$, if we what to find the length of this curve in some interval $[a,b]$, and $f(x)$  is differentiable on this interval, and $f'(x)$ is continuous in the interval, an approximation to the length will be approximately equal to the length of lines on the curve like so:
![[Pasted image 20240131173422.png]]
With $n$ points $P_{0}=a,P_{1},P_{2},\dots,P_{n}=b$ where the length between two points we write as $len(P_{i-1},P_{i})$ 
So:
$$
l_{approx} =\sum_{i=1}^nlen(P_{i-1},P_{i})
$$
$$
\implies l \approx \sum_{i=1}^\infty len(P_{i-1},P_{i}) 
$$
As having more sub-intervals makes the approximation better
![[Pasted image 20240131174606.png]]
We can work out the length function with pythagoras:
$$
len(P_{i-1},P_{i})=\sqrt{ (x_{i}-x_{i-1})^{2}+(y_{i}-y_{i-1})^{2} }
$$
$$
=\sqrt{ \Delta x^{2}+\Delta y_{i}^{2} }
$$
We can use the mean value theorem:
$$
\frac{f(x_{i})-f(x_{i-1})}{x_{i}-x_{i-1}}=f'(x_{i}^*)=\frac{\Delta y_{i}}{\Delta x}
$$
where $x_{i}^*$ is the value of $x$ that satisfies the theorem
$$
\implies \Delta y_{i}=f'(x_{i}^*)\Delta x
$$
$$
\implies len(P_{i},P_{i-1})=\sqrt{ (\Delta x^{2})+(f'(x_{i}^*)\Delta x)^{2} }
$$
$$
=\sqrt{ 1+f'(x_{i}^*)^{2} }\Delta x
$$
Since as $n\to \infty$, $x_{i-1}=x_{i}^*=x_{i}$ 
We can therefore say
$$
L=\lim_{ n \to \infty } \sum_{i=1}^n \sqrt{ 1+f'(x_{i}^*)^2 }\Delta x
$$
$$
\implies L=\int _{a}^b \sqrt{ 1+f'(x)^2 }\, dx 
$$

#Mathematics 