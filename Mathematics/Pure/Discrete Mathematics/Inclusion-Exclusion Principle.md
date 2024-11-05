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
If $x$ is in exactly two sets, say $A_{1}$ and $A_{2}$, it appears with a positive sign in $|A_{1}|$ and $|A_{2}|$ and ``
