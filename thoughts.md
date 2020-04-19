---
layout: gallery
title: Thoughts (blog space)
mathjax: true
permalink: /thoughts/
---


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


Anyway, the point here is that for ANNs to approximate or surpass the complexity and cognitive flexibility of the brain, they must first address this issue. I think wetware (embedding actual neural tissue in circuitry) is a really smart way of addressing this, and I'll be keeping my eye on [Cortical Labs](https://www.cclabs.ai/), [Koniku](https://koniku.com/technology), and maybe even [this nutjob](https://www.youtube.com/watch?v=h2nNKbO9-Eg) (who did the inverse).


&nbsp;


### *April 10th, 2020*
---
# **Humanity has already found the neural seat of consciousness, science has just overlooked it**

If someone put a gun to my head and made me blurt out the part of the brain that houses consciousness<sup>†</sup>, I'd say "thalamus" without breaking a sweat.

[The thalamus](https://www.ncbi.nlm.nih.gov/books/NBK542184/) is a chunk of gray matter found in the forebrain. This is the Grand Central of the brain—it receives input from a vast number of areas and its projections innervate almost all sections of the cerebral cortex. The result: the thalamus both integrates and distributes information from countless areas. For instance, if sensory input comes in, the thalamus works its magic (transforms that sensory information along some dimension), and then spits it back into the sensory area from whence it came.

I believe quite strongly that anticipation is an evolutionary prerequisite for consciousness and that it demands the coordinated integration of the senses. Why does anticipation require the integration of the senses? Just think about it: let's say a person is swinging a punch at you. Well, first of all, you would need to calculate the trajectory of their swing ([motor cortex](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0191480)) which would require that you visualize their fist reaching your face ([visual cortex](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4595480/)). Significance is assigned to avoiding their fist reaching your face because you know that it will hurt ([nociceptors](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2964977/)). All of this activity coming from disparate regions of your brain before the fist has even come near your face. Without the tight and timely integration of all the information, you can bet your ass that tomorrow you'd wake up with a black eye... 

Why is anticipation a requisite for consciousness? Because anticipation itself requires:
- An internal, updatable model of the world (think: [Bellman Equation](https://en.wikipedia.org/wiki/Bellman_equation))
- A sense of futurity (not just living in the *now*, but in the *next*)
- Pattern identification (I would feel pretty comfortable positing that this is the product of the other two)

I am putting forward that these 3 pillars are the building blocks on which consciousness is built. If we could find regions in the brain that encode or enable these, then I'd say we are well on our way to uncovering the secrets of consciousness.

Back to the thalamus... Just based on sheer connectivity, it seems like the thalamus has always been a prime candidate for understanding neural processes on a fundamental level. Why has it taken so long for focus to shift to the thalamus? The thalamus has historically been viewed as a "low-level" (yuck!) center (yuck yuck!!), as part of a contrived framework of anatomical hierarchy in the brain. Everyone learns in their 101 courses that "the midbrain is the lower brain... and the thalamus and associated areas are part of the limbic system" ([here](https://science.howstuffworks.com/life/inside-the-mind/human-brain/brain5.htm), [here](https://courses.lumenlearning.com/teachereducationx92x1/chapter/lower-level-structures-of-the-brain/), [here](https://www.psychologytoday.com/us/blog/where-addiction-meets-your-brain/201404/your-lizard-brain), and [here](https://www.khanacademy.org/science/health-and-medicine/executive-systems-of-the-brain/emotion-lesson/v/emotions-limbic-system)). The fact that they peddle this crap to unwitting freshmen is infuriating! "Experts" loooove to talk about the limbic system, also called your "Lizard Brain" (yes, experts literally call it that). These experts have grouped the thalamus in this category based on the antiquated idea that neural anatomy recapitulates the evolutionary development of the brain. In plain English: the deepest parts of the brain are the ones most like our evolutionary ancestors. As an unfortunate consequence of this antiquated school of thought, the thalamus has unfairly been identified as a primitive area, with little historical investigation into its role in cognition! Individuals and scientific communities are influenced deeply by egos and the perception of fundamental truths—scientists are unwilling to accept novel discoveries if they fly in the face of what the scientists fundamentally believe to be true (or if they spent most of their life committed to that which is being overturned). This has largely stifled investigation into the thalamus and acceptance of the promising results that come out of it.

[Mike Halassa](http://halassalab.mit.edu/) at MIT is one of the few scientists who gets it. He's still relatively early in his career but I am willing to predict that he will be one of the pioneers of his generation that will unhinge our current understanding of the brain (see also [Doris Tsao](https://en.wikipedia.org/wiki/Doris_Tsao) and more recently, [Steve Ramirez](http://theramirezgroup.org/team/steve-ramirez)). If you're looking for a good read on the thalamus and cognition, Halassa's paper [Schmidtt et al. 2017](https://www.nature.com/articles/nature22073) is seminal. In brief, the paper demonstrates that thalamic neurons engage in task-relevant computations that freely transition from object-based to task-based. This means that the thalamic neurons can encode the identity of specific stimuli *as well as* their significance. Importantly, these thalamic neurons were found to regulate activity in the pre-frontal cortex (PFC), which is largerly seen as the most significant center in cognition. This means that the "low-level" area was not merely relaying basic sensory information from the PFC, but in fact was responsible for conferring its cognitive flexibility!

Mike and I had a great discussion last November about this fundamental oversight in the field and how overwhelming the evidence is for the thalamus' role in cognition. The ingredients for the thalamus coming out as the neural seat of consciousness are all there—it integrates and distributes information from the broadest reaches of the brain, it confers the "high-level brain" the ability to transition between definitions of identity (object --> significance), and has been overlooked in the field for reasons unrelated to its significance in the brain (no one has gotten far trying to find consciousness in the brain, so maybe they should start looking under their noses!). I am super excited to know that this fundamental transition in the field of neuroscience is imminent and will be keeping a close eye on it all from afar.


&nbsp; 
><sup>†</sup>Defining consciousness is not something I will dive into here, despite some implicit definitions. That's an unproductive rabbit hole to be avoided when trying to identify candidate neural substrates for consciousness

>**Bonus:** Google Trends for "[thalamus](https://trends.google.com/trends/explore?date=2007-04-09%202020-04-09&geo=US&q=thalamus)" (I promise this won't be my only data source) shows an incredible periodicity with annual maxima every October going back to 2007. Can you guess why? :)

&nbsp;


### *April 8th, 2020*
---
# **Brown Gold: How our poop is the most untapped gold mine of the 21st Century**

Poop, and by extension, wastewater, is a data source that will be replenished each minute of every hour of every day until the end of civilization. The microbiome is *severely* underappreciated in medicine and health<sup>†</sup>.
I've always been puzzled by this... The evidence supporting the significance of the microbiome is almost insurmountable ([Alzheimer's](https://www.nature.com/articles/s41422-019-0227-7), [longevity](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6051225/), [obesity](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5082693/), [autism](https://www.nature.com/articles/d41586-020-00198-y). The list goes on...), so how the hell could this be almost universally overlooked?

Most recently, [researchers discovered](https://www.nature.com/articles/d41586-020-00973-x) that sewage water serves as a useful proxy for the extent of COVID-19 infections in the community. This made me wonder: why haven't we done this before?


What we have is a fundamental misalignment in the current and actual values of this asset (poop). Call it arbitrage or just plain old opportunity—the reality is clear. Wastewater is (literally) the shit that no one wants (well, [a few people](https://www.usgs.gov/special-topic/water-science-school/science/wastewater-treatment-water-use?qt-science_center_objects=0#)), and so starting to collect mass samples of wastewater wouldn't really perturb the existing system too much.


Despite all this, public interest in the microbiome seems to be stagnant:


<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/blogContent/googleTrends.png" height="250%" width="250%"/>


###### Okay, these might not be the most convincing data, but it's a start... Clearly the public appreciates the importance of health and bacterial diversity, but why don't people attend to the microbiome as an extension of that?


This space is going to make a select few *a lot* of money. The factors for success are all there: a paucity of competition, an almost infinite abundance of data, simple means of data collection, and a demonstrated role in domains relevant to health and disease... These are fertile grounds for discovery and the intrepid pioneers that get in early will no doubt be rewarded.

*Let not thy wastewater be wasted*... You heard it here first.


><sup>†</sup>I can name a couple good companies that recognize this systemic short-sightedness: [Pendulum Therapeutics](https://pendulum.co/) and [Gingko Bioworks](https://www.ginkgobioworks.com/). For the interested reader, I also recommend looking into [Richard Sprague](https://richardsprague.com/microbiome/), who has a pretty extensive passion project on his own microbiome

&nbsp; 
---

##### Thoughts on any of these articles (whether agreeable or otherwise)? Shoot me an [email](malito:sacha@nyu.edu)


&nbsp; 
&nbsp; 

<!-- Begin Mailchimp Signup Form -->
<link href="//cdn-images.mailchimp.com/embedcode/slim-10_7.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{background:#fbfbfb;; clear:left; font:14px Helvetica,Arial,sans-serif; }
	/* Add your own Mailchimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="https://github.us19.list-manage.com/subscribe/post?u=baf7a0905263a7207338e7584&amp;id=be11952091" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<label for="mce-EMAIL">If you want to follow my blog...</label>
	<input type="email" value="" name="EMAIL" class="email" id="mce-EMAIL" placeholder="email address" required>
    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_baf7a0905263a7207338e7584_be11952091" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
</form>
</div>

<!--End mc_embed_signup-->
