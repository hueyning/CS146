## Pre-class work to prepare for class activities:

In this session we model a data set using the normal likelihood with normal-inverse-gamma prior. Reuse your code from the previous class so that you can calculate posterior hyperparameters from the prior hyperparameters and data. Have this code ready for a class activity.


In the previous session you were told which prior hyperparameters to use. This time you have to choose them yourself. Given the information below, find reasonable values for the prior hyperparameters of the normal-inverse-gamma distribution — μ₀, ν₀, α₀, β₀. You will be asked to provide your values for the prior hyperparameters in class, and to explain how you came up with them.


Frame the information below as an optimization problem. You should design a function that is minimized when the constraints below are satisfied.

* The data are normally distributed. The error margins given below represent 1 standard deviation from mean of the parameter.
* Constraint: the mean of the data is approximately 2.3 ± 0.5.
* Constraint: the variance of the data is approximately 2.75 ± 1.

Find μ₀, ν₀, α₀, β₀ hyperparameters for the normal-inverse-gamma prior that match this information.

Paste the values that you arrived at for the hyperparameters of the normal-inverse-gamma prior in a Google Doc and explain how you determined that those values are reasonable given the information you were provided with. Be ready to paste a link to your document into a class poll.

## Solution:
The prior hyperparameter values I arrived at were:
* μ₀ = 2.29
* ν₀ = 1833.34
* α₀ = 356.41
* β₀ = 88.27

I verified the validity of these values by plugging them into a function that generates n samples from the normal-inverse-gamma distribution, where each sample consists of (x,sigma2). 

I generated 10 samples using the above hyperparameters, then plotted these values as normal distributions.

The following graph was achieved:

![norm_dist_samples](/norm_dist_samples.png)

The graph shows an average mean of around 2.3, and variance of around 2.75 (aka standard deviation of ~1.658).
