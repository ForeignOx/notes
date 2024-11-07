How do we find the size of a [[Set Operations|union]] of several [[Sets|sets]] $A_{1},\dots ,A_{n}$? If the sets are pairwise disjoint, we may use the [[Rule of Sum|rule of sum]]: if $A_{i}\cap A_{j}=\emptyset$ for all $i\neq j$,
$$
|A_{1}\cup A_{2}\cup\dots \cup A_{n}|=|A_{1}|+|A_{2}|+\dots+|A_{n}|
$$
If the sets are not pairwise disjoint, we can use the formula:
$$
|A_{1}\cup A_{2}|=|A_{1}|+|A_{2}|-|A_{1}\cap A_{2}|
$$
If we have more than two sets, we apply this repeatedly, for example
$$
|A_{1}\cup A_{2}\cup A_{3}|=|A_{1}|+|A_{2}|+|A_{3}|-|A_{1}\cap A_{2}|-|A_{1}\cap A_{3}|-|A_{2}\cap A_{3}|+|A_{1}\cap A_{2}\cap A_{3}|
$$
or another way of thinking about this is:
Consider any element $x\in A_{1}\cup A_{2}\cup A_{3}$, on the LHS it is counded exatly one, we must show it is counted exactly once on the RHS too.
If $x$ is in exactly one of the sets, say $A_{1}$, it is indeed just counted once, in $|A_{1}|$
If $x$ is in exactly two sets, say $A_{1}$ and $A_{2}$, it appears with a positive sign in $|A_{1}|$ and $|A_{2}|$ and with a negative sign in $|A_{2}\cap A_{1}|$, so is also counted once in total
If $x$ is in all three sets, it is counted a total of $1+1+1-1-1-1-1+1=1$ times
___
The more general version is conceptually no more difficult, but requires some more notation
Suppose we have sets $A_{1},A_{2},\dots A_{n}$. A typical $k$-fold intersection $(1\leq k\leq n)$ of a selection of these sets can be written as:
$$
A_{i_{1}}\cap A_{i_{2}}\cap\dots \cap A_{i_{k}}
$$
Where $1\leq i_{1}\leq i_{2}\leq\dots \leq i_{k}\leq n$. Let
$$
S_{k}=\sum_{i_{1}<i_{2}<\dots<i_{k}}|A_{i_{1}}\cap A_{i_{2}}\cap\dots \cap A_{i_{k}}|
$$
be the sum of the sizes of all possible $k$-fold intersections. For example, in the case $n=3$:
$$
S_{1}=|A_{1}|+|A_{2}|+|A_{3}|
$$
$$
 S_{2}=|A_{1}\cap A_{2}|+|A_{1}\cap A_{3}|+|A_{2}\cap A_{3}|
$$
$$
 S_{3}=|A_{1}\cap A_{2}\cap A_{3}|
$$
Then the case with $\hspace{0pt}3$ can be written as $|A_{1}\cup A_{2}\cup A_{3}|=S_{1}-S_{2}+S_{3}$. More generally, we have the following:
For a positive integer $n$ and finite sets $A_{1},A_{2},\dots,A_{n}$,
$$
|A_{1}\cup A_{2}\cup\dots \cup A_{n}|=\sum_{ k=1} ^{ n}  (-1)^{k+1}S_{k}
$$
## Proof
induct :)


#Mathematics #Set 