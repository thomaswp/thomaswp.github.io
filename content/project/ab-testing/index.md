---
title: "Adaptive Experiments to Improve A/B Testing"
summary: ''
date: 2023-09-28
authors:
  - admin
tags:
  - Evaluation
---

Image Credit: [Cheng Soon Ong](https://researchoutreach.org/articles/adaptive-experiments-machine-learning-help-scientific-discovery/)

As a researcher in Computing Education and AI in Education, I've run dozens of experiments to evaluate the interventions I've built (read some of them [here](https://scholar.google.com/citations?user=v6zJ_8cAAAAJ)).

These experiments are the best way we have to evaluate whether a learning tool or intervention actually helps students, and to make it better.

However, the nature of educational experiments has looked much the same for a long time, and they have a number of drawbacks:
* Experiments require a lot of time and effort to implement well.
* They are difficult to scale, especially at commercial scale.
* Not all students get to use the innovative technology (i.e. the Control group).

### XPRIZE Digital Learning Challenge

The [XPRIZE Digital Learning Challenge](https://www.xprize.org/challenge/digitallearning) was a $1M competition that asked competitors to find way to innovate on learning experiments.

My team, the [Adaptive Experimentation Accelerator](https://www.adexacc.org/) [won 1st place in this challenge](https://www.xprize.org/challenge/digitallearning/articles/xprize-and-the-institute-of-education-sciences-announce-winners-of-1m-digital-learning-challenge), for our work in scaling adaptive experiments for education in real-world courses.

We deployed our MOOClet framework across a variety of classes via the [Open Learning Initiative ](https://oli.cmu.edu/) and helped educators deploy experiments to evaluate interventions such as worked examples, self-explanation prompts, and learner-authored review problems.

### Adaptive Experiments

What made our framework special is its ability to run *adaptive experiments* at scale.

In a **traditional experiment**:
* Students are assigned to a single condition for the whole experiment.
* Students are split evenly across condition, such as an experimental condition (which received an intervention like hints or worked examples) and a control condition that does not
* We wait until the end of the experiment to learn from it, comparing student outcomes in each condition.

In an **adaptive experiment**, we use what we've learned from results earlier in the experiment to influence which conditions we assign students to later on in the experiment. If done right:
* Students are assigned to conditions that maximize both our learning (as researchers) and their learning (as students).
* The more effective a condition is, the more students experience it, maximizing learning.
* We learn throughout the experiment, and adjust based on that information.

So how does that help? With adaptive experiments:
* Students achieve better learning outcomes because they spend more time in more effective conditions.
* Researchers acheive more statistical power in 3+ condition experiments by fading out ineffective conditions.
* We get better data for statistical minority groups (e.g. students with low prior knowledge) by personalizing an experiment's duration based on our certainty.