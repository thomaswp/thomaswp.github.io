---
title: "ECONet: A Real-world Machine Learning Project"
summary: ''
date: 2023-09-28
authors:
  - admin
tags:
  - Curricula
  - Machine Learning
---

In my introductory Machine Learning (ML) course, for undergraduate and graduate students, students complete a course project, where they have to design an ML pipeline to solve a realistic problem from start to finish. While many datasets provide an adequate challenge, my goal had always been to find a real-world partner to act as a client, allowing students to tackle an authentic problem with potential impact.

### The ECONet Project

In 2022, I partnered with the [NC State Climate Office](https://climate.ncsu.edu/) (NCSCO), the primary scientific extension resource for weather and climate science for the state of North Carolina. The NCSCO had a large amount of weather sensor data from throughout the state, but the sensors occasionally malfunctioned (~3.5% of the time), providing faulty data. The office used a manual verification process to identify errors, which cost many hours of expert labor each year.

I worked with NCSCO to develop a comprehensive course project, focusing on automated anomaly detection in the ECOnet dataset. The project included:
* A prepared training and (held-out) test dataset that had previously be labeled by NCSCO experts, with 8M datapoints!
* Compiled documentation on the dataset and its features.
* A new lesson on error metrics for datasets with heavy class imbalance (e.g. PR-AUC).
* A [CodaLab](https://codalab.lisn.upsaclay.fr/competitions/4076) competation and online leaderboard, where students could compete to achieve the highest performance on the dataset.

{{< figure src="submissions.png" caption="Daily submissions and high scores for the ECOnet challenge." >}}

### Impact

The winning team acheived a PR-AUC of 0.96, with a recall of 0.95 and precision of 0.89 (where "error" was the positive class).

In practice this means that the NCSCO could **skip manual verification of 99.6% of their datapoints** (from ~8M to ~30k!), and still catch 95% of the real errors!

NCSCO was so impressed with the results that the hired two of the competitors to implement the model in the following semester, a project I helped to advise.!

All students left the class with a more complete understanding of the challenges of real-world datasets and constraints in ML, and an impressive project to put on their resumes.