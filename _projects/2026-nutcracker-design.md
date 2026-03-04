---
layout: project
title: Nutcracker design
description: Class project with Graphs
technologies: []
image: /assets/images/nutcrackerfbd.jpg
---


As part of a class project, I designed a lever nut cracker for macadamian nuts. The nut cracker needs to have the appropriate dimensions to crack macadamian nuts open when applied the average grip load, and can fit the average macadamian nut inside it and still has an appropriate angle to grip it.

The load needed for an average macadamian nut to be cracked open is 222.18kg, and the average human grip force is 40kg. The diameter of an avergae macadamina nut is about 2.5cm.

Since the nut cracker is a simple lever structure, the ratio between the output load and the given load is the same as the ratio between the distance of the joint to the point where grip load is applied and the distance of the joint to the point where output load is applied, according to the equlibrium of moments.

Calculations:

<img src="https://latex.codecogs.com/svg.image?\sum&space;\vec{M}&space;=&space;\vec{L}_1(-\text{load}_{\text{out}})&plus;\vec{L}_2(\text{load}_{\text{in}})" style="vertical-align:middle" />

<img src="https://latex.codecogs.com/svg.image?\frac{output force}{given load}=\frac{222.18}{40}=5.55" title="\frac{output load}{given load}=\frac{222.18}{40}" /></p>

Thus the ratio of the distances must be at least 5.55 too. In the design the ratio would be 6.

![Photo of fbd of nutcracker]({{ "/assets/images/nutcrackerfbd.jpg" | relative_url }}){: .inline-image-l}
In this free body diagram L1 is the distance between the joint and output force, L2 is the distance between the given load and the joint, <img src="https://latex.codecogs.com/svg.image?\alpha" style="vertical-align:middle" /> is the angle of the nutcracker at the joint. <img src="https://latex.codecogs.com/svg.image?\theta" style="vertical-align:middle" /> is the angle the handle deviates from its original direction.

For the nut cracker to be at a comfortable angle when a nut of diameter 2.5cm is put inside it, I've decided a length of 3 cm for L1 and an angle of 20 degrees for <img src="https://latex.codecogs.com/svg.image?\theta" style="vertical-align:middle" /> is appropriate.
L2 is thus 18 cm long.

Calculations:

<img src="https://latex.codecogs.com/svg.image?\tan^{-1}(\alpha)=\frac{3.5/2}{3}\approx30^{\circ}" style="vertical-align:middle" />

<img src="https://latex.codecogs.com/svg.image?\tan(10^{\circ})=\frac{d'}{L_2-L_1}" style="vertical-align:middle" />

d' = 2.64cm

<img src="https://latex.codecogs.com/svg.image?\text{distance}=2.64\times2+2.5=7.78\text{cm}" style="vertical-align:middle" />

Since the handle is crooked the distance between the two points of applied load is 7.78cm, which is within comfortable range(6-10cm) of a human grip.
