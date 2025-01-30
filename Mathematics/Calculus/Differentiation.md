## Functions of $\hspace{0pt}1$ Variable
![[Differentiation From First Principles 2024-03-14 22.58.05.excalidraw]]
Geometrically the derivative of a [[Functions|function]] $f'(a)$ (or $\frac{df}{dx}(a)$ or $\frac{df}{dx}|_{x=a}$) is equal to the slope of the unique non-vertical tangent to the graph of $f$ at $x=a$ if it exists
This is naturally defined as the [[Limit|limit]] of the slope of a line segment joining two nearby points on the graph of $f$, i.e. at a point $(a,f(a))$, the nearby point will be $(a+h,f(a+h))$, so we use the gradient of a line equation to find the tangent like so:
$$
\frac{f(a+h)-f(a)}{a+h-a}=\frac{f(a+h)-f(a)}{h}
$$
By taking $h$ to be as small as possible, i.e. the limit as $h$ tends to 0, we will get the tangent, hence:
$$
f'(x)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}
$$
### Differentiability
A function $f(x)$ $f:D\to \mathbb{R}$, $D\subseteq \mathbb{R}$ is differentiable at $x=x_{0}$ iff:
In words: (all points close to $x_{0}$ are in $D$) when I zoom into the function near $x=x_{0}$ it looks like a (non-vertical) straight line
Proper: 
- $\exists\delta>0:\left| x-x_{0} \right| <\delta\implies x\in D$
- The function can be written as
$$
f(x)=f(x_{0})+M(x-x_{0})+R(x)
$$
Which is the tangent line with some error term $R(x)$, where $M$ is some constant and
$$
\lim_{ x \to x_{0} } \frac{R(x)}{\left| x-x_{0} \right| }=0 
$$
So the error term must shrink faster than the tangent line
- If the limit exists, we say $f$ is differentiable at $x=a$
- If $f'(a)$ exists for all $a\in \text{Dom}f$, we say that $f$ is differentiable and the function $f'(x)$ is called the derivative
- The equation of the tangent to $f$ at a point $(a,f(a))$ is given in terms of the derivative as $y=f(a)+f'(a)(x-a)$ 
- A necessary condition for $f'(a)$ to exists and hence for the function to be differentiable at the point $x=a$, is for $f$ to be [[Continuity|continuous]] at $a$, but this is a necessary but not sufficient condition
- There are $\hspace{0pt}2$ ways that a function can fail to be differentiable at a point where it is continuous:
    - The tangent line is vertical at the point
    - There is no unique tangent line at the point
