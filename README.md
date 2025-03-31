# Simulating-Repeated-Helping-Games

The code of my master's thesis: 

Evaluating the performance of behavioral strategy estimation methods in repeated helping games: A Monte Carlo approach.

Master's thesis can be found on: **[link to be included]**

**Mentor**: Assoc. Prof. Aljaž Ule, PhD

**Co-Mentor**: Assist. Žiga Velkavrh, PhD

**Keywords**: game theory, repeated games, helping games, simulations, Monte Carlo methods, strategy estimation methods

## Abstract:

In behavioral game theory, human behavior is often studied with controlled laboratory experiments. 
One of the drawbacks of such experiments is that they are often expensive to run, leading researchers to limit the number of participants in order to avoid exceeding their budget, which consequently results in lower statistical power of the study. 

As an alternative to laboratory experiments, in this thesis we use simulations, that are for certain research questions more suitable than laboratory experiments. 
Using simulations, based on empirical distributions of (sub)strategies, we evaluate the effectiveness of methods for estimating behavioral strategies in repeated helping games. 
Simulations allow for controlled testing of the performance of estimation methods under a variety of conditions, including controlling for noise and distribution of (sub)strategies present in the simulation. 

The estimation methods are based on those used in experimental helping game studies. 
Two of the methods (SFIT and TREND) are based on logistic regression, one (MLFIT) is based on finite mixture models, relying on maximum likelihood estimates, and one (DFIT) is based on the number of successful matches of actual decisions with decisions simulated from deterministic (sub)strategies. 

The simulations allowed us to estimate the true accuracy of each of the four methods, revealing their potential shortcomings. The resultsshowed that the MLFIT method was quite accurate (accuracy: 82%-88% at different noise levels), and in particular was more accurate than the other three methods for
both substrategy distributions studied, regardless of the magnitude of the noise.

## Contents: 

**main** - Contains the main code for the master's thesis:
- Defining substrategy distributions,
- Defining substrategies,
- Defining simulations,
- Defining all estimation methods (DFIT, SFIT, TREND, MLFIT),
- Running simulations,
- Classifying players using estimation methods,
- Saving simulation and classification results.

**analysis** - Contains all statistical analysis done for the thesis: 
- Loads simulation and classification results,
- Plots confusion matrices for strategies,
- Calculates stats for substrategies,
- Calculates accuracy used for hypothesis testing (QQ plots, Shapiro-Wilk, ANOVA, Friedman, Wilxocon paired signed rank, paired t tests).

**Currently the code is implemented in R markdown for easier comprehension. R is used since there are already packages in R that simplify implementing MLFIT.**

## To be included:

Simple and needed implementations:
- Testing epsilon = 0 (curiosity),
- Tidying up the main code and analysis,
- Implementing a single R file that runs simulations,
- Making a new R file that contains only estimation methods and is suited for experimental analysis,

Other implementations (mostly elaborated in the Further Discussion of my master's thesis):
- Implementing a new estimation method,
- Using evolutionary game theory for simulations (running different distributions and having developing populations based on which strategy/substrategy is most profitable and/or cognitively simple).
