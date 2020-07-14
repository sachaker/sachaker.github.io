---
layout: gallery
title: Projects
permalink: /projects/
---

## [Fig Finance](http://fig.finance)
<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/fig.png" width="25%"/>

Fig is a side project I started with my best friend to address the growing discrepancy between financial literacy and the accessibility of investing. We wanted to create a "Bloomberg terminal for Robinhood users". Ironically, while Robinhood has done a lot to democratize investing, they've done almost nothing to increase financial literacy, resulting in amateur investors losing a lot of hard-earned money. We're building a dashboard that offers investment data in a simple, clean interface.

The other arm of Fig is the automated trading platform, which scrapes the positions that Wall St.'s top analysts are taking and makes trades based on those positions in real-time. We have consistently beat out the S&P 500 and our peak annual returns were at ~105%.

Check out an interactive protoype for our dashboard [here](https://www.figma.com/proto/AdGaBc5V70Mn9VYEFJF9On/Fig-Finance?node-id=115%3A2&scaling=min-zoom) and a sneak peek at a very (very!) alpha version of the actual dashboard [here](https://drive.google.com/file/d/16PrnHMCN_JaHgFPBGHLLkxsAyTY3ydXb/view). Fig is still nascent and we've yet to iron out a solid vision for what it will look like.


&nbsp;


## [Speech-to-speech voice conversion](https://audioapp.co/)
<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/ellen.gif" width="30%" />

"aud.io" is an automated system for speech-to-speech voice conversion. Want to speak as Spongebob? Donald Trump? Ellen Degeneres and more? Look no further. 

You simply speak into the microphone and out comes the same audio, only your voice is now that of your selected speaker. It can learn new output with a day of training and is robust to pretty much any input you throw at it. Its technology is bordering on the frontier of what is out there and is certainly the only readily implementable platform for social purposes. Part of the tournament for the online accelerator [Pioneer](https://pioneer.app).

&nbsp;

## [Analyzing rideshare data](https://medium.com/@skm440/analyzing-rideshare-data-a7c83f95cd65)
<img style="float: right; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/map.gif" width="65%" />

I explored the possibility of developing an app that would help rideshare drivers receive bigger payouts for their rides. Since drivers are constantly shifting between rideshare services (always trying to maximize their profits based on surge prices, percent payouts, and general pricing models for each service), I thought to build an app that would put this maximization problem into a quantitative framework. Given the time of day, the driver's location, and other factors (like the weather), which service would be most likely to be most profitable? While the idea had potential, my analysis of the data ultimately proved there to be too much variance for the service be reliable.


&nbsp;


## [Modified labeling system for DeepLabCut](https://github.com/sachaker/deeplabcut_texteam)
<img style="float: right; margin: 10px 15px 15px 0px;" src="{{site.imgurl}}/alternateGUI_20nodes.gif" width="65%"/>

The DLC labeling process for whiskers can be laborious and repetitive. This alternative to [DeepLabCut](https://www.nature.com/articles/s41593-018-0209-y)'s point-and-click labeling allows for rapid labeling of contiguous structures, like whiskers. In this new system, the user drags the cursor along each structure, after which the spline is discretized into a pre-set number of nodes with equal increments along the path. This modification increased our throughput from labeling a frame every minute (at least) to labeling a frame every few seconds. I was very pleased when the [original authors](http://www.mousemotorlab.org/deeplabcut) of the software at Harvard asked if they could include my code in their latest, official version.

&nbsp;

## [Discovering a new protein in Alzheimer's disease](https://drive.google.com/file/d/1cGzeoDXuqn-UVnipOR9pSiZqdJP9OBgw/view?usp=sharing)

<img style="float: center; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/scrn1.png" width="65%"/>


I spent 2 years of my undergraduate career working in the lab of [Dr. Thomas Wisniewski](https://nyulangone.org/doctors/1033103759/thomas-m-wisniewski), who is famous for having co-discovered the role of [APOE](https://en.wikipedia.org/wiki/Apolipoprotein_E) in Alzheimer's disease. The goal was ambitious: we were on a journey to discover a protein that had never before been implicated in the disease. Through immeasurable hours of hard work we were ultimately successful in this pursuit and the outcome of our project has been incredible. Our results were [published](https://actaneurocomms.biomedcentral.com/articles/10.1186/s40478-019-0848-6) and have been read more than 90% of all publications from 2019 (despite being published in its final month!), the conference presentations we delivered received several [major awards](https://cas.nyu.edu/content/dam/nyu-as/cas/documents/deans-undergraduate-research-fund/DURF%20Recipients%202017-18.pdf), [my thesis](https://drive.google.com/file/d/1zqqtPSbplwEJelNPvN9cPh1el9Ua9WOe/view?usp=sharing) won a [university-wide award](https://cas.nyu.edu/content/nyu-as/cas/academic-programs/honors-programs/dean-awards.html), and we were able to blow the doors open to a completely new therapeutic target! At several stages of the project I was able to incorporate my computational inclinations as well. I was incredible lucky to work with such a great team ([Dr. Eleanor Drummond](https://www.researchgate.net/profile/Eleanor_Drummond) and [Geoffrey Pires](https://www.linkedin.com/in/geoffrey-pires-b03877b2)) and I couldn't be more proud of the outcome!


&nbsp;


## [Modeling information transfer in high-noise neural systems](./files/neuronalTelephone.html)

<img style="float: right; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/rotate.gif" width="30%"/>

This program was the first part of my Final Project for [Dr. Alex Reyes](https://as.nyu.edu/faculty/alexander-reyes.html)' course, Network Models. My goal was to determine how information dissapates throughout a network. To do this, I developed a generative model that creates a population of excitatory neurons that synapse onto each other using a probabilistic mode  based on the proximity between the two units. The position of the neuron was generated using a [Gaussian distribution](https://en.wikipedia.org/wiki/Normal_distribution) with parameters in arbitrary units for each of the 3 dimensions. Then, the physiological properties of each unit were generated using the [Hodgkin-Huxley equations](https://en.wikipedia.org/wiki/Hodgkin%E2%80%93Huxley_model), and stochastically fire for the duration of "recording" based on a model I built from a previous assignment. One of these HH units was then selected at random and given a stimulation of a set pattern. The goal of this project was to see how many units in the network show significant alignment with this stimulus (i.e. received the information), and how that decays with distance and with number of units.

&nbsp;

## Motion tracker for fruit fly larvae

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/tracker1.jpg" width="40%"/>

This project was done during my time at University of Michigan for Summer 2017, in the [Collins Lab](https://sites.lsa.umich.edu/collins-lab/) as a National Institute of Health [BP-ENDURE Scholar](http://www.bpendure.org/sacha-mcelligott.html). Researchers in the [Kuwada Lab](https://sites.lsa.umich.edu/kuwada-lab/research/) were studying the effects of various intervention types on larval locomotion, and had been using ImageJ's tracking software, which was rife with errors and caused many frustrations. I approached one of the researchers and mentioned my interest in creating a tracking software, and she was more than happy to offer their database of videos in order for me to try. 


A brief summary of the algorithm: the program iterates through each frame of the video, and starts by binarizing and processing the given frame to ease the object detection of the larvae. From there it computes the borders of all objects within a given size constraint (tailored specifically to the area of a larva), and calculates the [centroid](https://en.wikipedia.org/wiki/Centroid) of those objects. It then stores the pixel coordinates of each detected object in a matrix. After having calculated all the coordinates of all the centroids from each object for all frames, it asks for the user to select the paths for each of the larvae, so as to label the coordinates stored in the coordinate matrix (and to avoid [Kalman filtering](https://en.wikipedia.org/wiki/Kalman_filter) and other slow algorithms for inferring to which larva each coordinate pair belongs). It then iterates through each larval matrix and calculates the [Euclidean distance](https://en.wikipedia.org/wiki/Euclidean_distance) between each object's centroid in consecutive frames for all frames, and stores those distances in a CSV file. Furthermore, it detects whether a larva stopped (paused in its motion) or hit the wall of the dish, and provides a notice in the CSV for all of those events. This was a super fun project and I feel grateful that I was given an opportunity to pursue it.


&nbsp;


## [Tracking and analyzing eye movements in real-time](https://drive.google.com/file/d/1JbnQGaE06BWwYERrD_EwS7khkD_rkpzh/view?usp=sharing)
<img style="float: right; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/1000hz.jpg" width="30%"/>

Despite our experience of perceptual stability, our eyes are constantly in motion, darting around in subtle movements called [saccades](https://en.wikipedia.org/wiki/Saccade) about three times a second. Saccades are used to sample important visual information from our environment, by quickly directing the fovea to relevant stimuli. Past studies have characterized perceptual changes that occur during saccade preparation, yet the physiological mechanisms that drive such changes remain elusive. During my time at the [Paradiso Lab](https://www.paradisolab.net/), we attempted to characterize these mechanisms by delivering [transcranial magnetic stimulation (TMS)](https://www.mayoclinic.org/tests-procedures/transcranial-magnetic-stimulation/about/pac-20384625) to human subjects’ primary visual cortex, a region that has been implicated in saccade-based perceptual changes. We delivered rapid, single TMS pulses during a psychophysical discrimination task at various points relative to the saccade. In doing so, we attempted to abolish these perceptual changes leading up to saccades, and thus expose one link in the chain between physiology and perception. This project was incredibly ambitious and exciting, and I ended up devleoping a full-scale software package, recreating the entire psychophysical task from a past study by [Dr. Marissa Carrasco](https://en.wikipedia.org/wiki/Marisa_Carrasco) and [Dr. Martin Rolfs](http://www.martinrolfs.de/), interfacing with the eye tracking camera and TMS machinery, and developing algorithms to do on-line identification of saccades. The lab has plans to continue this project due to our promising, early results.


&nbsp;


## [Automated quantification of cellular structures](./files/quantifier.md)
<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/quantifier2.png" width="30%"/>

I undertook this project in hopes of avoiding the incredibly monotonous task of manually quantifying thousands of cells for my research project. The program processes an RGB image ([IHC stains](https://en.wikipedia.org/wiki/Immunohistochemistry) are almost always some combination of red, green and blue channels) into a 3D matrix, and allows the user to input a specified channel (e.g. [DAPI](https://en.wikipedia.org/wiki/DAPI) staining for nuclei (blue)) and input the size range of the desired object. It then makes minor contrast adjustments to the binary image so as to emphasize the edges of all enclosed objects, and outlines and stores the boundaries of all objects. The cell array containing all data pertaining to the boundaries is further processed to filter out the objects whose areas do not fit within the inputted size constraints. The remaining objects are outlined with the same color as the channel (yes, I had some fun with the aesthetics) and the number of remaining, bounded objects are counted. I also account for [occlusions](https://stackoverflow.com/questions/2764238/image-processing-what-are-occlusions) (such as clumped nuclei) wherein multiple objects that are too close together for the program to identify (as they exceed the size constraints for a single nucleus), are counted by dividing the area of each clump by the average area of the desired object, and adding that to the total object count. I also made a simple function for this program, just to make it a little simpler to use. This was one of my first software packages and I learned a lot from building it. I also want to quickly express my gratitude the postings of Mathworks user, [Image Analyst](https://www.mathworks.com/matlabcentral/profile/authors/1343420-image-analyst), who helped me with contrast adjustments and thus helped me improve my code.
