# Human-in-the-Loop AutoML: Information Needs and Usage Patterns


## Motivation

Automated machine learning (AutoML) tools have come a long way — from simple search strategies to sophisticated optimization methods like Bayesian optimization and evolutionary algorithms. Originally, they aimed to automate the full development of machine learning models by finding the best configurations automatically.

However, full automation is often not what practitioners need. In reality, experts often don't just want a final model handed over by a black-box system. Instead, experts often prefer gaining insights, control, and flexibility in guiding the process, adjusting decisions on the fly, and understanding how certain results are produced.

Working with AutoML tools often means balancing performance, costs, and time. This also applies to iterative human-in-the-loop development with AutoML tools, which is characterized by running experiments, analyzing results, tweaking hyperparameters, and refining strategies. In such contexts, AutoML tools can assist exploration, sense-making, or hypothesis testing — not just optimization.

But many AutoML tools aren’t designed with human-in-the-loop in mind. One-shot optimization is often assumed the ultimate goal, which is one reason why AutoML tools offer little transparency about what’s happening under the hood. This discrepancy between how tools are designed and how you actually work with them leads to selecting suboptimal search spaces, difficulties interpreting intermediate results, wasting computational resources, and developing less robust models.

That’s why we’re here. This workshop is about understanding the information needs in AutoML in human-in-the-loop workflows. Together, we’ll explore how AutoML can better support iterative model development.

## Goal

The goal of this workshop is simple but important:  
We want to better understand how practitioners like you actually use AutoML tools — not as a means of full automation, but as a tool for exploration, learning, and decision-making in your workflow.

We aim to uncover:
- **What information you need** when working with AutoML tools
- **Why you need it** — what decisions it helps you make
- **When you need it** — at which stages in your workflow across the [ML Pipeline](ML%20Pipeline%20Overview.md)
- **How you go about finding it** — whether from the tool, experimentation, or other means

By gathering this knowledge, we want to shed light on real-world AutoML usage patterns.  
Our long-term goal is to help design AutoML tools that:
- **Support human-in-the-loop workflows** instead of assuming full automation
- **Make relevant information accessible when you need it**
- **Adapt to the iterative nature of model development**

This workshop is not about testing hypotheses or validating existing tools.  
It’s about capturing your experiences, challenges, and strategies — and using them to inform better tool design that fits your actual work, not the idealized workflows often assumed by tool developers.

Your participation will help us define information needs in a structured, reusable way — so they can directly inspire the next generation of AutoML tools that are transparent, flexible, and centered on expert users like you.


## Targeted Results

We aim to create a collection of information needs and, building on these information needs, information need patterns of AutoML tools in human-in-the-loop. A possible structure of the information need patterns is demonstrated in this [template](Template.md) and this [example](Example.md). The pattern is just a predefined format to make analyzing, refining and applying these information needs easier in the future.

Information need patterns should describe the context, when specific information needs are relevant, which information is needed, how you acquire the needed information and your goal why you need certain information.


## Getting Started

### Editor

You can open any GitHub repository in your browser in the following ways:

* To open the repository in the same browser tab, press . while browsing any repository or pull request on GitHub.
* To open the repository in a new browser tab, press >.
* When viewing a file, select the edit dropdown menu and click github.dev.

### Creating Patterns

Please copy and start working on your first pattern using this [template](workshop/Template.md)! Please use [template](workshop/Template.md) and an [example](workshop/Example.md) to articulate your information needs.

It can help to think of a specific past project of yours. Try to remember the stages from start to finish along the [ML Pipeline](ML%20Pipeline%20Overview.md). Which goals did you persue in each stage or in general? Did you iterate over certain stages? Which decisions did you take? Which information was necessary to take a further step?

There are no wrong answers! We are very interested in your personal experiences, what you have learned so far, when you apply this knowledge and how it has payed off for you.
If you are unsure where to write down certain information feel free to write it to the seemingly most appropriate point — do not skip it if it feels important.


## Commit your Patterns

Don't forget to commit your patterns every so often, and especially before you sign off!
