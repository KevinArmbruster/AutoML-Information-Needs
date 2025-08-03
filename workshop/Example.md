# Pattern Name
*Give the pattern a short and descriptive name.*

Search Space Scoping.

## Context
*Describe the scenario where this pattern is applicable. When would a developer start thinking about this problem? Describe the ML Task, Model, Data Type & Volume, and Pipeline Stage*

I'm training a Convolutional Neural Network, a ResNet, for a supervised image classification task.
My dataset has about 25,000 images (10GB) and 100 different categories.
A single training run with my baseline settings takes about 45 minutes on the GPU I have access to.
I have a working baseline model, but its performance isn't good enough for my project's needs.
The next step is Hyperparameter Optimization (HPO).

### Problem
*Clearly state your specific problem in this context. What are the risks and inefficiencies that you are trying to avoid?*

The problem is, my model has dozens of hyperparameters.
I know that tuning all of them is impossible with my time and compute budget.
I need to figure out which parameters are actually worth tuning.

### Forces
*Describe the trade-offs or conflicting concerns that need to be balanced.*

* My team usually only uses default hyperparameters and maybe tweaks the learning rate a bit, otherwise they do not do HPO because it costs to much time.
* I am not sure which parameters are the most sensitive to change and therefore the ones I should focus on.
* I only have a certain amount of GPU time allocated for this entire tuning job. I can't run a massive search that would take days.
* I am not sure which and how hyperparameters interact with each other. Tweaking the learning rate might help, but I may have to also change the number of training epochs or batch sizes. Adjusting the regularization strength might also change the optimal learning rate and batch size.

### My Goal
*A description of the goal that you want to reach.*

My goal is to achieve the best performance according to F1 score.
I need to decide which hyperparameters I'm going to tune simultaneously and which ones I'll just fix to a constant value.
This way, I can maximize my chances of finding a great model without wasting compute resources.

## Information Need
*Describe what questions you need to answer to achieve your goal. Additionally, specify if the information you need changes over iterations.*

I use all hyperparameters in a few low-fidelity runs to gauge which hyperparameters are the most important.
I already know from experience that the learning rate and batch size are important so I leave those during initial search on the default value.
Afterwards, I check the results of the runs and look at the plots to see which parameters were changed and how big the impact on the performance was.

## Result
*Describe the outcome and any advantages. Also, describe any new trade-offs or disadvantages this might introduce.*

I create a list of hyperparameters I've decided to actively tune and to leave at the default value.

## Rationale
*Explain why the aquired information helps you to solve the problem. Why is the information a good choice to solve the problem.*

I want to avoid spending a lot of time optimizing parameters that have little to no effect.
If I define fewer parameters I can search them more thouroughly.
Also, I can understand the plots for my top 3-4 variables more easily than if I optimize 10+ at the same time.

## Related Patterns
*List any other connected patterns, goals, and problems, that are prerequisites, alternatives.*

* Selecting search ranges per hyperparameter
* HPO algorithm selection
* Selecting of primary metric

## Known Uses & Limitations
*Please describe, if you know this pattern to be suitable for other contexts as well. Also, if you know it is unsuitable for certain contexts.*

This is something I do in virtually every project. It's a fundamental part of the process in classic or deep learning, and visual and tabular data.
I only skip it if I have less than 8 variabels.
