Let $f:X\to Y$ be a [[Functions|function]] between [[Sets|sets]] $X,Y$
If $A\subset X$, we define the image of $A$ as:
$$
f(A)=\{ f(a)\in Y|a\in A \}
$$
For $B\subset Y$ we define the pre-image of $B$ as:
$$
f^{-1}(B)=\{ x\in X|f(x)\in B \}
$$
Note this is not the same as the [[Inverses of Functions|inverse function]], it is a notion only in set theory

Let $f:X\to Y$ be a function, and assume that $A,B\subset X$ Then
- $f(A\cap B)\subset f(A)\cap f(B)$
- $f(A\cup B)=f(A)\cup f(B)$
- $f(X\setminus A) \supset f(X)\setminus f(A)$

Assume that $C,D\subset Y$. Then:
- $f^{-1}(C\cup D)=f^{-1}(C)\cap f^{-1}(D)$
- $f^{-1}(C\cup D)=f^{-1}(C)\cup f^{-1}(D)$
- $f(Y\setminus C) \supset f(Y)\setminus f(C)$

## Proof
Look at $f(A\cap B)\subset f(A)\cap f(B)$ 
Take $y\in f(A\cap B)$ then there is $x\in A\cap B$ with $f(x)=y$ Then $x\in A$ and $x\in B$. Then $y=f(x)\in f(A)$ and $y= f(x)\in f(B)$ so $y\in f(A)\cap f(B)$
Look now at $f^{-1}(C\cap D)=f^{-1}(C)\cap f^{-1}(D)$
To prove this, we want to show both $f^{-1}(C\cap D)\subseteq f^{-1}(C)\cap f^{-1}(D)$ and $f^{-1}(C\cap D)\supseteq f^{-1}(C)\cap f^{-1}(D)$
Take $x\in f^{-1}(C\cap D)$. Then $f(x)\in C\cap D$. So $f(x)\in C$ and $f(x)\in D$. So $x\in f^{-1}(C)$ and $x\in f^{-1}(D)$
Hence $x \in f^{-1}(C)\cap f^{-1}(D)$ so $f^{-1}(C\cap D)\subseteq f^{-1}(C)\cap f^{-1}(D)$ is true
Take $x\in f^{-1}(C)\cap f^{-1}(D)$. So $x\in f^{-1}(C)$ and $x\in f^{-1}(D)$ so $f(x)\in C$ and $f(x)\in D$. So $f(x)\in C\cap D$ so $x\in f^{-1}(C\cap D)$, $x$ is in the pre-image by definition, so we have, $f^{-1}(C\cap D)\supseteq f^{-1}(C)\cap f^{-1}(D)$ thus we have equality

#Mathematics #Functions #Definition