---
layout: gallery
title: Quantifying nuclei
---

# The Problem
#### [Immunohistochemistry](https://en.wikipedia.org/wiki/Immunohistochemistry) is a high-specifity method that uses tagged antibodies to identify proteins in tissue. This method enables the use of fluorescent markers that glow when bound to the target protein and allow researchers to visualize the expression of the protein in the given tissue. Despite the popularity of this method, tools for quantifying structures remain largely inaccessible and researchers typically quantify the stained structures manually (loose estimation is much more common than anyone will readily admit), which is a burden on both the researcher's time as well as the integrity of their data. Since you can stain for up to three proteins ("red", "green", "blue"), this would typically entail 3x the work load!

# The Solution
#### To avoid having to do this task for many hundreds of images (the number of hours would have been incalculable), I built a system that would automatically identify and count structures from images of our stained tissue. Let's look at an example to understand how the program works:

1. Start with an image

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/quantifier1.png" width="100%" />

2. Split into color channels

3. Binarize the image and sharpen borders

4. Identify objects

5. Count objects

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/quantifier2.png" width="100%" />


#### Another example, this time with morphologically weird objects (clear-cut circles, like the nuclei above, are easiest)

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/original.jpg" width="100%" />

Now we split the image into each of the RGB channels

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/red.jpg" width="100%" />

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/green.jpg" width="100%" />

<img style="float: left; margin: 0px 15px 15px 0px;" src="{{site.imgurl}}/blue.jpg" width="100%" />

#### Awesome! It quantifies these objects no problem!

#### I love building simple tools to automate or aid in menial tasks, and have seen how severely untapped such tools across scientific disciplines!
