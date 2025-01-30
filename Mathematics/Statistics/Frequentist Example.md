We are polling station, $\hspace{0pt}485$ said Harris, $\hspace{0pt}515$ said Trump, what do I say about the result of the election? Do I trust this? Would I bet on it?
If we pick a person at random from Pennsylvania at random then they will have probability $p$ of saying (truthfully) that they will vote for Trump, where $p$ is the proportion of Trump voters in the state, so $p=\frac{N_\text{Trump}}{N}$, with $N$ being the total voters in the state, but this value of $p$ is unknown (we will assume people are telling the truth here)
If we choose $n$ random people (sample), then it is the same, each has probability $p$, provided the sample is small compared to the total population of voters $N$; $n\ll N$ 
## Probability vs Statistics
A typical probability question would involve telling you the probability $p$ and then having to calculate the probabilities of various configurations of $X_{1},\dots,X_{n}$. However, in statistics we want to go a step further: following a real world experiment, we would be told the results:
$$
X_{1}=x_{1},X_{2}=x_{2},\dots,X_{n}=x_{n}
$$
And then have to infer something meaningful about the unknown probability $p$. This is referred to as inference
## Statistical Inference
Think about what $p$ actually is:
- real fixed with "true" value that is 
    - just unknown (frequentist)
    - an unknown quantity for which we should represent our subjective unceertainty about via a probability distribution (Bayesian/subjective)
