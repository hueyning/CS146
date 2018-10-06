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
* μ₀ = 2.30000008    
* ν₀ = 11.00143402
* α₀ = 9.56252627
* β₀ = 23.5470067

I verified the solution by calculating the 68% confidence interval for a normal-inverge-gamma distribution with the above prior hyperparameter values (10000 samples were drawn).


68% confidence interval for mean: (1.8125130790485078, 2.7710685971047777)
68% confidence interval for variance: (1.875758984857007, 3.6186149782970967)