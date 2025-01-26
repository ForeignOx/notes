Let $a_{n}$ be a [[Sequences|sequence]] of real numbers and $l\in\mathbb{R}$. $a_{n}$ converges to $l$ if:
$$
\forall\varepsilon>0,\exists N_{\varepsilon}\in\mathbb{N}:\forall n\geq N_{\varepsilon},\left|a_{n}-l\right|<\varepsilon
$$
Another way of writing this is using $l=x$, $N_{\varepsilon}=n_{0}$,
$$
\forall\varepsilon>0\exists n_{0}\in \mathbb{N}:|x_{n}-x|<\varepsilon \forall n\geq n_{0}
$$
A sequence that converges to a limit is called a converent sequence. If a sequence is not convergent, we call it a divergent sequence
We often write:
$$
l=\lim_{ n \to \infty }a_{n} 
$$
Or $a_{n}\to l$ as $n\to \infty$
And using a proof in [[Proofs with Inequalities]], we know:
$$
\left|a_{n}-l\right|<\varepsilon\iff l-\varepsilon<a_{n}<l+\varepsilon
$$
## Examples
### Example 1
$a_{n}=\frac{1}{n}$, clearly $l=0$
![[Convergence 2024-07-02 09.51.22.excalidraw]]
We can take an example of $\varepsilon$ to be $\varepsilon=0.1$, so we are looking for:
$$
\left|a_{n}-0\right|<0.1\iff-0.1<a_{n}<0.1
$$
![[Convergence 2024-07-02 09.54.56.excalidraw]]
For $n\geq 11$, $-0.1<a_{n}<0.1$, so we can take $N_{\varepsilon}=11$, however, this is also true for $n\geq 79$, so if we wanted, $N_{\varepsilon}$ would be acceptible, so:
$$
N_{\varepsilon}\in\{ x \in\mathbb{N}:x\geq 11 \}
$$
#### Proof
Pick an $\varepsilon>0$:
$$
\left| \frac{1}{n}-0\right|=\frac{1}{n}<\varepsilon \forall n\geq n_{0}
$$
Choose $n_{0}\in\mathbb{N}$ such that $n_{0}>\frac{1}{\varepsilon}$ (which is possible by [[Theorem of Archimedes|theorem of Archimides]])
### Example 2
$a_{n}=1$,
If we take $\varepsilon=1$, we can have $N_{\varepsilon}=1$, if we take $\varepsilon=0.5$ we can have $N_{\varepsilon}=1$, if we take $\varepsilon=0.000001$, we can have $N_{\varepsilon}=1$ because it has already converged, so constant sequences clearly converge
#### Proof
A mathematical way of showing this is that:
$$
|a_{n}-l|=|1-1|=0<\varepsilon
$$
Since $\varepsilon$ is defined to be strictly positive
### Example 3
For a convergent sequence such as $a_{n}=n^{2}$, we can never draw lines that bound the sequence, it always escapes:
![[Convergence 2024-07-02 10.11.07.excalidraw]]

### Example 4
$a_{n}=(-1)^{n}$
If we take $\varepsilon=2$, $N_{\varepsilon}=1$, so that works, as $n\geq 1$, $\left|a_{n}-0\right|<2$, but if instead we take $\varepsilon=0.5$, we cannot bound the sequence by the two lines, so it doesn't converge as the definition is only true for all $\varepsilon>0$
### Example 5
Let $a_{n}=\frac{1}{n}$. Prove that $a_{n}$ converges to 0 as $n\to \infty$
$$
n=\frac{1}{\varepsilon}\iff\varepsilon=\frac{1}{n}
$$
So our $N\varepsilon$ will have to be greater $\frac{1}{\varepsilon}$, so we use:
$$
N_\varepsilon=\left\lceil  \frac{1}{\varepsilon}  \right\rceil 
$$
But when $\frac{1}{\varepsilon}$ is an integer, this is still too small, so we instead use:
$$
N_\varepsilon =\left\lceil  \frac{1}{\varepsilon}  \right\rceil +1
$$
#### Proof
Given $a_{n}=\frac{1}{n}$ and $\varepsilon>0$. Let $N_{\varepsilon}=\left\lceil  \frac{1}{\varepsilon}  \right\rceil+1$
If $n\geq N_{\varepsilon}$ then:
$$
n\geq \left\lceil  \frac{1}{\varepsilon}  \right\rceil +1>\left\lceil  \frac{1}{\varepsilon}  \right\rceil \geq \frac{1}{\varepsilon}
$$
So $n>\frac{1}{\varepsilon}$ since $\varepsilon>0$ and $n\geq \frac{1}{\varepsilon}>0$
$$
\left|a_{n}-0\right|=\left|\frac{1}{n}\right|=\frac{1}{n}<\varepsilon
$$
So $a_{n}$ converges to 0
### Example 6
Let $a_{n}=\frac{(-1)^{n}}{2n^{2}}$. Prove that $a_{n}$ converges to 0 as $n\to \infty$
$$
\left| \frac{(-1)^{n}}{2n^{2}}-0\right|=\frac{1}{2n^{2}}<\varepsilon 
$$
$$
\implies \frac{1}{2\varepsilon}<n^{2}
$$
$$
\implies \sqrt{ \frac{1}{2\varepsilon} }<n
$$
$$
\therefore N_{\varepsilon}=\left\lceil  \sqrt{ \frac{1}{2\varepsilon} }  \right\rceil +1
$$
#### Proof
Let $\varepsilon>0$
Let $N_{\varepsilon}=\left\lceil  \sqrt{ \frac{1}{2\varepsilon} }  \right\rceil +1$
 If $n\geq N_{\varepsilon}$ then:
 $$
