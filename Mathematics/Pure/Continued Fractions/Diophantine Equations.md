A diophantine equation is a polynomial equation with integer coefficients such that only integer solutions are sought
When we are given a diophantine equation, we typically look to investigate:
1. are there any solutions?
2. if so, are there finitely many or infinitely many?
3. can we find all the solutions?

## Continued Fractions
The [[convergents]] of a [[finite continued fraction]] can be used to generate all solutions to the diophantine equation $ax+by=1$ for $a,b\in\mathbb{Z}$ such that $gcd(a,b)=1$
### Proof:
1. Find one valid solution using what we know about convergents, $p_{k-1}q_{k}-p_{k}q_{k-1}=(-1)^{k}$, so if we set $p_{k}=a$ and $q_{k}=b$ then for $a,b>0$:
    1. {a} for even $k$, $x=-q_{k-1}$ and $y=p_{k-1}$ gives a valid solution
    2. for odd $k$, $x=q_{k-1}$ and $y=p_{k-1}$ gives a valid solution
2. Show that if there is 1 solution, we can find others; let's call our initial solution $(x_{0},y_{0})$, then consider $x-x_{0}+b_{n}$, $y=y_{0}-a_{n}$ for some $n\in\mathbb{Z}$
$$
ax+by=a(x_{0}+b_{n})+b(y_{0}-a_{n})=ax_{0}+ab_{n}+by_{0}-ba_{n}=1
$$

 
#Mathematics #Definition 