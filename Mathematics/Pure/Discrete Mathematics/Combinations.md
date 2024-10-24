A combination from a [[Sets|set]] of objects is an unordered selection of elements of that set. Repeats may be allowed
So $STOAT$ and $TOAST$ are different [[Arrangements|arrangements]], but the same combinations
Formally a combination on set $S$ is identified by factors $m_{i}$, $i\in S$, where $m_{i}=$ number of times element $i$ appears
In our example, $A:1,O:1,S:1,T:2$ 
The size at combination is the total number of selections we call a combination of size $k$ a $k$-combination
How many $k$-combinations without repetitions do we have from a set of size $n$
Solution: this is the same as [[Unordered Choice of Distinct Objects without Replacement]], as we can first consider the number of arrangements and then sort the number of these into groups, each group having $k!$, so the number of combinations is $\frac{P(n,k)}{k!}=\frac{n!}{k!(n-k)!}$
## Example
From the letters $P,Q,R,S$, find the number of combinations of $\hspace{0pt}2$ distinct letters, then $\hspace{0pt}3$ distinct letters
Solution: for the first case there are $\hspace{0pt}6$ combinations, for the second there are $\hspace{0pt}4$, 

#Mathematics #Discrete 