n\geq \left\lceil  \sqrt{ \frac{1}{2\varepsilon} }  \right\rceil +1>\left\lceil  \sqrt{ \frac{1}{2\varepsilon} }  \right\rceil \geq \sqrt{ \frac{1}{2\varepsilon} }
$$
$$
\implies n>\sqrt{ \frac{1}{2\varepsilon} }
$$
$$
\implies n^{2}>\frac{1}{2\varepsilon}
$$
$$
\implies \varepsilon>\frac{1}{2n^{2}}
$$
as $n>0$
$$
\left|a_{n}-0\right|=\left| \frac{(-1)^{n}}{2n^{2}}-0\right|=\frac{1}{2n^{2}}<\varepsilon
$$
So $a_{n}$ converges to 0
### Example 7
Let $a_{n}=\frac{\sin n}{n}$. Prove that $a_{n}$ converges to 0 as $n \to \infty$
$$
\left| \frac{\sin n}{n}-0\right|<\varepsilon 
$$
$$
\left| \frac{\sin n}{n}\right|=\frac{\left|\sin n\right|}{n}\leq \frac{1}{n}
$$
$$
\therefore N_{\varepsilon}=\left\lceil  \frac{1}{\varepsilon}  \right\rceil +1
$$

#### Proof
Given $a_{n}=\frac{\sin n}{n}$, $\varepsilon>0$. Let $N_{\varepsilon}=\left\lceil  \frac{1}{\varepsilon}  \right\rceil+1$
If $n\geq N_{\varepsilon}$ then
$$
n\geq \left\lceil  \frac{1}{\varepsilon}  \right\rceil +1>\left\lceil  \frac{1}{\varepsilon}  \right\rceil \geq \frac{1}{\varepsilon}
$$
$$
\left|a_{n}-0\right|=\left| \frac{\sin n}{n}-0\right|=\frac{\left|\sin n\right|}{n}\leq \frac{1}{n}<\varepsilon
$$
So $a_{n}$ converges to 0
### Example 8
Let $a_{n}=\frac{n^{2}}{1+n^{2}}$. Prove that $a_{n}$ converges to 1 as $n\to \infty$
$$
\left| \frac{n^{2}}{1+n^{2}}-1\right|=\left| \frac{n^{2}-(1+n^{2})}{1+n^{2}}\right|=\left| \frac{-1}{1+n^{2}}\right|=\frac{1}{1+n^{2}}<\varepsilon 
$$
$$
\implies \frac{1}{\varepsilon}<1+n^{2}
$$
$$
\implies \sqrt{ \frac{1-\varepsilon}{\varepsilon} }<n
$$
If $\varepsilon \leq 1$
#### Proof
Given $a_{n}=\frac{n^{2}}{1+n^{2}}$ and $\varepsilon>0$ 
If $\varepsilon \leq 1$
Let $N_{\varepsilon}=\left\lceil  \sqrt{ \frac{1-\varepsilon}{\varepsilon} }  \right\rceil+1$
If $n\geq N_{\varepsilon}$ then
$$
n\geq \left\lceil  \sqrt{\frac{1-\varepsilon}{\varepsilon}}  \right\rceil +1>\left\lceil  \sqrt{ \frac{1-\varepsilon}{\varepsilon} }  \right\rceil \geq \sqrt{ \frac{1-\varepsilon}{\varepsilon} }
$$
$$
\implies n>\sqrt{ \frac{1-\varepsilon}{\varepsilon} }
$$
$$
\implies n^{2}+1>\frac{1}{\varepsilon}
$$
$$
\implies \varepsilon>\frac{1}{1+n^{2}}
$$
$$
\left|a_{n}-l\right|=\left| \frac{n^{2}}{1+n^{2}}-1\right|=\left| \frac{-1}{1+n^{2}}\right|=\frac{1}{1+n^{2}}<\varepsilon
$$
so $a_{n}$ converges to 1
If $\varepsilon>1$
Let $N_{\varepsilon}=1$
If $n\geq N_{\varepsilon}=1\implies n^{2}+1\geq 2$
$$
\left| \frac{n^{2}}{1+n^{2}}-1 \right|=\frac{1}{1+n^{2}}\leq \frac{1}{2}<\varepsilon
$$
So $a_{n}$ converges to 1
### Example 9???
Let $a_{n}=\frac{4n^{2}-1}{n^{2}+1}$. Prove that $a_{n}$ converges to 4 as $n\to \infty$
$$
\left| \frac{4n^{2}-1}{n^{2}+1}-4 \right|=\left| \frac{4n^{2}-n^{2}-4(n^{2}+1)}{n^{2}+1} \right|=\left| \frac{-5}{n^{2}+1} \right|=\frac{5}{n^{2}+1}
$$
$$
\frac{5}{n^{2}+1}<\frac{5}{n^{2}}<\varepsilon 
$$
$$
\implies n>\sqrt{ \frac{5}{\varepsilon} }
$$
#### Proof
Given $a_{n}=\frac{4n^{2}-1}{n^{2}+1}$ and $\varepsilon>0$
Let $N_{\varepsilon}=\left\lceil  \sqrt{ \frac{5}{\varepsilon} }  \right\rceil+1$
If $n\geq N_{\varepsilon}$ then
$$
n\geq \left\lceil  \sqrt{ \frac{5}{\varepsilon} }  \right\rceil +1>\left\lceil  \sqrt{ \frac{5}{\varepsilon} }  \right\rceil \geq \sqrt{ \frac{5}{\varepsilon} }
$$
$$
\implies n>\sqrt{ \frac{5}{\varepsilon} }
$$
$$
\implies \varepsilon>\frac{5}{n^{2}}
$$
Since $n>0$
$$
\left| a_{n}-l \right|=\left| \frac{4n^{2}-1}{n^{2}+1}-4 \right|=\left| -\frac{5}{n^{2}+1} \right|=\frac{5}{n^{2}+1}<\frac{5}{n^{2}}<\varepsilon
$$
So $a_{n}$ converges to 4
## In the form of $x_{n}=c^{n}$
If $c=0$ or $c=1$, then $x_{n}$ is constant, so we get convergence to $c$
If $c=(-1)$, then $x_{n}=(-1)^{n}$ is divergent
If $c>1$, write $c=1+h,h>0$, now:
$$
x_{n}=(1+h)^{n}\geq 1+hn\geq hn
$$
By the [[Bernoulli Inequality|Bernoulli Inequality]], so the sequence is [[Boundedness|unbounded]], so it is divergent by [[Every Convergent Sequence is Bounded|this theorem]] 
If $c<-1$, consider $x_{2n}=(c^{2})^{n}$ with $c^{2}>1$, so also unbounded and also divergent
If $0<c<1$, write $c=\frac{1}{1+h}$ with $h>0$, so
$$
x_{n}=\frac{1}{(1+h)^{n}}\leq \frac{1}{1+nh}\leq \frac{1}{nh}=y_{n}
$$
Using the Bernoulli Inequality again, and using the $y_{n}$ from the [[Squeeze Theorem|squeeze theorem]], so $x_{n}\to0$
If $-1<c<0$, write $c=-\frac{1}{1+h}$, with $h> 0$,
$$
|x_{n}|=\frac{1}{(1+h)^{n}}
$$
Giving the same as above, so again by the squeeze theorem, $x_{n}$ goes to $\hspace{0pt}0$
## Geometric Series
### Example
Consider $a_{n}=1+\frac{1}{2}+\dots+\frac{1}{2^{n}}$, nos $2-a_{n}=\frac{1}{2^{n}}$, which can be proved by [[Proof by Mathematical Induction!!!!!|induction]]
So
$$
|a_{n}-2|=\frac{1}{2^{n}}
$$
Which is an example of $x_{n}=c^{n}$, so $|a_{n}-2|$ converges to $\hspace{0pt}0$, and hence $a_{n}$ converges to 2
## [[Exponential Functions|Exponentials]] beat Powers
$$
\lim_{ n \to \infty } \frac{n^{k}}{e^{ n }}=0
$$
### Proof
$$
e^{ n }\geq\left( 1+\frac{n}{k+1} \right)^{k+1}\geq \frac{n^{k+1}}{(k+1)^{k+1}}
$$
Where the last term is the final term in the [[Binomial Theorem|binomial expansion]] of the second term
Now
$$
0\leq \frac{n^{k}}{e^{ n}}\leq \frac{n^{k}(k+1)^{k+1}}{n^{k+1}}=\frac{(k+1)^{k+1}}{n}\to0
$$
Which means, by the squeezing theorem, it tends to 0
## Powers beat Logarithms

$$
\lim_{ n \to \infty } \frac{\ln(n)}{\sqrt[k]{n  }}
$$
By substituting $m=\sqrt[k]{n  }$, we get
$$
\lim_{ n \to \infty } \frac{\ln(n)}{\sqrt[k]{n  }}=\lim_{ m \to \infty } \frac{\ln(m^{k})}{m}=\lim_{ m \to \infty } k \frac{\ln m}{m}
$$
Then using a substitution of $l=\ln m$, we get
$$
\lim_{ n \to \infty } \frac{\ln(n)}{\sqrt[k]{n  }}=\lim_{ l \to \infty } k \frac{l}{e^{ l }}=0
$$



#Mathematics #Analysis  #Definition 