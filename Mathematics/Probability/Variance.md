$Var(X)$ is the variance of a [[Discrete Random Variables|discrete random variable]] and tells us about the spread of the possible values of $X$, we calculate it like so:
$$
Var(X)=E((X-E(X))^{2})=E(X^2-2XE(X)+E(X)^2)
$$
$$
=E(X^2)-E(2XE(X))+E(E(X)^{2})
$$
$E(X)$ is a constant, so
$$
=E(X^{2})-2E(X)E(X)+E(X)^{2}
$$
$$
Var(X)=E(X^{2})-E(X)^{2}
$$
It is useful to note that variance is the square of the [[Standard Deviation|standard deviation]], $Var(X)=\sigma^{2}$
___
By LOTUS, taking $g(x)=(X-E(x))^{2}$, for discrete,
$$
Var(X)=\sum_{x}(x-E(X))^{2}p(x)
$$
For continuous:
$$
Var(X)=\int_{-\infty}^{\infty} (x-E(X))^{2}f(x) \, dx 
$$

___
To find $Var(f(X))$, where $f(X)$ is a function of X, we do:
$$
Var(f(X))=E(f(X)^{2})-E(f(X))^{2}
$$
Usefully, this means:
$$
Var(aX+b)=E((aX+b)^{2})-E(aX+b)^{2}
$$
$$
=E(a^{2}X^{2}+2abX+b^{2})-(aE(X)+b)^{2}
$$
$$
=a^{2}E(X^{2})+2abE(X)+b^2-a^{2}E(X)^{2}-2abE(X)-b^{2}
$$
$$
=a^{2}E(X^{2})-a^{2}E(X)^{2}=a^{2}Var(X)
$$
$$
\implies Var(aX+b)=a^{2}Var(X)
$$
___
Consider two [[Discrete Random Variables|discrete random variables]] $X$ and $Y$, where
$$
p(x,y)=P(X=x, Y=y)
$$
We can write
$$
Var(X \pm Y)=E(((X\pm Y)-E(X\pm Y))^{2})
$$
$$
=E((X- E(X))\pm (Y-E(Y))^{2})
$$
$$
=E((X-E(X))^{2}+(Y-E(Y))^{2} \pm 2(X-E(X))(Y-E(Y)))
$$
$$
=E((X-E(X))^{2})+E((Y-E(Y))^{2})\pm E(2(X-E(X))(Y-E(Y)))
$$
$$
=Var(X)+Var(Y)\pm 2Cov(X,Y)
$$
So if $X$ and $Y$ are independent, their [[Covariance|covariance]] will be 0, so we can write:
$$
Var(X\pm Y)=Var(X)+Var(Y)
$$
Another way of showing this using properties of covariance is as follows:
$$
Var(X+Y)=Cov(X+Y,X+Y)=Cov(X,X)+Cov(X,Y)+Cov(Y,X)+Cov(Y,Y)
$$
$$
= Var(X)+Var(Y)+2Cov(X,Y)
$$
Using this,
$$
Var\left( \sum_{i=1}^{n}X_{i} \right)=\sum_{ i=1} ^{ n}Var(X_{i})+2\sum_{i<j}Cov(X_{i},X_{j})
$$


#Mathematics #Statistics 