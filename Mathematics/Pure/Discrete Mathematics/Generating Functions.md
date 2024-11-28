Generating [[Functions|functions]] provide a powerful eneral method of solving counting problems. They encode combinatorial information in a convenient analytical form
For example that:
$$
(1+x)^{n}=\sum_{ k=1} ^{ n}{n \choose k }x^{k}
$$
THe real analytic function $f(x)=(1+x)^{n}$ encodes the counting information:
$$
{n \choose 0 },{n \choose 1 },\dots,{n \choose n }
$$
As the coefficients in the corresponding power series
This is a powerful link between discrete and continuous mathematics. Generating functions provide a systematic approach to exploiting this link
Let $a_{0},a_{1},a_{2},\dots$ be a [[Sequences|sequence]] of [[Real Numbers|real numbers]]. The ordinary generating function for the sequence is the formal sum:
$$
f(x)=\sum_{ k=1} ^{\infty}  a_{k}x^{k}
$$
The generating function enapsulates the sequence in a form amenable to the standard methods of analysis. We are allowed to manipulate these functions without worrying about the convergence of the power series - this is what we mean by a formal sum
## Example
$\hspace{0pt}7$ chocolate bars are distributed among $\hspace{0pt}4$ people. Alice gets at most $\hspace{0pt}4$, Brian gets at most $\hspace{0pt}3$, Claire gets at most $\hspace{0pt}2$, and Derek gets at most $\hspace{0pt}1$. How many ways of distributing the bars are there?
We are counting solutions $(e_{1},e_{2},e_{3},e_{4})$ to the equation:
$$
e_{1}+e_{2}+e_{3}+e_{4}=7
$$
Where $e_{1},e_{2},e_{3},e_{4}$ are integers satisfying $0\leq e_{1}\leq 4,0\leq e_{2}\leq 3,0\leq e_{3}\leq 2,0\leq e_{4}\leq 1$
We construct an associated generating function. Associate to each variable $e_{i}$ an expression with the sum of $x^{p}$ over $p$ the possible values of $e_{i}$, so $e_{1}$ is associated to the term $x^{0}+x^{1}+x^{2}+x^{3}+x^{4}$ as it can take values from $\hspace{0pt}0$ to $\hspace{0pt}4$
Then create the prouct of the expressions for eqch $e_{i}$:
$$
f(x)=(x^{0}+x^{1}+x^{2}+x^{3}+x^{4})(x^{0}+x^{1}+x^{2}+x^{3})(x^{0}+x^{1}+x^{2})(x^{0}+x^{1})
$$
Then each term in $f(x)$ represents a possible product $x^{e_{1}}\times x^{e_{2}}\times x^{e_{3}}\times x^{e_{4}}$, but we know from the function above, that
$$
x^{e_{1}}\times x^{e_{2}}\times x^{e_{3}}\times x^{e_{4}}=x^{e_{1}+e_{2}+e_{3}+e_{4}}=x^{7}
$$
So every solution corresponds uniquely to a way of multiplying out the expressions in the product $f(x)$ to accumulate $x^{7}$
So the number of solutions is the coefficient of $x^7$ in the series expansion of $f(x)$. The answer is 15
This example shows the basic idea of how a generating function can encode a counting problem. However, to solve the problem, it so far provided limited help; it has mapped the problem of enumerating solutions to that of multiplying out brackets and collecting terms, which is not really a reduction in compxity. The power of the method will come from certain efficiencies of dealing with power series expansions
Note that we can write the generating function $f(x)$ in the above example in more compact form as:
$$
f(x)=\frac{1-x^{5}}{1-x}\times \frac{1-x^{4}}{1-x}\times \frac{1-x^{3}}{1-x}\times \frac{1-x^{2}}{1-x}
$$
$$
= (1-x)^{-4}(1-x^{5})(1-x^{4})(1-x^{3})(1-x^{2})
$$
In principle this is a step towards a more efficient identification of the coefficients
___
How many solutions are there to the equation
$$
e_{1}+e_{2}+\dots+e_{n}=k
$$
Where each $e_{i}\in\{ 0,1 \}$ and $n$ and $k$ are given positive integers
In constructing our generating function, each $e_{i}$ is associated with the expression $(x^{0}+x^{1})=1+x$, so the generating function is the $n$-fold product:
$$
f(x)=(1+x)\times(1+x)\times\dots \times(1+x)=(1+x)^{n}
$$
If we expand the generating function as a power series, we get:
$$
(1+x)^{n}=\sum_{ k=1} ^{ n}{n \choose k }x^{k}
$$
By the binomial theorem
Each term $x^{k}$ corresponds to a choice of $x^{e_{1}}$ from the first bracked, $x^{e_{2}}$ from the second etc. in which the total power of $x$ is $e_{1}+\dots+e_{n}=k$, so the number of solutions is the coefficient of $x^{k}$ in the generating function, which is ${n \choose k }$
___
How many solutions are there to the equation
$$
e_{1}+e_{2}+\dots+e_{n}=k
$$
Where each $e_{i}\in\{ 0,1,2 \}$ and $n$ and $k$ are given positive integers?
Arguing as in the previous example, we wnat the coefficient of $x^{k}$ in the expansion of $(1+x+x^{2})^{n}$. In other words, if $a_{k}$ is the number of solutions required, then
$$
(1+x+x^{2})^{n}=\sum_{ k=1} ^{\infty}  a_{k}x^{k}
$$
Is the generating function of the sequence $a_{k}$
To mak further progress, we need to be able to handle these formal sums in a more compact form
In nice exapmles, the formal power series has a closed form expression in terms of elementary functions for which we know the power series expension explicitly, for insance we can write:
$$
(1+x+x^{2})^{2}=\left( \frac{1-x^{3}}{1-x} \right)^{n}
$$
## Lemma
For $n\geq 0\in\mathbb{Z}$,
$$
\sum_{ k=1} ^{ n}  x^{k}=\frac{1-x^{n+1}}{1-x}
$$
Is the generating function for the sequence $1,1,1,1,\dots,1,1,0,0,\dots$ (the first $n+1$ terms are 1)
### Proof
This is the sum of a geometric sequence, it can be proven by induction, or directly in the form:
$$
(1-x)\sum_{ k=0} ^{ n}  x^{k}=\sum_{ k=0} ^{ n}  (x^{k}-x^{k+1})=1-x^{n+1}
$$
Since the sum telescoples
___
The generating functon for the sequence $(a_{k})_{k\in\mathbb{N}}=1$ is:
$$
\sum_{ k=0} ^{\infty} x^{k}=\frac{1}{1-x} 
$$
The sum to infinity makes analytical sense only for $|x|<1$, in which case, we can take $n\to \infty$ in the part above
___
The generating function for the sequence ${n+k-1 \choose k }$, for $k\geq 0$ is:
$$
\sum_{ k=0} ^{\infty} {n+k-1 \choose k }x^{k}=\frac{1}{(1-x)^{n}}
$$
If you use the [[Binomial Theorem#Extended Theorem|extended binomial theorem]] here, you derive the required result
Alternatively, we can use the method of counting to recognise that this is a case to use [[Ordered Grouping of Indistinguishable Objects|stars and bars]] and the principle of upper negation:
$$
{-n \choose k }=(-1)^{k}{k+n-1 \choose k }
$$
So
$$
(1-x)^{-n}=\sum_{ k=0} ^{\infty}{n+k-1 \choose k }x^{k}
$$
Or even that:
$$
(1-x)^{-n}=((1-x)^{-1})^{n}=(1+x+x^{2}+\dots)^{n}
$$
and the coefficient of $x^{k}$ in the power series expansion here is the number of solutions to $e_{1}+e_{2}+\dots+e_{n}=k$ where $e_{i}\geq 0$ are integers, which we know has solution ${n+k-1 \choose k }$
___
If $f(x)=\sum_{ k=0} ^{\infty} a_{k}x^{k}$ and $g(x)=\sum_{ k=0} ^{\infty} b_{k}x^{k}$ are the generating functions for the sequences $(a_{k})$ and $(b_{k})$ respectively, then
$$
f(x)g(x)=\sum_{ k=0} ^{\infty}  c_{k}x^{k}
$$
Is the generating function of the sequence $(c_{k})$ where
$$
c_{k}=\sum_{l=0}^{k}a_{l}b_{k-l}
$$
This can be shown by simply collecting terms
## Example
Find the coefficient of $x^{17}$ in the expansion of $f(x)=(1+x+x^{2}+\dots+x^{10})^{5}$, we use the geometric sum to rewrite it:
$$
f(x)=\left( \frac{1-x^{11}}{1-x} \right)^{5}=(1-x)^{-5}(1-x^{11})^{5}
$$
Considerign separately the two terms in the product, we have:
$$
(1-x^{11})^{5}=\sum_{i=0}^{5}{5 \choose i }(-x^{11})^{i}=\sum_{i=0}^{5}{5 \choose i }(-1)^{i}x^{11i}
$$
And
$$
(1-x)^{-5}=\sum_{j=0}^{\infty}{4+j \choose 4 }x^{j}
$$
So the terms in the product
$$
\left( \sum_{i=0}^{5}{5 \choose i }(-1)^{i}x^{11i} \right)\left(  \sum_{j=0}^{\infty}{4+j \choose 4 }x^{j} \right)
$$
that contribute $x^{11i+j}=x^{17}$ are $(i,j)=(0,17)$ and $(i,j)=(1,6)$, so the required coefficient is:
$$
{5 \choose 0 }{21 \choose 4 }-{5 \choose 1 }{10 \choose 4 }=4935
$$
## [[Recurrence Relations|Recurrrence Relations]]
Generating functions also find uses in solving recurrence relations
### Examples
Solve for $(a_{n})$ satisfying the recurrence relation $a_{n}=a_{n-1}+2a_{n-2}$, $n\geq 2$ with initial conditions $a_{0}=1,a_{1}=-1$
The idea is that we write the generating function for $(a_{n})$ as $f(x)=\sum_{ n=0} ^{\infty} a_{n}x^{n}$. In this sum, substitute in for $a_{n}$ using the recurrence relation for those values of $n$ for which it is valid, then tidy up the remaining terms using the initial conditions. After some manipulations, obtain an algebraic equation involving $f(x)$ which can be solved to give a closed form formula for $f(x)$
In this case, the recurrence relation allows us to replace $a_{n}$ by $a_{n-1}+2a_{n-2}$ for all $n\geq 2$, so we can write:
$$
f(x)=a_{0}+a_{1}x+\sum_{n=2}^{\infty}a_{n}x^{n}=a_{0}+a_{1}x+\sum_{n=2}^{\infty}(a_{n-1}+2a_{n-2})x^{n}
$$
$$
= 1-x+\sum_{n=2}^{\infty}a_{n-1}x^{n}+2\sum_{n=2}^{\infty}a_{n-2}x^{n}=1-x+x\sum_{n=2}^{\infty}a_{n-1}x^{n-1}+2x^{2}\sum_{n=2}^{\infty}a_{n-2}x^{n-2}
$$
$$
= 1-x+x\sum_{n=1}^{\infty}a_{n}x^{n}+2x^{2}\sum_{n=0}^{\infty}a_{n}x^{n}
$$
We see that the last terms is $\sum_{n=0}^{\infty}a_{n}x^{n}=f(x)$ by definition, the other sum is not quite $f(x)$, as it is missing the $n=0$ term:
$$
\sum_{n=1}^{\infty} a_{n}x^{n}=\sum_{ n=0} ^{\infty}  a_{n}x^{n}-a_{0}=f(x)-1
$$
By the initial condition, so we obtain the following equation for $f(x)$:
$$
f(x)=1-x+x(f(x)-1)+2x^{2}f(x)
$$
$$
\implies f(x)(2x^{2}+x-1)=2x-1
$$
$$
\implies f(x)(2x-1)(x+1)=2x-1
$$
$$
\implies f(x)=\frac{1}{x+1}=\frac{1}{1-(-x)}=1-x+x^{2}-x^{3}+\dots
$$
So our solution is:
$$
a_{n}=\begin{cases}
1&\text{if }n\text{ is even}\\0&\text{if }n\text{ is odd}
\end{cases}
$$
___

