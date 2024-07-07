The binomial distribution is the sum of $n$ [[Independence|independent]] [[Bernoulli Distribution|Bernoulli distributions]] with probability of success $p$
So if:
$$
X_{n}\sim \text{Bernoulli}(p)
$$
$$
Y\sim B(n,p) \iff Y=\sum_{ r=1} ^{ n}  X_{r}
$$
___
## PMF
The probability mass function is as follows:
$$
P(X=r)=\begin{pmatrix}
n\\x
\end{pmatrix}p^{r}q^{n-r}
$$
For $r \in \{ 0,1,\dots,n \}$
This is because $p^rq^{n-r}$ is the probability of obtaining the sequence of $n$ Bernoulli trials in which the first $r$ trials are successes and the remaining $n-r$ trials result in failure. Since the trials are independent with probabilities remaining constant between them, any sequence of $n$ trials with $x$ successes has the same probability of being achieved. There are $^nC_{r}=\frac{n!}{r!(n-r)!}$ such sequences. The binomial distribution is concerned with the probability of obtaining any of these sequences, meaning the probability of one of them must be added $^nC_{r}$ times
___
## [[E(X)]]
Since a binomial distribution is the sum of $n$ independent bernoulli distributions:
$$
E(Y)=\sum_{ r=1} ^{ n}  E(X_{r})=\sum_{ r=1} ^{ n}p=np
$$
___
## [[Var(X)]]
Since a binomial distribution is the sum of $n$ independent bernoulli distributions:
$$
Var(Y)=\sum_{ r=1} ^{ n}  Var(X_{r})=\sum_{ r=1} ^{ n}  pq=npq
$$
___
## Requirements
The binomial distribution is a suitable modelling distribution if the following hold:
- Each trial has only two possible outcomes, success, or failure
- The number of trials, $n$, is fixed
- The probability of success, $p$, is also fixed throughout all the trials
- Trials are [[Independence|independent]] of one another

#Mathematics #Statistics #Distribution 