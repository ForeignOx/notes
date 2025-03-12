

## Examples
Say we have a [[light|light]] rod and two masses:
![[Rigid Bodies 2025-03-10 14.33.56.excalidraw]]
Then the distance $D$ from the axis to the [[Centre of Mass|centre of mass]] is 
$$
D=\frac{1}{2m}\left( m\cdot \frac{L}{2}+m\cdot L \right)=\frac{3}{4}L
$$
And the [[Moment of Inertia|moment of inertia]] is:
$$
I=m\left( \frac{L}{2} \right)^{2}+mL^{2}=\frac{5}{4}mL^{2}
$$
We can comppute $V(\theta)$ by adding the two pendulum equations:
$$
V(\theta)=mgL(1-\cos\theta)+mg\left( \frac{L}{2} \right)(1-\cos\theta)=\frac{3}{2}mgL(1-\cos\theta)
$$
Note that we can also compute $V$ as:
$$
\text{total mass}\times g\times \text{distance from pivot to CoM}\times(1-\cos\theta)
$$
Which for this example gives:
$$
2m\times g \times \frac{3}{4}L(1-\cos\theta)=\frac{3}{2}mgL(1-\cos\theta)
$$
Note that this way of calculating $V(\theta)$ always works because the calculation of centre-of-mass is the same as that of adding up $V(\theta)$ for each bit of the pendulum
___
Say you have a pendulum consisting of a solid [[Rigid Bodies|rigid]] bar of mass $M$, length $L$, pivoted at one end. Compute $E=K+V$
![[Compound Pendula 2025-03-12 11.17.34.excalidraw]]
First, he distance to the centre of mass is $\frac{1}{2}L$, which we can in fact check, but this immediately gives us
$$
V(\theta)=Mg \frac{L}{2}(1-\cos\theta)
$$
However we can consider a more careful calculation of the centre of mass:
![[Compound Pendula 2025-03-12 11.21.58.excalidraw]]
So centre of mass at
$$
\frac{1}{M}\underbrace{ \int_{0}^{L}  }_{ \text{limit of small sums} }\underbrace{ x }_{ \text{location of bit} }\underbrace{ \left( \frac{Mdx}{L} \right) }_{ \text{mass of small bit} }=\frac{1}{L}\int _{0}^{L}x \, dx =\frac{1}{L}\left[ \frac{x^{2}}{2} \right]_{0}^{L}=\frac{L}{2}-0=\frac{L}{2}
$$
We now need the moment of inertia, so we'll need to do a similar process to find it:
$$
I=\int_{0}^{L} x^{2} \left( M \frac{dx}{L}  \right)=\frac{1}{3}ML^{2}
$$
So
$$
K=\frac{1}{6}ML^{2}\dot{\theta}^{2}
$$
Hence
$$
E=\frac{1}{6}ML^{2}\dot{\theta}^{2}+\frac{1}{2}MgL(1-\cos\theta)
$$

What is the equation of motion for $\theta(t)$? What is the [[Period|period]] $P$ of [[Small Oscillations|small oscillations]] about stable equilibrium? Release the bar from rest horizontally, what is the maximum value of $\dot{\theta}$?
For the first part, we use $\frac{d E}{dt}=0$
$$
\frac{1}{3}ML^{2}\dot{\theta} \ddot{\theta}+\frac{1}{2}MgL\sin(\theta)\dot{\theta}=0
$$
$$
\implies \ddot{\theta}+\frac{3}{2} \frac{g}{L}\sin\theta=0
$$
For the second, if $\theta$ is small, then
$$
\ddot{\theta}+\frac{3}{2} \frac{g}{L}\theta=0
$$
$$
\implies P=2\pi \sqrt{ \frac{2L}{3g} }
$$
For the third, we stat at $\theta=\frac{\pi}{2}$, $\dot{\theta}=0$, we finish with $\theta=0$, and $\dot{\theta}$ is maximised. Conservation of energy gives:
$$
\underbrace{ \frac{1}{2}MgL }_{ \text{initial} }=\underbrace{ \frac{1}{6}ML^{2}\dot{\theta}^{2}_\text{max} }_{ \text{finish} }
$$
Giving 
$$
\dot{\theta}_\text{max}=\dots
$$
    
