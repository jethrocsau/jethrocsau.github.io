---
title: RandomForest with PySpark - A ground up implementation
date: 2023-04-30
external_link: https://github.com/jethrocsau/msbd5003-random-forest
tags:
  - Spark
  - Distributed Computing
  - RandomForest
---

## Parallelization of Random Forest using PySpark (Equal Contributor)
- Explored optimization of the Random Forest algorithm using parallel computing in Spark on Microsoft Azure to measure how to improve training time of random forest through the divide and conquer approach.

- Developed three implementation strategies of distributed Random Forest - a top-down approach of parallelizing decision tree building and two bottom-up approaches that parallelize the node-splits algorithm (Depth-First and Breadth-First search)

- Analyzed training times and computational overhead, proposing enhancements for dynamic partitioning and resource allocation.


<!--more-->
