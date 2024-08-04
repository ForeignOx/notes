Let $d$ be a non-square integer. Then the [[Diophantine Equations|diophantine equation]] of the form $x^{2}-dy^{2}=\pm 1$ is called Pell's equation
## Solutions
All positive integer solutions $x-p$, $y=q$ of Pell;s equation $x^{2}-dy^{2}=\pm 1$ are among pairs $x=p_{k}$, $y=q_{k}$, where $\frac{p_{k}}{q_{k}}$ is a [[Convergents|convergent]] to the [[continued fraction]] expansion of $\sqrt{ d }$ 
This is a one way implication - not all convergents are solutions
### Proof
We will consider the case $x^{2}-dy^{2}=1$, here, if $x=p$, $y=q$ is a solution, then $p^{2}-dq^{2}=1$. Factorising we get $(p-\sqrt{ d }q)(p+\sqrt{ d }q)=1$. The right hand side is greater than 0, so $p+\sqrt{ d }q>0$. Hence $p>q\sqrt{ d }$. Consider
$$
\left| \frac{p}{q}-\sqrt{ d } \right|=\left| \frac{p-\sqrt{ d }q}{q} \right|=\left| \frac{(p-\sqrt{ d }q)(p+\sqrt{ d }q)}{q(p+\sqrt{ d }q)} \right|=\left| \frac{p^{2}-dq^{2}}{q(p+q\sqrt{ d })} \right|=\frac{1}{q(p+q\sqrt{ d })}<\frac{1}{2q(q\sqrt{ d })}<\frac{1}{2q^{2}}
$$
As $p>q\sqrt{ d }\implies p+\sqrt{ d }>2q\sqrt{ d }$
Hence, by this [[Convergents#For $x in mathbb{R} backslash mathbb{Q}$, if $ exists frac{a}{b} in mathbb{Q}$ ($b geq 1$) $ left x- frac{a}{b} right < frac{1}{2b {2}}$, then $ frac{a}{b}$ is one of the convergents of the continued fraction expansion of $x$|lemma]], $\frac{p}{q}$ must be a convergent of $\sqrt{ d }$
### How to tell which convergents work
Let $r$ be the length of the period of the continued fraction expansion of $\sqrt{ d }$. Then $p_{kr-1}^{2}-dq_{kr-1}^{2}=(-1)^{k}$, for $k \in\mathbb{Z}^+$
In particular, if $r$ is even, then $x^{2}-dy^{2}=-1$ has no solutions.
The positive integer solutions to $x^{2}-dy^{2}=1$ are kiven by $x=p_{kr-1}$, $y=q_{kr-1}$ $\forall k \in\mathbb{Z}^+$
Similarly if $r$ is odd, then $x=p_{kr-1}$, $y=q_{kr-1}$ give all integer solutions for:
- $x^{2}-dy^{2}=-1$ for $k$ being odd
- $x^{2}-dy^{2}=1$ for $k$ being even

#Mathematics #Fractions #Definition