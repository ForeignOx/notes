A system of [[linear]] equations is a nubmer of linear equations in a given number of variables
## Example
$$
a_{11}x_{1}+a_{12}x_{2}+\dots+a_{1n}x_{n}=b_{1}
$$
$$
a_{21}x_{1}+a_{22}x_{2}+\dots+a_{2n}x_{n}=b_{2}
$$
$$
\vdots
$$
$$
a_{n1}x_{1}+a_{n 2}x_{2}+\dots+a_{nn}x_{n}=b_{n}
$$
Is a system of linear equations
If the constants $b_{1},\dots,b_{n}$ are all 0, we call the system homogeneous
## Solution
A solution to a system of linear equations in $n$ variables is $n$-tuple ($\alpha_{1},\dots,\alpha_{n}$) of real numbers such that $x_{1}=\alpha_{1},x_{2}=\alpha_{2},\dots,x_{n}=\alpha_{n}$. The equations all hold simultaneously
To find all solutions of a linear system, we can also use a matrix representation
### Example
$$
x+y+w=1
$$
$$
x-w=0
$$
$$
x+y+z-w=2
$$
$$
x+z+w=3
$$
Is a system o equations which can be written as:
$$
1\times x+1\times y+0\times z+1\times w=1
$$
$$
1\times x+0\times y+0\times z+(-1)\times w=0
$$
$$
1\times x+1\times y+1\times z+(-1)\times w=2
$$
$$
1\times x+0\times y+1\times z+1\times w=3
$$
Which can be written as:
$$
\left(
\begin{array}{cccc|c}
1&1&0&1&1\\
1&0&0&-1&0\\
1&1&1&-1&2\\
1&0&1&1&3
\end{array}
\right)
$$
This is known as an augmented matrix. If the system is homogeneous 



#Mathematics #LinAlg #Definition