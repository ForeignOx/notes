A combination from a [[Sets|set]] of objects is an unordered selection of elements of that set. Repeats may be allowed
So $STOAT$ and $TOAST$ are different [[Arrangements|arrangements]], but the same combinations
Formally a combination on set $S$ is identified by factors $m_{i}$, $i\in S$, where $m_{i}=$ number of times element $i$ appears
In our example, $A:1,O:1,S:1,T:2$ 
The size at combination is the total number of selections we call a combination of size $k$ a $k$-combination
How many $k$-combinations without repetitions do we have from a set of size $n$
If we start with $n$ distinct objects, each selection, or combination, of $r$ of these objects, with no reference to order, corresponds to $r!$ [[Permutations|permutations]] of a size $r$ from the $n$ objects. Thus the number of combinations of size $r$ forom a collection of size $n$, denoted $C(n,r)$, where $0\leq r\leq n$ satisfies $(r!)C(n,r)=P(n,r)$, so:
$$
C(n,r)=\, ^nC_{r}=C^r_{n}=\begin{pmatrix}
n\\r
\end{pmatrix}:=\frac{P(n,r)}{r!}=\frac{n!}{r!(n-r)!}=\frac{n(n-1)(n-2)\dots(n-r+1)}{r!}
$$
Note that:

$$
\begin{pmatrix}
n\\r
\end{pmatrix}=\begin{pmatrix}
n\\n-r
\end{pmatrix}=\begin{pmatrix}
n-1\\r-1
\end{pmatrix}+\begin{pmatrix}
n-1\\r
\end{pmatrix}
$$
The second equality is also known as Pascal's formula
Also note that $^nC_{r}$ is also a binomial coefficient, and appears in the [[Binomial Theorem|binomial expansion]] of $(1+x)^{n}$
The fact that ${n \choose r }={n \choose n-r }$ shows a correspondence between the selection of size $r$ from a collection of $n$ and the selection of the $n-r$ objects left behind
## Example
Suppose that Ellen draaws five cards from a standard deck of $\hspace{0pt}52$ cards, in how many ways can her selection result in a  hand with no clubs?
If we examine this more closel, we see that Ellen is restricted to selecting her $\hspace{0pt}5$ cards from the $\hspace{0pt}39$ cards in the deck that are not clubs. Consequently, she can make her selection in ${39 \choose 5 }$ ways
Now suppose we want to count the number of Ellen's 5-card selections that contain at least one club. These are precisely the selections that were not counted in the previous question, and since there are ${52 \choose 5 }$ possible 5-card hands in total, we find that
$$
{52 \choose 5 }-{39 \choose 5 }=2023203
$$
Of all 5-card hands contain at least one club
Can we obtain this result in another wya? For example, since Ellen wants to have at least one club in the 5-card hand, let her first select a club. This she can do in ${13 \choose  1}$ ways, and now she doesn't care what comes up for the other $\hspace{0pt}4$ cards, so after she eliminates the $\hspace{0pt}1$ club, she can then select the other $\hspace{0pt}4$ cards in ${51 \choose 4 }$ ways. Therefore, by [[Rule of Product|rule of product]], we count the number of selections here as:
$$
{13 \choose 1 }{51 \choose 4 }=3248700
$$
Which is different... This answer is larger than the previous one by more than $\hspace{0pt}1000000$ hands, the reason for this is overcounting. Imagine for example, that first Ellen selects $\hspace{0pt}3$ of clubs to start, then $\hspace{0pt}5$ of clubs then king of clubs, then $\hspace{0pt}7$ of hearts then jack of spades, that is not different to if she selected $\hspace{0pt}5$ of clubs to start, then $\hspace{0pt}3$ of clubs, king of clubs, $\hspace{0pt}7$ of hearts, jack of spades. There is also another identical case if she selected king of clubs to start
Another way then to do this properly is to consider exact numbers of clubs, as demonstrated in the table below:

| Number of clubs | Numer of Ways to Select this Number of Clubs | Number of Non-Clubs | Number of Ways to Select this Number of Non-Clubs |
| --------------- | -------------------------------------------- | ------------------- | ------------------------------------------------- |
| 1               | ${13 \choose 1 }$                            | 4                   | ${39 \choose 4 }$                                 |
| 2               | ${13 \choose 2 }$                            | 3                   | ${39 \choose 3 }$                                 |
| 3               | ${13 \choose 3 }$                            | 2                   | ${39 \choose 2 }$                                 |
| 4               | ${13 \choose 4 }$                            | 1                   | ${39 \choose 1 }$                                 |
| 5               | ${13 \choose 5 }$                            | 0                   | ${39 \choose 0 }$                                 |
Since no two of these cases have any 5-card hand in common, the number of hands that Ellen can select with at least one club is:
$$
{13 \choose 1 }{39 \choose 4 }+{13 \choose 2 }{39 \choose 3 }+{13 \choose 3 }{39 \choose 2 }+{13 \choose 4 }{39 \choose 1 }+{13 \choose 5 }{39 \choose  0}=\sum_{i=1}^{5}{13 \choose i }{39 \choose 5-i }=2023203
$$
Yay

#Mathematics #Discrete 