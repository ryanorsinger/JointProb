Notes for Chapter 1

Heart of Bayesian thinking: updating your beliefs after considering new evidence.

We can rarely be certain, but we can develop increasing levels of confidence. Instead of making statistics about certainty, Bayesian view is about measuring believability in an event.

Frequentists assume that probability is about long-run frequency of events (measuring stable/static frequencies) and this is challenging if there have been zero of something, for example, like zero nuclear accidents (before there were any).

If Bayesian and Frequentist inference were functions, they would return different things, representing different ideas with data types. Frequentist answers return a single number, representing an estimate, like a sample average. Bayesian inference returns a probability distribution (which ain't a single number)

As N, the number of instances of evidence approaches infinity, our Baeysian results (often) align with frequentist results. For large N, statistical inference is more or less objective. But for small N, inference is much more unstable. Frequentist estimates have more variance and larger confidence intervals. This is where Bayesian inference shines. 

"The posterior probabilities are represented by the curves, and our uncertainty is proportional to the width of the curve."

## Discrete Random Variables?
For discrete variables? Probability Mass Function

If a random variable  𝑍
  has a Poisson mass distribution, we denote this by writing

`𝑍∼Poi(𝜆)`
 
One useful property of the Poisson distribution is that its expected value is equal to its parameter, i.e.:

`𝐸[𝑍|𝜆]=𝜆`
 

## Continuous Random Variables
Use the Probability Density Function

When a random variable has an exponential distribution with parameter  `𝜆`, we say  𝑍 is exponential and write

`𝑍∼Exp(𝜆)`
 
Given a specific  𝜆
 , the expected value of an exponential random variable is equal to the inverse of  𝜆
 , that is:

`𝐸[𝑍|𝜆]=1𝜆`


Poisson is great for counts data, especially counts per period.


## What is probabilistic programming?
Simply: probability model components are first class citizens. 



## Installation and Environment Setup for Bayesian Modeling and Computation (as well as Bayesian Methods for Hackers)
- Installed Anaconda
- Cloned the https://github.com/BayesianModelingandComputationInPython/BookCode_Edition1 repo.
- Clone the https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers repo
- Copied BayesianModelingandComputationInPython/BookCode_Edition1/blob/main/environment.yml over to the Probabilistic-Programming-and-Bayesian-Methods-for-Hackers repo
- Attempt 1:
    - `conda env create -f environment.yml`
        - received a CondaEnvException
            ```
                Pip subprocess error:
                ERROR: Could not find a version that satisfies the requirement jaxlib>=0.1.65 (from numpyro) (from versions: none)
                ERROR: No matching distribution found for jaxlib>=0.1.65

                failed

                CondaEnvException: Pip failed
            ```
        
        - ran `pip install --upgrade "jax[cpu]"`, globally

        - `conda env remove -n bmcp` to remove the incomplete bmcp environment.

        - `conda env create -f environment.yml`
    - I tried to be good. I tried to do it right and propper in a conda environment, but this produced more challenges.
- Attempt 2Ran `conda install -c conda-forge pymc3` globally.


