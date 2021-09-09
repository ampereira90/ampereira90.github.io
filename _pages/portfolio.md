---
layout: archive
title: "Tools Developed for the Scientific Community"
permalink: /portfolio/
author_profile: true
---

{% include base_path %}

## HEP-Frame

HEP-Frame is a framework to aid the development and efficient execution of pipelined data analysis applications in homogeneous and heterogeneous servers. This tool resulted from the work developed during my PhD, and is currently actively used in particle physics research. <br />
 <br />
Access HEP-Frame [here](https://bitbucket.org/ampereira/hep-frame/wiki/Home).

## PRNG-Broker

PRNG-Broker is a middle layer between the application code, e.g., a Monte Carlo simulation, and specialised pseudo-random number generation (PRNG) libraries. It efficiently manages parallel PRN requests to external PRNG libraries, adequately using the computational resources available in multicore, manycore, and GPU devices. This efficient management of PRN generation focus on improving the performance of parallel compute-bound applications, but also provides a significantbenefit for both sequential and memory-bound codes. <br />
 <br />
Technical report available [here](/files/PRNG_Broker.pdf). <br />
Access PRNG-Broker [here](https://github.com/prng-broker/prng-broker/wiki/PRNG-Broker).

## TEG Analyser and Debugger

An adequate Task Execution Graph for the representation of the possible execution flows within complex pipelines of conditional tasks must respect a strict set of properties:
- Must represent tasks and paths connecting tasks (vertices and edges), where the edgeshave a direction associated with them (directed graph);
- Must have one start vertex (task) and always reach one end vertex (task);
- Must represent the weight of a task;
- Must represent dependencies between tasks;
- Each task may be executed at most once (acyclic);
- May have an hierarchical representation with subgraphs;
- Subgraphs may be strongly connected and complete graph;
- Must support multiple paths between the starting and the ending vertices.

The creation of such TEGs must be automatically validated. Inaccuracies in its structure often lead to erroneous scheduling behaviour, whose source cannot be easily traced. While these mechanisms should be integrated into the schedulers to avoid critical failures, they are extremely useful during the R&D of novel scheduling strategies. Such tool is especially important if TEGs are developed for software workflows composed by large numbers of conditional or non-conditional tasks with complex inter-dependencies. <br />
<br />
![image](/files/teg.png)
<p align="center">
 <i>The workflow of creating and analysising a TEG.</i>
</p>

This tool is currently under development after a successful proof-of-concept, with an alpha version expected in the near future. <br />
<br />
![image](/files/visualizer.png)
<p align="center">
 <i>Sample test case from the proof-of-concept development.</i>
</p>
