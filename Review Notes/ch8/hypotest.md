### Chapter 8 Hypothesis Testing
#### Motivation
In previous chapters, we discussed about the statistics of a population. This chapter provides an application of those stats theory we mentioned before. In real life, people wants to draw some useful conclusion with the data drawn from a certain population. If we put it by statistical language, these claims are in the form of hypothesis and it's the statistician's job to test  whether it's true. Usually, statistics function as a medium tool to achieve this goal. Therefore, this chapter consists of two parts:
- Methods for finding tests 
- Methods for evaluating estimators

The first part provides methods to construct test procedures using different ideas. It's made up of three parts: LRT; Bayesian; and Union-Intersection(or Intersection-Union) Tests. Different method applies to different scenarios.
#### Methods for finding tests
##### Likelihood Ratio Test
Definition: The likelihood ratio test  for testing $H_0:\theta\in \Theta_0$ versus $H_1:\theta\in \Theta_0^c$ is 
$$
\lambda(x)=\frac{\sup_{\Theta_0}L(\theta|x)}{sup_{\Theta}L(\theta|x)}
$$
A LRT is any test that has a rejection region of the form $\{x:\lambda(x)\leq c\}$ where $c$ is any number satisfying $0\leq c\leq 1$.
- Remarks:The intuition behind LRT is that The denominator denotes the largest likelihood of the observed $x$ is drawn from a distribution where the parameter lies in $\Theta_0$. The nominator denotes which of the whole param space. Therefore, the LR lies between 0 and 1.The number small implies that $H_0$ is a hypothesis is one that is not likely to be true, while large implies the contrary.
Example 8.2.3 is an interesting application of the method.

 (Relationship with ss)
 Theorem: If $T(x)$ is a ss for $\theta$ and $\lambda^*(t)$ and $\lambda(x)$ are the LRT stats based on $T$ and $X$ respectively. Then $\lambda^*(T(X))=\lambda(X)$ for all $X$ in the sample space.
 - This theorem is another extension of ss theory. It's not a surprising result since a stats is ss means it contains all the useful information about a param already thus this is just a verification of this property in the test theory.
##### Bayesian Tests
The Bayesian method regards the param as an r.v and has a distribution for itself. Before the observation about $X$ is obtained, it has a prior distribution and with $X$ we update the prior and get a posterio distribution $\Pi(\theta|x)$ about the param. With $\Pi$, we can compute $P(\theta\in \Theta_0|x),P(\theta\in \Theta^c|x)$. If $P(\theta\in \Theta_0|x)\geq P(\theta\in \Theta^c|x)$, we accept $H_0$ otherwise the reverse.
##### Union-Intersection(or Intersection-Union) Tests
This test method applies to the case where $H_0$ is the intersection (or union) of a set of expression. If 
$$
H_0:\theta\in \displaystyle\cap_{\gamma\in\Gamma}\Theta_{\gamma}(\text{or }H_0:\theta\in \displaystyle\cup_{\gamma\in\Gamma}\Theta_{\gamma})
$$
Suppose the rejection region for the test $H_{0\gamma}$ is $\{x:T_{\gamma}(x)\in R_{\gamma}\}$. Then the rejection region for the U-I is 
$$
\cup_{\gamma\in\Gamma}\{x:T_{\gamma}(x)\in R_{\gamma}\}(\text{or }\cap_{\gamma\in\Gamma}\{x:T_{\gamma}(x)\in R_{\gamma}\})
$$