# Restricted Boltzmann Machines based on archetype selection
We explore an alternative Restricted Boltzmann Machine (RBM) model based on archetype learning, described in ["The emergence of a concept in shallow neural networks"](https://www.sciencedirect.com/science/article/pii/S0893608022000272).
Compaing this alternative model with the standard implementation of the network designed for classification problems.

## Introduction
One of the main challenges of RBMs is that, despite being very versatile and having a broad range of applications, the computational cost of training them can be prohibitive for large datasets or complex models.
In addition, in order to use them as classifiers, one has to use a non-standard implementation such as the Supervised Restricted Boltzmann Machine (SRBM).

In this repository, we explore an alternative setup for the Boltzmann machine that involves training the system based on archetype learning. This means calculating the maximum likelihood parameters by clamping
each training example with its class, thus making it able to be used as both classification and conditional generation. The aim is to be able to reproduce the results stated in [[1]](https://www.sciencedirect.com/science/article/pii/S0893608022000272),
and compare the performance of this proposed model with that of the supervised RBM.

## Repository structure
This repository is based on my final bachelor's degree thesis. On the folder **/documentation** you can find:
 - Thesis report, which provides a brief introduction on RBMs, including a theoretical background on this type of Artificial Neural Networks.
 - Some comparative results obtained by replicating the plots in the aforementioned research paper.

The folder **/codes** has two Jupyter Notebooks, one for each implementation of the Supervised RBMs, that are named after their model (e.g. *SRBM.ipynb*).
It also contains the codes used to generate the figures in **/documentation**, however, these are meant to be used with a cluster since the computations are rather slow.
