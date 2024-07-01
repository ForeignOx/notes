## For $n \in \mathbb{R}^+$ what can be said about $n^{2}$?
If $0<n<1$ then by multiplying by $n$:
$$
0<n^{2}<n<1
$$
$$
\implies 0<n^{2}<1
$$
If $n>1$ then by multiplying by $n$:
$$
n^{2}>n>1
$$
$$
\implies n^{2}>1
$$

## For $n \in \mathbb{R}^+$, what can be said about $n$?
If $0<n^{2}<1$ then:
$$
n^{2}<1
$$
$$
\implies n^{2}-1<0
$$
$$
\implies (n-1)(n+1)<0
$$
as $n+1>0$:
$$
\implies n-1<0
$$
$$
\implies 0<n<1
$$

If $n^{2}>1$ then:
$$
n^{2}-1>0
$$
$$
\implies (n-1)(n+1)>0
$$
as $n+1>0$:
$$
\implies n-1>0
$$
$$
\implies n>1
$$
## Given $a,n \in\mathbb{R}^+$
$$
n>\sqrt{ a }\iff n^{2}>a
$$
$$
n<\sqrt{ a }\iff n^{2}<a
$$
### Proof:
If $n>\sqrt{ a }$:
$$
n^{2}>n\sqrt{ a }>\sqrt{ a }\sqrt{ a }=a
$$
$$
\implies n^{2}>a
$$
If $n^{2}>a$:
$$
n^{2}-a>0
$$
$$
\implies(n+\sqrt{ a })(n-\sqrt{ a })>0
$$
As $n+\sqrt{ a }>0$:
$$
n-\sqrt{ a }>0
$$
$$
\implies n>\sqrt{ a }
$$
If $n<\sqrt{ a }$, by multiplying by $\sqrt{ a }$, we get:
$$
n\sqrt{ a }<a
$$
As $n^{2}<n\sqrt{ a }$:
$$
n^{2}<a
$$
If $n^{2}<a$:
$$
n^{2}-a<0
$$
$$
\implies (n-\sqrt{ a })(n+\sqrt{ a })<0
$$
Since $n+\sqrt{ a }>0$
$$
n-\sqrt{ a }<0
$$
$$
\implies n<\sqrt{ a }
$$
## Given that $x,a \in\mathbb{R}$ and $b\in\mathbb{R}^+$, prove that $|x-a|<b \iff a-b<x<a+b$
We know that either $x-a\geq 0$ or $x-a<0$
If $x-a\geq 0$
$$
x\geq a
$$
$$
\implies |x-a|=x-a
$$
    If $|x-a|<b$
$$
x-a<b
$$
$$
\implies x<a+b
$$
    Since $a\leq x$, $b>0$
$$
a-b< a\leq x
$$
$$
\implies a-b<x
$$
$$
\therefore a-b<x<a+b
$$
    If $a-b<x<a+b$
$$
x-a<b 
$$
$$
\implies |x-a|<b
$$
    So if $x-a\geq 0$ then:
$$
a-b<x<a+b \iff |x-a|<b
$$
If $x-a<0$
$$
|x-a|=-(x-a)=a-x
$$
$$
x<a
$$
    If $|x-a|<b$
$$
a-x<b
$$
$$
\implies a<b+b
$$
$$
\implies a-b<x
$$
    Since $b>0$
$$
x<a<a+b
$$
$$
\implies a-b<x<a+b
$$
    If $a-b<x<a+b$
$$
a<x+b
$$
$$
\implies a-x<b
$$
$$
\implies |x-a|<b
$$
    So if $x-a<0$ then:
$$
|x-a|<b\iff a-b<x<a+b
$$
So $\forall x,a\in\mathbb{R}$, $b\in\mathbb{R}^+$:
$$
|x-a|<b \iff a-b<x<a+b
$$

## Given that $\epsilon \in\mathbb{R}^+$ and $n\in\mathbb{N}$ prove that $n> \frac{1}{\sqrt{ \epsilon }}\implies \frac{1}{n^{2}}<\epsilon$ 
If $n> \frac{1}{\sqrt{ \epsilon }}$, since $\epsilon>0\implies \sqrt{ \epsilon }>0$
$$
n\sqrt{ \epsilon }>1
$$
$$
\implies \sqrt{ \epsilon }> \frac{1}{n}
$$
$$
\implies \epsilon< \frac{1}{n^{2}}
$$
Due to the proof above
## Given that $\epsilon \in \mathbb{R}^+$ and $n\in\mathbb{N}$, prove that $n> \frac{1}{\epsilon^{2}}\implies \frac{1}{\sqrt{ n }}<\epsilon$
If $n> \frac{1}{\epsilon^{2}}$, $\epsilon^{2}>0$
$$
n\epsilon^{2}>1
$$
$$
\implies \epsilon^{2}> \frac{1}{n}
$$




#Mathematics #Limits 