#### Differentiability is a Stronger Property than Continuity
Let $X\subset \mathbb{R}$ and $f:X\to \mathbb{R}$. If $f$ is differentiable at $c\in X$, then $f$ is also continuous at $c$
##### Proof
Assume $f$ is differentiable at $x=c$
$$
f(x)-f(c)=(x-c) \frac{f(x)-f(c)}{x-c}\to0\cdot f'(c)=0
$$
As $x\to c$, so $\lim_{ x \to c }f(x)=f(c)$, in other words, $f$ is continuous at $c$
# 
___
##### Remarks
The converse is false! Take for example $f(x)=\left| x \right|$, this is not differentiable at $x=0$, but is continuous
You can even have functions that are continuous everywhere and differentiable nowhere. Historically there was the longstanding belief that every continuous function should be differentiable everywhere except for a set of isolated points. This misconception was proven incorrect by Karl Weierstrass who provided a counterexample: 
$$
f(x)=\sum_{k=0}^{\infty} \frac{1}{2^{k}}\cos(15^{k}\pi x)
$$
Which you can show by [[Series#Comparison Test|comparison test]] converges for all $x$, but is differentiable nowhere 
### Multiple Derivatives
If $f(x)$ is differentiable, then $f'(x)$ may also be differentiable, and we say $f$ is twice differentiable which we write as: $f''(x)$, the second derivative
More generally, $f^{(n)}(x)$ is the $n$th derivative. Other common notation includes $\frac{d^nf}{dx^{n}}$ or $Df,D^{n}f$ or if we have a function of time as the variable eg. position, $r(t)$, then one usually writes velocity as $\dot{r}(t)$, then acceleration $\ddot{r}(t)$
### Examples
Calculate the derivative of $f(x)=\frac{1}{x^{2}}$ in $(0,\infty)$. Let $c\in(0,\infty)$, then
$$
\lim_{ x \to c }  \frac{f(x)-f(c)}{x-c}=\lim_{ x \to c } \frac{\frac{1}{x^{2}}-\frac{1}{c^{2}}}{x-c}
$$
$$
= \lim_{ x \to c } \frac{c^{2}-x^{2}}{x^{2}c^{2}(x-c)}=\lim_{ x \to c } \frac{(c-x)(c+x)}{(x-c)x^{2}c^{2}}=\lim_{ x \to c } -\frac{c+x}{x^{2}c^{2}}
$$
$$
= -\frac{2c}{c^{4}}=-\frac{2}{c^{3}}
$$
___
With $f(x)=x^{2}$, calculate $f'(a)$ using the limit definition:
$$
f'(a)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}=\lim_{ h \to 0 } \frac{(a+h)^{2}-a^{2}}{h}=\lim_{ h \to 0 } \frac{2ah+h^{2}}{h}=\lim_{ h \to 0 } 2a+h=2a
$$
___
Let $f(x)$ be a polynomial. Then $f(x)-f(c)$ is also a polynomial which has a $\hspace{0pt}0$ at $x=c$. Thus by polynomial division, we can write
$$
f(x)-f(c)=(x-c)f_{1}(x)
$$
For some polynomial $f_{1}(x)$. In particular, $f_{1}(x)$ is continuous. We therefore have shown that all polynomials are differentiable
___
Calculate the deribative of $f(x)=\sin x$
$$
f'(x)=\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}=\lim_{ h \to 0 } \frac{\sin(x+h)-\sin x}{h}=\lim_{ h \to 0 } \frac{\sin x\cos h+\cos x\sin h-\sin x}{h}
$$
$$
= \lim_{ h \to 0 } \left( \sin x\left( \frac{\cos h-1}{h} \right)+\cos x\left( \frac{\sin h}{h} \right) \right)=\cos x
$$
___
$f(x)=x^{1/3}$ is not differentiable at $x=0$ as the tangent is vertical:
![[Pasted image 20241024141454.png]]
___
$f(x)=|x|$ is not differentiable at $x=0$ as its gradient has a left sided limit and a right sided limit, but they were not equal
___
Using the fact about the [[Exponential Functions|exponential function]] that
$$
x\leq e^{ x }-1\leq \frac{x}{x-1}
$$
So
$$
1\leq \frac{e^{ x }-1}{x}\leq \frac{1}{1-x}
$$
So by squeezing, we get the limit
$$
\lim_{ x \to 0 } \frac{e^{ x }-1}{x}=\lim_{ x \to 0 }  \frac{e^{ x }-e^{ 0 }}{x-0}=1=e^{ 0 }
$$
So due to the addition law, we know it everywhere else since we know it at one point:
$$
(e^{ x })'(0)=e^{ 0 }=1
$$
So general $c$:
$$
\frac{e^{ x }-e^{ c }}{x-c}=e^{ c }\left( \frac{e^{ x-c }-1}{x-c} \right)
$$
So as $x\to c$, this goes to
$$
e^{ c }\times 1=e^{ c }
$$
So
$$
(e^{ x })'=e^{ x }
$$

## Differentiability for Functions of $\hspace{0pt}2$ Variables $f(x,y)$
In words: A function $f(x,y)$ is differentiable at $(x_{0},y_{0})=\vec{x}_{0}$ if when I zoom in, it looks like its [[Tangent Plane|tangent plane]] 
![[Differentiation 2025-01-21 14.18.57.excalidraw]]
We can rewrite $f(x,y)$ as
$$
z=f(x_{0},y_{0})+M(x-x_{0})+N(y-y_{0})
$$
Proper definition: The function $f(x,y):D\to \mathbb{R},D\subseteq \mathbb{R}^{2}$ is differentiable at $\vec{x}_{0}=(x_{0},y_{0})$ iff
- $\exists\delta>0:$ if $\left| \vec{x}-\vec{x}_{0} \right|<\delta$ then $\vec{x}\in D$
- $f(x,y)=f(x_{0},y_{0})+M(x-x_{0})+N(y-y_{0})+R(x,y)$
Which means that when $M$ and $N$ are constants and
$$
\lim_{ \vec{x} \to \vec{x}_{0} } \frac{R(x,y)}{\left| \vec{x}-\vec{x}_{0} \right| }
$$
### Example
Show that $f(x,y)=x^{2}+y^{2}$ is differentiable at $\vec{x}_{0}=(x_{0},y_{0})=(1,1)$
$$
f(x,y)=((x-1)+1)^{2}+((y-1)+1)^{2}
$$
$$
= (x-1)^{2}+2(x-1)+1+(y-1)^{2}+2(y-1)+2
$$
$$
= \underbrace{ 2 }_{ =f(1,1) }+\underbrace{ 2(x-1) }_{ =M(x-x_{0}) }+\underbrace{ 2(y-1) }_{ =N(y-y_{0}) }+\underbrace{ (x-1)^{2}+(y-1)^{2} }_{ =R(x,y) }
$$
$$
R(x,y)=(x-1)^{2}+(y-1)^{2}=\left| (x,y)-(1,1) \right| ^{2}=\left| \vec{x}-\vec{x}_{0} \right| ^{2}
$$
Then
$$
\lim_{ \vec{x} \to \vec{x}_{0} } \frac{R(x,y)}{\left| \vec{x}-\vec{x}_{0} \right| }=\lim_{ \vec{x} \to \vec{x}_{0} }  \frac{\left| \vec{x}-\vec{x}_{0} \right| ^{2}}{\left| \vec{x}-\vec{x}_{0} \right| }=\lim_{ \vec{x} \to \vec{x}_{0} } \left| \vec{x}-\vec{x}_{0} \right| =0
$$



#Mathematics #Calculus