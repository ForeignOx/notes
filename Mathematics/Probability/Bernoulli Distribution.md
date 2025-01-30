A Bernoulli trial is a random experiment with only two possible outcomes:
- Success, with probability $p$
- Failure, with probability $1-p(=q)$
___
The Bernoulli distribution assigns a [[Random Variables|random variable]] to a Bernoulli trial with:
- a value of 1 corresponding to a 'success'
- a value of 0 corresponding to a 'failure'
So:
$$
X\sim \text{Bernoulli}(p) \iff P(X=x)=f(x|p)=\begin{cases}
p^{x}q^{1-x} && x=0,1 \\
0 && \text{otherwise}
\end{cases}
$$
Note that [[Binomial Distribution|$\text{Bernoulli}(p)=B(1,p)$]] 
A Bernoulli variable will be a [[Discrete Random Variables|discrete random variable]]
___
## [[Expectation]]
$$
E(X)=\sum_{x=0}^{1} xP(X=x)=1\times p+0\times(1-p)=p
$$
___
## [[Variance]]
$$
Var(X)=\sum_{x=0}^{1} x^{2}P(X=x)-(E(X))^{2}=1^{2}\times p+0^{2}\times (1-p)-p^{2}=p-p^{2}=p(1-p)=pq
$$
## [[Moment Generating Functions|Moment Generating Function]]
$$
\psi(t)=E(e^{ tX })=\sum_{x=0}^{1}e^{ tx }f(x|p)=e^{ 0\times t }q+e^{ t\times 1 }p=q+pe^{ t }
$$
## [[Binomial Distribution|Binomial Distribution]]
Let $Y_{1},Y_{2},\dots,Y_{n}$ be an [[Independent and Identically Distributed|independent and identically distributed]] Bernoulli random varibale
$$
B_{n}=\sum_{ i=1} ^{ n}  Y_{i}
$$
So obvserve that $E(B_{n})=\sum_{ i=1} ^{ n} E(Y_{i})=np$, since $E(Y_{i})=p$
$$
Var(B_{n})=\sum_{ i=1} ^{ n}  
Var(Y_{i})

$$


#Mathematics #Statistics #Distribution