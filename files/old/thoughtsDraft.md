
### *April 19th, 2020*
---
# **The crucial missing link for Artificial Neural Networks**

> ##### I'm going to jump right into this one, so apologies if it lacks the technical introduction such a post might demand. This post is oriented towards a reader who is relatively well read in this topic...


Artificial Neural Networks (ANNs), as the name might suggest, were built with the brain as a primary influence—neurons connect to each other, each conferring information or signals to the other and each with connections that vary mostly in accordance with the alignment between each neuron's activity and the ultimate achievement of the system's goal (see [objective functions](https://en.wikipedia.org/wiki/Mathematical_optimization)). This was a breakthrough in the field of computer science as it completely transformed the capabilities of computers to achieve complex tasks. Computers were no longer just efficient computing devices that did simple tasks quickly—they now could improve iteratively (see [Perceptron](https://en.wikipedia.org/wiki/Perceptron) and the lesser appreciated [MENACE](https://www.mscroggs.co.uk/blog/19)).


Now, things have improved a lot with regards to computing power since those early days but the reality is that the fundamentals of ANNs haven't witnessed the same growth.


What we see is that, despite the fact that we can reach unprecedented [network depth](https://towardsdatascience.com/gating-and-depth-in-neural-networks-b2c66ae74c45), performance just doesn't scale. Take a look at how performance can actually get worse by adding layers (it's clear that a network with connectivity as its only parameter is insufficient to generate the complexity of the brain):


<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/blogContent/errorXiterXlayers.png" height="250%" width="250%"/>


Part of this is due to what is dubbed the [vanishing gradient problem](https://en.wikipedia.org/wiki/Vanishing_gradient_problem), though this was significantly alleviated by the development of [ResNets](https://arxiv.org/abs/1512.03385). ResNets broke numerous world records for classification accuracy and other tasks. However, the error as a function of ResNet layers isn't as impressive after a certain number (the error between 50 and 100 layer ResNets, for the tasks I've used them for, is minimal enough not be worth the extra training time).


I believe that the most significant factor missing from the way we build ANNs that is present in the brain is electric fields. While artifical neurons in ANNs are mathematical representations, biological neurons (just "neurons", from now on) occupy physical space, and thus their interactions are influenced along a spatial dimension, whereas artifical neurons do not (*Note: I definitely do not consider layers in ANNs as spatial*). I also believe that the importance of the electric fields emitted by neurons is severely underappreciated in the field of neuroscience, despite the vast evidence for their significance in the biophysics of the brain as well as cognition ([here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4534030/) and [here](https://www.scientificamerican.com/article/brain-electric-field/), and I'm comfortable arguing that the breakthrough of [LFPs](http://www.scholarpedia.org/article/Local_field_potential) is because they register action potentials and the resulting electric fields).


The electric fields emitted by active neurons contribute to the complexity by being reflexive—an active neuron emits a field which in turn influences the firing dynamics of that neuron and the surrounding neurons, which influence downstream neurons which in turn emit electric fields which in turn... you see where this going. The result is that groups of neurons in the same vicinity will collectively generate large electric fields that will modify their biophysical signature and possibly enable computations that are otherwise unachievable in a state of individual isolation.


Anyway, the point here is that for ANNs to approximate or surpass the complexity and cognitive flexibility of the brain, they must first address this issue. I think wetware (embedding actual neural tissue in circuitry) is a really smart way of addressing this, and I'll be keeping my eye on companies like [Cortical Labs](https://www.cclabs.ai/), [Koniku](https://koniku.com/technology), and maybe even [this nutjob](https://www.youtube.com/watch?v=h2nNKbO9-Eg).


&nbsp;
