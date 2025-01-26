$\mathfrak{F}$ is a collection of [[Subsets|subsets]] of [[Sample Spaces|$\Omega$]] is called a $\sigma$-algebra if it satisfies the following properties:
- $\Omega \in\mathfrak{F}$
- If $A\in\mathfrak{F},A^c\in\mathfrak{F}$
- If a countably infinite collection $A_{1},A_{2},\dots \in\mathfrak{F}$, then $\bigcup_{n=1}^\infty A_{n}\in\mathfrak{F}$ 
$\mathfrak{F}$ is a collection of all [[Events|events]]:
$$
A\subseteq\Omega \forall A\in \mathfrak{F}
$$
In general however, if $\Omega$ is uncountable, it is too much to demand that $\mathbb{P}$ satisfying the axioms of [[Probabilities|probability]] should be defined on all subsets of $\Omega$. The essence of the reason, is that for uncountable sample spaces, such as $\Omega=[0,1]$, there exist subsets of $\Omega$ that cannot be assigned a probability in a way that is consistent with the axioms. The constructionn of such non-measurable sets is also the basis of the famous Banach-Tarski paradox. Uncountable $\Omega$ are unavoidable, and examples occur whenever we have an experiment whose outcome is modelled by a [[Continuous Random Variables|continuous distribution]] 
If $\Omega$ is discrete, we can always take 
$$
\mathfrak{F}=2^{\Omega}
$$
so that every subset of $\Omega$ is an event, it is easy to see that it is the biggest possible $\sigma$-algebra over $\Omega$
For uncountable $\Omega$ however, the set $2^{\Omega}$ may be too unwiieldy, in which case we would consider a smaller $\sigma$-algebra
The trivial $\sigma$-algebra $\{ \emptyset,\Omega \}$ is the smallest possible $\sigma$-algevra over $\Omega$, but it carries no information about the outcome of an experiment

#Mathematics #Probability 