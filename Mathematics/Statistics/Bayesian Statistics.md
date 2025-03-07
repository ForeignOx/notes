## Fundamental Principle of Bayesian Statistics
Everything that is uncertain can be treated as random and be associated with its own probability distribution, provided we use a subjecive interpretation of probability
___
We can hence treat the parameter $\theta$ as a random variable. We describe our uncertainty by a (subjective) pdf $f(\theta)$. The [[Likelihood|likelihood]] can be viewed as the conditional probability distribution $f(x|\theta)$ of the data given the parameter.
## Fundamental Procedure of Bayesian Statistics
To “learn about $\theta$ from data $x$” which becomes trivial. We use conditional probability with $f(\theta)$ and $f(x|\theta)$ to find $f(\theta|x)$, which is the conditional pdf of the parameter $\theta$ given the data $x$
___
The problem of being unable to make direct probability statements about $\theta$ in the standard frequntist approach have now been resolved. We can sue $f(\theta|x)$ to answer all questions and test hypotheses directly. This allows us to ask and answer the question we wanted to ask:
    "What values of $\theta$ are most likely given the data under this model?"
In Bayesian methods, large samples aren't necessary for the method to be valid, and we don't need to imagine many hypothetical replications of our experiment
The main criticism of the Bayesian approach si that it asks for more: we need to be specific with the initial (prior) distribution for $\theta$; $f(\theta)$. This is subjective and some don't like this as they prefer maths and science to be objective, but hey this is stats, so say goodbye to that dream...
As the Bayesian approach is more complex, the calculations are also ypically more complex
## $\hspace{0pt}4$ Bayesian Stages
### $\hspace{0pt}1$. Prior
We assign a prior distribution for the parameter $\theta$ (that describes a statistical model) denoted $f(\theta)$
### $\hspace{0pt}2$. Data
We observe data $X=x$, we can now formulate the likelihood $f(x|\theta)$. Same as $\ell(\theta)$, but now viwewed as a full conditional pdf
### $\hspace{0pt}3$. Posterior
After seeing the data $x$, we can evaluate the likelihood and then use [[Bayes' Theorem|Bayes' theorem]] to obtain the posterior distribution for $f(\theta|x)$ which expresses our uncertainty/beliefs about $\theta$, now we have seen the data $x$
### $\hspace{0pt}4$. Inference
Using the posterior distribution $f(\theta|x)$, the problem of inference becomes one of making statements about the posterior distribution, such as probability intervals; $\mathbb{P}(a<\theta<b)=0.95$, credibal intervals, point estimates of the probability of particular hypothesis