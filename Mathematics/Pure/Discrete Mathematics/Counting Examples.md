Using the standard alphabet from A-Z
1. How many $\hspace{0pt}4$-letter words use the letter E at least once?
2. How many $\hspace{0pt}4$-letter words use E exactly once?
3. How many $\hspace{0pt}4$-letter words contain no three identical letters in consecutive positions?
4. How many $\hspace{0pt}4$-letter words use E and T at least once?
5. How many $\hspace{0pt}3$-letter words have letters in strict alphabetical order?
## Solutions
### Number $\hspace{0pt}1$ 
The number of all $\hspace{0pt}4$-letter words is $26^{4}$ from what we know about [[Ordered Choice of Distinct Objects with Replacement|ordered choice of distinct objects with replacement]], consider those not using E, there are $25^4$, thus the number of using E is $26^4-25^4$ 
A more formal way of explaining this is that the set $A=\{ 4\text{-letter words using E} \}$, $B=\{ 4\text{-letter words not using E} \}$, $A\cup B$ is the set of all $\hspace{0pt}4$-letter words, $A\cap B=\emptyset$, thus $|A\cup B|=|A|+|B|$ from the [[Rule of Sum|rule of sum]], so $|B|=|A\cup B|-|A|$, which is how we reach the solution
### Number $\hspace{0pt}2$ 
Using the [[Rule of Product|rule of product]]. First choose where E goes, there are $\hspace{0pt}4$ possibilities for this to occur and then there are $25^3$ possibilites to fil the other $\hspace{0pt}3$ places, so the answer is $4\times 25^3$
Again a more formal way of thinking about this is to consider the unions between the sets where E takes the $i$th spot
### Number $\hspace{0pt}3$ 
There are $\hspace{0pt}3$ ways that give the opposite of what we want: 
$$
A\neq B\,\begin{cases}
A,A,A,A\\B,A,A,A\\A,A,A,B
\end{cases}
$$
For the first case, there are $\hspace{0pt}26$ such words, one for each letter, for the second and third cases, there are $26\times 25$ such words, one to pick the first letter, the other to pick the second
So the answer is $26+26\times 25+26\times 25=26\times 51$ 
So the number of ways we can have $\hspace{0pt}4$ letter words with no three identical letters in consecutive positions is $26^4-26\times 51$
### Number $\hspace{0pt}4$ 
First number of words with neither E nor T is $24^4$
Let $E=\{ \text{words with at least one E} \}$, $T=\{ \text{words with at least one T} \}$, we know the cardinality of each is $26^4-25^4$ from problem 1
Now we know $|E\cup T|=26^4-24^4$, but we want $|E\cap T|$. We know $|E\cup T|=|E|+|T|-|E\cap T|$ from here follows: $|E\cap T|=|E|+|T|-|E\cup T|=(26^4-25^4)+(26^4-25^4)-(26^4-24^4)=26^4-2\times 25^4+24^4$ 
### Number $\hspace{0pt}5$ 
Number of words with $\hspace{0pt}3$ distinct letters is $26\times 25\times 24=P(26,3)$ which we know from [[Git?/Mathematics/Pure/Discrete Mathematics/Permutations|permutations]] If we pick a general word with $\hspace{0pt}3$ distinct letters, there will be $\hspace{0pt}6$ ways to order it, but only one of them will be in alphabetical order (example the word CAT,ACT,TAC,ATC,CTA,TCA, only ACT is in order) so the answer to the problem is $\frac{26\times 25\times 24}{6}=26\times 25\times 4$ 