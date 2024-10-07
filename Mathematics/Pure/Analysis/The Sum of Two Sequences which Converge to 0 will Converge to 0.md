If $a_{n}$ and $b_{n}$ are [[Sequences]] of real numbers which both [[Convergence|converge]] to 0, then $a_{n}+b_{n}$ converges to 0
## Proof
Given $a_{n}$ and $b_{n}$ both converge to 0, then if $\epsilon>0$ then there also exists $\frac{\epsilon}{2}>0$ such that:
$$
\exists N_{a}:n\geq N_{a}\implies \left| a_{n} \right|<\frac{\epsilon}{2}
$$
$$
\exists N_{b}:n\geq N_{b}\implies \left| b_{n} \right|<\frac{\epsilon}{2}
$$
So if $N=max(N_{a},N_{b})$, then if $n\geq N$ then $\left| a_{n} \right|<\frac{\epsilon}{2}$ and $\left| b_{n} \right|<\frac{\epsilon}{2}$ so
$$
\left| a_{n}+b_{n} \right|\leq \left| a_{n} \right|+\left| b_{n} \right|
$$
From [[The Absolute Value of x+y is Less Than or Equal    to the Sum of the Absolute Values of x and y|this]] theorem
$$
\implies \left| a_{n}+b_{n} \right|<\frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon 
$$
$$
\implies \left| a_{n}+b_{n}-0 \right|<\epsilon
$$
So $a_{n}+b_{n}$ converges to 0


#Mathematics #Limits #Theorem 