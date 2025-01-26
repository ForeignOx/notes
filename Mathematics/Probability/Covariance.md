Suppose we have two [[Random Variables|random variables]]
$$
X:\Omega\to \mathbb{R}
$$
$$
Y:\Omega\to \mathbb{R}
$$
Then the covariance of $X$ and $Y$ is related to [[E(X)|expextation]] and is defined as:
$$
Cov(X,Y):=E((X-E(X))(Y-E(Y)))
$$
If $Cov(X,Y)>0$, then $X$ and $Y$ are positively [[Correlation|correlated]]
If $Cov(X,Y)<0$, then $X$ and $Y$ are negatively correlated
Intuition: suppose $E(X)=E(Y)=0$, then $Cov(X,Y)=E(XY)$
___
## $Cov(X,Y)=E(XY)-E(X)E(Y)$
Proof:
$$
Cov(X,Y)=E((X-E(X))(Y-E(Y)))=E(XY-XE(Y)-YE(X)+E(X)E(Y))
$$
Which by linearity gives:
$$
= E(XY)-E(X)E(Y)-E(X)E(Y)+E(X)E(Y)=E(XY)-E(X)E(Y)
$$

___
By LOTUS, for [[Discrete Random Variables|discrete]]
$$
Cov(X,Y)=\sum_{x}\sum_{y}(x-E(X))(y-E(Y))p(x,y)
$$
for [[Continuous Random Variables|continuous]]:
$$
Cov(X,Y)=\int_{-\infty}^{\infty} \int_{-\infty}^{\infty} (x-E(X))(y-E(Y))f(x,y) \, dx  \, dy 
$$
___
Note that [[Var(X)|variance]] is related in such a way:
$$
Cov(X,X)=E((X-E(X))(X-E(X)))=E((X-E(X))^{2})=Var(X)
$$
___
Covariance is symmetric, that is:
$$
Cov(X,Y)=Cov(Y,X)
$$
Which directly follows from the definition
___
Let $X,Y,Z$ be random variables, $\alpha,\beta,\gamma,\delta \in\mathbb{R}$,
$$
Cov(\alpha+\beta X,\gamma+\delta Y)=\beta\delta Cov(X,Y)
$$
$$
Cov(X+Y,Z)=Cov(X,Z)+Cov(Y,Z)
$$
$$
Cov(X,Y+Z)=Cov(X,Y)+Cov(X,Z)
$$
## Expecation
If $X$ and $Y$ are [[Independence|independent]], then $Cov(X,Y)=0$
### Proof
$$
Cov(X,Y)=E(XY)-E(X)E(Y)
$$
When they are independent, $E(XY)=E(X)E(Y)$, so
$$
Cov(X,Y)=E(X)E(Y)-E(X)E(Y)=0
$$
The converse is not true;
$$
\mathbb{P}((X,Y)=(1,0))=\mathbb{P}((X,Y)=(0,1))=\mathbb{P}((X,Y)=(0,-1))=\mathbb{P}((X,Y)=(-1,0))=\frac{1}{4}
$$
So
$$
\mathbb{P}(XY=0)=1
$$
So $E(XY)=0$, and we can find $E(X)=E(Y)=0$
But
$$
\mathbb{P}(X=1,Y=1)=0\neq \mathbb{P}(X=1)\mathbb{P}(Y=1)
$$
$$
 \mathbb{P}(X=1)=\mathbb{P}(X=1,Y=0)=\frac{1}{4}
$$
Similarly $\mathbb{P}(Y=1)=\frac{1}{4}$
Hence $X$ and $Y$ are nt independent

