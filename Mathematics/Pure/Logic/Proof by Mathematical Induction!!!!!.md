Here we need a [[Proposition|proposition]] $A(n)$ for every $n\in\mathbb{N}$, if we want to show that $A(n)$ is a true statement for every $n$, we need to start by showing $A(1)$ is true, then we need to show for every $n\in\mathbb{N}$, $A(n)\implies A(n+1)$ 
## Examples
$1^{3}+2^{3}+3^{3}+\dots+n^{3}=\frac{n^{2}(n+1)^{2}}{4}$, which we can call $A(n)$
Check $A(1)$, $LHS=1$, $RHS=\frac{1^{2}2^{2}}{4}=1=LHS$ yayyy
Assume $A(k)$ is true, for some $k\in\mathbb{N}$:
$$
1+2^{3}+3^{3}+\dots+k^{3}+(k+1)^{3}=\frac{k^{2}(k+1)^{2}}{4}+(k+1)^{3}
$$
$$
= (k+1)^{2}\left( \frac{k^{2}}{4}+k+1 \right)=\frac{(k+1)^{2}}{4}(k^{2}+4k+4)=\frac{(k+1)^{2}(k+2)^{2}}{4}
$$
So $A(k+1)$ is true
Thus by induction it holds for all $n\in\mathbb{N}$
___
Let $a_{1},\dots,a_{n}$ be positive real numbers with $a_{1}\cdot a_{2}\cdot\dots a_{n}=1$, then $a_{1}+a_{2}+\dots+a_{n}\geq n$ with equality if and only if all $a_{i}=1$. This will be $A(n)$
Consider $A(1)$, we must have $\hspace{0pt}1$ real number and it must be equal to $1$, so $1\geq 1$ and there is equality since all terms are 1
Assume $A(k)$ is true, consider $A(k+1)$, take positive real numbers $a_{1},\dots,a_{k+1}$ with $a_{1}+\dots+a_{k+1}\geq n+1$ with equality if all $a_{i}=1$
The equality is easy to show, if all $a_{i}=1$, their sum is $n+1$
Now assume they are not all $1$, so some $a_{i}\neq 1$, we can assume $a_{i}<1$, now there must be some real number $a_{j}>1$ to make their product equal to $\hspace{0pt}1$, we can say without loss of generality $i=1$, $j=2$, so $a_{1}<1,a_{2}>1$, consider $(a_{1}-1)(a_{2}-1)$ which will be negative as $a_{1}-1$ is negative and $a_{2}-1$ is positive. 
$$
(a_{1}-1)(a_{2}-1)=a_{1}a_{2}-a_{2}-a_{1}+1<0
$$
$$
 \iff a_{1}a_{2}<a_{1}+a_{2}-1
$$
Now consider $k$ positive numbers $a_{1}a_{2},a_{3},\dots,a_{k+1}$ which also have a product of $\hspace{0pt}1$, now by induction assumbtion we have that:
$$
k\leq a_{1}a_{2}+a_{3}+\dots+a_{k+1}<a_{1}+a_{2}+a_{3}+\dots+a_{k+1}-1
$$
$$
 \implies a_{1}+a_{2}+..+a_{k+1}>n+1
$$
Proved QED yaya