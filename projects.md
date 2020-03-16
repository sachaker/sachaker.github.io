---
layout: gallery
title: Projects
permalink: /projects/
---

## [Analyzing rideshare data](https://medium.com/@skm440/analyzing-rideshare-data-a7c83f95cd65)
<img style="float: right; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/map.gif" width="65%" />

During the summer of 2019, I explored the possibility of developing an app that would help rideshare drivers receive bigger payouts for their rides. Since drivers are constantly shifting between rideshare services (always trying to maximize their profits based on surge prices, percent payouts, and general pricing models for each service), I thought to build an app that would put this maximization problem into a quantitative framework. Given the time of day, the driver's location, and other factors (like the weather), which service would be most likely to be most profitable? While the idea had potential, my analysis of the data ultimately proved there to be too much variance for the service be reliable.

## [Modified labeling system for DeepLabCut](https://github.com/sachaker/deeplabcut_texteam/blob/master/Protocols/alternateLabelingGUI.md)
<img style="float: right; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/alternateGUI_20nodes.gif" width="65%" />

The DLC labeling process for whiskers can be laborious and repetitive. This alternative to DeepLabCut's point-and-click labeling allows for rapid labeling of contiguous structures, like whiskers. In this new system, the user drags the cursor along each structure, after which the spline is discretized into a pre-set number of nodes with equal increments along the path. This modification increased our throughput from labeling a frame every minute (at least) to labeling a frame every few seconds. I was very pleased when the [original authors](http://www.mousemotorlab.org/deeplabcut) of the software at Harvard asked if they could include my code in their latest, official version.


## [Discovering a new protein in Alzheimer's disease](https://github.com/sachaker/oldWebsite/blob/master/NYU_CNS_Honors_Thesis.pdf)
We discovered a new protein involved in Alzheimer's disease!

## [Modeling information transfer in high-noise neural systems](https://github.com/sachaker/sachaker.github.io/blob/master/files/neuronalTelephone.html)
<img style="float: right; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/rotate.gif" width="30%"/>
This program was the first part of my Final Project for Dr. Alex Reyes' course, Network Models. My goal was to determine how information dissapates throughout a network. To do this, I developed a generative model that creates a population of excitatory neurons that synapse onto each other using a probabilistic mode  based on the proximity between the two units. The position of the neuron was generated using a Gaussian distribution with parameters in arbitrary units for each of the 3 dimensions. Then, the physiological properties of each unit were generated using the Hodgkin-Huxley equations, and stochastically fire for the duration of "recording" based on a model I built from a previous assignment. One of these HH units was then selected at random and given a stimulation of a set pattern. The goal of this project was to see how many units in the network show significant alignment with this stimulus (i.e. received the information), and how that decays with distance and with number of units.
