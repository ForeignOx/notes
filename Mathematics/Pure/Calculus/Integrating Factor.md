Any first order differential equation which is linear (in $y$) can be written in the form:
$$
\frac{dy}{dx}+P(x)y=Q(x)
$$
Let $P=P(x), Q=Q(x)$, we want to find a function $I=I(x)$ (known as the integrating factor):
$$
I\frac{dy}{dx} +PIy=QI
$$
Such that $I\frac{dy}{dx}+PIy$ is a perfect derivative by [[Product Rule]]:
$$
I\frac{dy}{dx} +PIy=\frac{d }{dx} (Iy)
$$
$$
\implies I\frac{d y}{dx} +PIy=I\frac{d y}{dx} +y \frac{d I}{dx} 
$$
$$
\implies PI=\frac{d I}{dx} 
$$
$$
\implies \int P \, dx =\int \frac{1}{I}\frac{d I}{dx}  \, dx =\int \frac{1}{I} \, dI 
$$
$$
\implies \int P \, dx =\ln I
$$
$$
\implies I = e^{ \int P \, dx  }
$$
So the differential equation becomes
$$
\frac{d }{dx} (Iy)=QI
$$
$$
\implies Iy = \int QI \, dx 
$$
$$
\implies y=\frac{1}{I}\int QI \, dx 
$$

#Mathematics #Calculus