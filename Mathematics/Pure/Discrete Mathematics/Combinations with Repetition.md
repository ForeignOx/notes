Given a [[sets|set]] of $n$ objects, how many [[Combinations|combinations]] of size $k$ can be chosen if objects may be selected more than once? In other words, how many $k$-combinations with repetitions form $n$ objects are there?
## How many $k$-combinations with repetitions from $n$ objects are there in which each object is chosen with at least $\hspace{0pt}1$ repetition?
This can be solved first to solve the above question
Note that $k\geq n$ for a non=zero answer
### Example
Count the $5$-combinations with repetition from set $\{ 1,2,3 \}$ in which each element repeats at least once
Solution: since order does not matter, we represent each combination in numerical order
$$
1,1,1,2,3
$$
$$
 1,1,2,2,3
$$
$$
 1,1,2,3,3
$$
$$
 1,2,2,2,3
$$
$$
 1,2,2,3,3
$$
$$
 1,2,3,3,3
$$
Now insert markers where the numbers change:
$$
1,1,1|2|3
$$
$$
 1,1|2,2|3
$$
$$
 1,1|2|3,3
$$
$$
 1|2,2,2|3
$$
$$
 1|2,2|3,3
$$
$$
 1|2|3,3,3
$$
So we inserted $\hspace{0pt}2$ markers in $\hspace{0pt}4$ possible gaps, so the number of combinations is the number of ways to put markers which is $^4C_{6}$
So the number of $k$-combinations from $n$ repetitions and each object occuring at least once is:
$$
\begin{pmatrix}
k-1\\n-1
\end{pmatrix}
$$
