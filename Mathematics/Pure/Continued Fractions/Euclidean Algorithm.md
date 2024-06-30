## Lemma
Let $a,b,q\in\mathbb{Z}:a\geq b>0$, we can write 
$$
gcd(a,b)=gcd(a,b-a)
$$
$$
=gcd(a,b-2a)
$$
$$
\vdots
$$
$$
=gcd(a,b-qa)
$$
### Proof
Want to show:
any divisor of $a$ and $b$ is also a divisor of $b-a$

Let $d|a$ and $d|b$, so $a=xd$ and $b=yd$, for some $x,y\in\mathbb{Z}$
Then $b-a=yd-xd=d(y-x)$, as $y,x \in\mathbb{Z},d|(b-a)$

Conversely want to show:
Each divisor of $a$ and $b-a$ is also a divisor of $b$

Let $k|a$ and $k|(b-a)$ so $a=uk$ and $b-a=vk$, for $u,v \in\mathbb{Z}$, then $a_{(b-a)=uk+vk}\implies b=k(u+v)$ as $u+v \in\mathbb{Z},k|b$ This holds for all divisors, so must also hold for gcd
## Euclidean Algorithm
Let $a,b\in\mathbb{Z}:a\geq b>0$, we can write $a=qb+r$, where $0 \leq r<b$ by the [[Divisor Algorithm]]
In fact, we have a series of quotients $q$ and remainder $r_{i}$ such that $0\leq r_{i+1}<r$ ($i\in\mathbb{N}$) and $r_{0}=b$ with:
$$
a=q_{1}b+r_{1}
$$
$$
b=q_{2}r_{1}+r_{2}
$$
$$
r_{1}=q_{2}r_{2}+r_{3}
$$
$$
\vdots
$$
$$
r_{n-1}=q_{n+1}r_{n}+r_{n+1}
$$
Until some remainder, $r_{n+1}$ becomes 0, then $r_{n}=gcd(a,b)$
### Proof
From the Lemma, $g(a,b)=gcd(a-q_{1}b)$
$$
=gcd(b,r_{1})
$$
$$
=gcd(b-q_{2}r_{1},r_{1})
$$
$$
\vdots
$$
$$
=gcd(r_{n+1}r_{n})
$$
$$
=gcd(0,r_{n})
$$
$$
=r_{n}
$$
We are guaranteed that this algorithm well terminate: $b=r_{0}>r_{1}>\dots>r_{n}>r_{n+1}=0$