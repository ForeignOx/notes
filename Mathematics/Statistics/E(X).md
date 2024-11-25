$E(X)$ is the expected value, or mean of a [[Git?/Mathematics/Statistics/Probability/Discrete Random Variables|discrete random variable]] X, and can be calculated like so:
$$
E(X)=\sum_{x\in \mathbb{R}} xP(X=x)
$$
Or for a [[Continuous Random Variables|continuous random variable]],
$$
E(X)=\int_{-\infty}^{\infty} xf(x) \, dx 
$$
___
To find $E(f(X))$, where $f(X)$ is a function of $X$, you can use the formula:
$$
E(f(X))=\sum f(x)P(X=x)
$$
This is useful for calculating [[Var(X)|variance]]
This is also useful to show:
$$
E(aX+b)=\sum (ax+b)P(X=x)
$$
$$
=a\sum xP(X=x)+b\sum P(X=x)
$$
Probabilities sum to one
$$
=a\sum xP(X=x)+b=aE(X)+b
$$
$$
\therefore E(aX+b)=aE(X)+b
$$
___
Consider two [[Git?/Mathematics/Statistics/Probability/Discrete Random Variables|discrete random variables]] $X$ and $Y$, where 
$$
p(x,y)=P(X=x, Y=y)
$$
We can write
$$
E(X+Y)=\sum^{x}\sum^{y}(x+y)p(x,y)
$$
$$
=\sum^{x}\sum^{y}(xp(x,y)+yp(x,y))
$$
$$
=\sum^{x}x\sum^{y}p(x,y)+\sum^{y}y\sum^{x}p(x,y)
$$
$$
=E(X)+E(Y)
$$
Similarly, $E(X-Y)=E(X)-E(Y)$, hence:
$$
E(X\pm Y)=E(X)\pm E(Y)
$$
___

#Mathematics #Statistics 
