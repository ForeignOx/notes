An arrangemment or list or string is a (finite) sequence of items in which order is important
The length of the arrangement is the number of items in the sequence
## Example
$$
[D,I,S,C,R,E,T,E]
$$
Is an arrangement
Note that items can be repeated
## Standard Problem
How many lists of length $k$ can be made from elements of a set of size $|S|=n$
### Solution
The answer is $n^{k}$ 
![[Arrangements 2024-10-15 15.19.36.excalidraw]]
Because in each of the $k$ places you have $n$ possibilities so you do $n\times n\times\underbrace{\dots}_{k\text{ times}}\times n=n^{k}$ 
## Examples
- How many $\hspace{0pt}4$ letter words can be constructed using the $\hspace{0pt}26$ letters of the alphabet. The answer is $26^4$
- How many $\hspace{0pt}4$ letter words with no letter used more than once? For the first place you can choose any of $\hspace{0pt}26$ options, but the second will have one fewer possibility, so only $\hspace{0pt}25$, then the next will have $\hspace{0pt}2$$\hspace{0pt}4$ and so on. So the answer will be $26\times 25\times 24\times 23=\frac{26!}{22!}$ 
## Standard Problem $\hspace{0pt}2$ (yippeee)
How many lists of length $k$ with no repetition can be made from elements of set $S$ with $|S|=n$
Solution: $n(n-1)(n-2)\dots(n-k+1)=\frac{n!}{(n-k)!}$ for $k\leq n$
We use the [[Multiplication Principle|multiplication principle]] 