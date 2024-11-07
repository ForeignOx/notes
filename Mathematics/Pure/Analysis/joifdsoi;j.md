Let $(x_{n})_{n\in\mathbb{N}}$ be a sequence such that $x_{n}\in[a,b]$ for all $n$. If the sequence converges to $x\in\mathbb{R}$, then $x\in[a,b]$
## Proof
Assume $x<a$, choose $\epsilon=\frac{a-x}{2}>0$
By convergence, there exists $N_{\epsilon}\in\mathbb{N}$ with:
$$
|x_{n}-x|<\epsilon \forall n\geq N_{\epsilon}
$$
In particular:
$$
x-x_{n}>-\epsilon
$$
Now
$$
a-x_{n}=a-x+x-x_{n}=2\epsilon+x-x_{n}>\epsilon>0
$$
So $a>x_{n}$ which is a contradiction

