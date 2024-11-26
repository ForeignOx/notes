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
To mak further progress, we need to be able to handl these formal sums in a more compact form