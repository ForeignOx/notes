Let $X\subset \mathbb{R}$, we say that $X$ is bounded above if:
$$
\exists U\in \mathbb{R}:x\leq U\forall x\in X
$$
$U$ is known as an upper bound
Similarly $X$ is bounded below if:
$$
\exists L\in \mathbb{R}:L\leq x\forall x\in X
$$
$L$ is known as a lower bound
If $X$ is bounded above and bounded below, we say $X$ is bounded
## Functions
Let $f(x)$ be a [[Functions|function]] defined on some [[Intervals|interval]] $I$
$f(x)$ is bounded above in $I$ by an upper bound $U$ if:
$$
f(x)\leq U\forall x\in I
$$
$f(x)$ need not take the value $U$ in $I$, if $\exists x_{1}\in I:f(x_{1})=U$, then we say the upper bound $U$ is attained and $U$ is the global maximum value in $I$
$f(x)$ is bounded below in $I$ by a lower bound $L$ if:
$$
f(x)\geq L\forall x\in I
$$
$f(x)$ need not take the value $L$ in $I$, if $\exists x_{2}\in I:f(x_{2})=L$, then we say the lower bound $L$ is attained and $L$ is the global maximum value in $I$
$f(x)$ is bounded in $I$ if it is bounded both above and below, that is if there exists $M$:
$$
|f(x)|\leq M\forall x\in  I
$$
As for other properties, if we don't specify an interval, we take it to be the domain
## Sequences
Let $a_{n}$ be a [[Sequences|sequence]] of real numbers
___
$a_{n}$ is bounded above if:
$$
\exists U:\forall n\in\mathbb{N},a_{n}\leq U
$$
So $U$ is an upper bound for $a_{n}$
___
$a_{n}$ is bounded below if:
$$
\exists L:\forall n\in\mathbb{N},a_{n}\geq L
$$
So $L$ is a lower bound for $a_{n}$
___
$a_{n}$ is bounded if it is both bounded above and bounded below; iff:
$$
\exists M:\forall n\in\mathbb{N},\left| a_{n} \right|\leq M
$$
___
Let $a_{n}$ be a sequence of real numbers which is bounded from above. $M\in\mathbb{R}$ is called the supremum (or least upper bound) if:
1. $M$ is an upper bound of $a_{n}$, and
2. For any $x<M$, $x$ is not an upper bound of $a_{n}$
Note that, if $x$ is not an upper bound of $a_{n}$ then there exists $i:a_{i}>x$
Note that, if $a_{n}$ is bounded from above, then it must have a supremum

#Mathematics #Definition #Analysis 