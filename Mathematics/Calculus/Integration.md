## Indeinite Integrals (or Anti-[[Differentiation|Derivative]])
A [[Functions|function]] $F(x)$ is called an indefinite integral or antiderivative of a function $f(x)$ in the [[Intervals|interval]] $(a,b)$ if $F(x)$ is differentiable:
$$
F'(x)=f(x)\forall x\in (a,b)
$$
We write:
$$
F(x)=\int f(x) \, dx
$$
Note that if $F(x)$ is an indefinite integral, then so is $F(x)+c$ for any constant $c$, since $\frac{d }{dx}(F(x)+c)=\frac{d }{dx}(F(x))$
It is important to include this arbitrary constant when writing indefinite integrals
If $F_{1}(x)$ and $F_{2}(x)$ are both indefinite integrals of $f(x)$, then $F_{2}(x)-F_{1}(x)=c$, since:
$$
\frac{d }{dx} (F_{2}(x)-F_{1}(x))=\frac{d }{dx} (F_{2}(x))-\frac{d }{dx} (F_{1})(x)=f(x)-f(x)=0
$$
Therefore $F_{2}(x)-F_{1}(x)$ is constant. or is it...? yeh it is
## Integrability
We say $f(x)$ is integrable in $(a,b)$ if it has an indefinite integral on $(a,b)$ which is [[Continuity|continuous]] on $[a,b]$
## Definite Integrals
A definite integral of a function $f(x)$ gives the (signed) area between $f(x)$ and the $x$-axis
![[Integration 2024-11-05 14.26.00.excalidraw]]
In the above diagram, the green would have positive area, and the blue, negative
We define this as the [[Limit|Limit]] of a [[Riemann Sums|Riemann Sum]], by splitting the area into rectangles:
![[Integration 2024-11-05 14.28.16.excalidraw]]
There are lots of ways we could do this, by choosing where we place the $x_{i}$s and where we define the heights of the rectangles. If $f(x)$ is continuous, and the rectangles have small width, we expect this to be a good approximation and the error can be reduced to zero by taking the limit of the width of the rectangles to zero. We say this limit exists if it is independent of how we construct hte rectangles
The definite integral is given in terms of a Riemann sum by taking a limit as the [[Subdivisions|norm]] $|S|$ goes to 0
We say this limit exists if it is independent of subdivision and set of sample points:
Let $f(x)$ be defined $\forall x\in[a,b]$, the definite integral of $f(x)$ from $a$ to $b$ is then:
$$
\int ^{b}_{a} f(x) \, dx =\lim_{ |S| \to 0 } R
$$
It can be shown that this limit does exists if $f$ is continuous on $[a,b]$
We can define:
$$
\int ^{b}_{a} f(x) \, dx -\int ^{a}_{b}  f(x)\, dx 
$$
Which implies:
$$
\int ^{a}_{a} f(x) \, d=0
$$
### Properties
The definite integral satisfies the following properties:
Let $f(x),g(x)$ be integrable functions in $(a,b)$
- Linearity, if $\lambda,\mu \in\mathbb{R}$, then $(\lambda f+\mu g)(x)$ is also integrable in $(a,b)$ with
$$
\int ^{b}_{a} (\lambda f+\mu g)(x) \, dx =\lambda \int ^{b}_{a} f(x) \, dx +\mu \int ^{b}_{a} g(x) \, dx 
$$
- If $c\in[a,b]$, then
$$
\int ^{b}_{a} f(x) \, dx =\int ^{c}_{a} f(x) \, dx +\int ^{b}_{c} f(x) \, dx 
$$
- If $f(x)\geq g(x)\forall x\in(a,b)$, then
$$
\int ^{b}_{a} f(x) \, dx \geq \int ^{b}_{a} g(x) \, dx 
$$
- If $m\leq f(x)\leq M\forall x\in(a,b)$ then
$$
m(b-a)\leq\int ^{b}_{a} f(x) \, dx \leq M(b-a)
$$

#Mathematics #Calculus #Definition