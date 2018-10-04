## Task
Describe this new model, with unknown &alpha; and &beta;, using generative modeling language.

In the first model we have a universe where each player gets given an expected field goal rate from the uniform distribution. 

The expected field goal rate is always the same in all their games. In any particular game, the number of successful field goals are given by a binomial distribution.

How would you describe the new model?

Write your answer in a Google doc, share it, and be ready to paste a link to your shared doc in poll in class.

<hr>

Given posterior and conjugate priors consisting of binomial distributions, and a likelihood function consisting of a beta distribution, unknown parameters &alpha; and &beta; of the likelihood beta distribution will have to be estimated based on our expectation of the shape of the beta distribution, given appropriate levels of uncertainty.

The expected field goal rate should include some uncertainty, and we can model this with unknown &alpha; and &beta; parameters.

Now we have to decide on the distributions that our unknown &alpha; and &beta; parameters should be sampled from.

Since the parameters for the Beta distribution are constrained by &alpha; > 0 and &beta; > 0, the support for the chosen distribution should be all real positive numbers.

I've decided to choose a Gamma(&alpha;=7, &beta;=2) distribution in order to sample for both &alpha; and &beta;, which gives us &mu; = E(x) = 3.5. 

![Image of Gamma dist](https://github.com/hueyning/CS146-repo/blob/master/cs146-4.2-pre-class-work/Gamma-distribution.png | width=100)

Thus, the expected field goal rate will be modeled by Beta(&alpha;=3.5, &beta;=3.5), which gives us &mu; = E(x) = 0.5. The shape of the graph resembles a normal distribution, with σ^2=Var(X)=0.0313.

![Image of Beta dist](https://github.com/hueyning/CS146-repo/blob/master/cs146-4.2-pre-class-work/Beta-distribution.png | width=100)
