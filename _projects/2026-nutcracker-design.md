---
layout: project
title: Nutcracker design
description: Class project with Graphs
technologies: []
image: /assets/images/nutcrackerfbd.jpg
---

As part of a class project, I designed a lever nut cracker for macadamian nuts. The nut cracker needs to have the appropriate dimensions to crack macadamian nuts open when applied the average grip load, and can fit the average macadamian nut inside it and still has an appropriate angle to grip it.

The load needed for an average macadamian nut to be cracked open is 222.18kg, and the average human grip force is 40kg. The diameter of an average macadamian nut is about 2.5cm.

Since the nut cracker is a simple lever structure, the ratio between the output load and the given load is the same as the ratio between the distance of the joint to the point where grip load is applied and the distance of the joint to the point where output load is applied, according to the equilibrium of moments.

<img src="https://latex.codecogs.com/svg.image?\sum\vec{M}=\vec{L}_1(-\text{load}_{out})+\vec{L}_2(\text{load}_{in})" />

<img src="https://latex.codecogs.com/svg.image?\frac{output\ force}{given\ load}=\frac{222.18}{40}=5.55" />

Thus the ratio of the distances must be at least 5.55 too. In the design the ratio would be 6.

![Photo of fbd of nutcracker]({{ "/assets/images/nutcrackerfbd.jpg" | relative_url }}){: .inline-image-l}

In this free body diagram L1 is the distance between the joint and output force, L2 is the distance between the given load and the joint, α is the angle of the nutcracker at the joint, θ is the angle the handle deviates from its original direction.

For the nut cracker to be at a comfortable angle when a nut of diameter 2.5cm is put inside it, I've decided a length of 3 cm for L1 and an angle of 20 degrees for θ is appropriate. L2 is thus 18 cm long.

Calculations:

<img src="https://latex.codecogs.com/svg.image?\tan^{-1}(\alpha)=\frac{3.5/2}{3}\approx30^\circ" />

<img src="https://latex.codecogs.com/svg.image?\tan(10^\circ)=\frac{d'}{L_2-L_1}" />

<img src="https://latex.codecogs.com/svg.image?d'=2.64\text{ cm}" />

<img src="https://latex.codecogs.com/svg.image?\text{distance}=2(2.64)+2.5=7.78\text{ cm}" />

Since the handle is crooked the distance between the two points of applied load is 7.78cm, which is within comfortable range (6–10cm) of a human grip.

Now, assuming the handle of the nutcracker is not rigid, but are beams which bend under point pressure from the actuator and the nut.

The location of maximum elastic deflection in the handles would be the longer end of the handle. Since the distance of deflection at the joint and where the nutcracker is in contact with the nut is 0,

<img src="https://latex.codecogs.com/svg.image?v(x)=\begin{cases}222.18\times9.81\times\cos(20^\circ)=2048.14\text{ N} & 0<x<3\\40\times9.81=392.4\text{ N} & 3\leq x\leq18\end{cases}" />

<img src="https://latex.codecogs.com/svg.image?\sum\vec{M}=0:\ M(x)=\begin{cases}2048.14x & 0<x<3\\7063.2-392.4x & 3\leq x\leq18\end{cases}" />

<img src="https://latex.codecogs.com/svg.image?EIy=\int\int M\,dx\,dx=\begin{cases}1024.07x^3+C_1x+C_2 & 0<x<3\\3531.6x^2-65.4x^3+C_3x+C_4 & 3\leq x\leq18\end{cases}" />

Applying boundary and continuity conditions:

<img src="https://latex.codecogs.com/svg.image?\begin{cases}y(0)=0\\y(3^-)=y(3^+)\\y'(3^-)=y'(3^+)\\y(18)=0\end{cases}" />

Solving gives constants (approx):

<img src="https://latex.codecogs.com/svg.image?C_1=-9216.63,\ C_2=0,\ C_3=-18433.26,\ C_4=27649.89" />

<img src="https://latex.codecogs.com/svg.image?y(x)=\begin{cases}\frac{1}{EI}(1024.07x^3-9216.63x) & 0<x<3\\\frac{1}{EI}(3531.6x^2-65.4x^3-18433.26x+27649.89) & 3\leq x\leq18\end{cases}" />

According to the function y(x), the deflection at point B would be smaller than the deflection at point C.

[image of upper handle with points ABC and angles]

For the vertical deflection of the handle to be below 2% of its length:

<img src="https://latex.codecogs.com/svg.image?\delta_{max}=0.02\times18\text{ cm}=0.36\text{ cm}=0.0036\text{ m}" />

Using maximum deflection at (x=18):

<img src="https://latex.codecogs.com/svg.image?y_{max}\approx\frac{1.12\times10^5}{EI}" />

Thus:

<img src="https://latex.codecogs.com/svg.image?EI=\frac{1.12\times10^5}{0.0036}=3.11\times10^7\text{ N\cdot mm}^2" />

With:

<img src="https://latex.codecogs.com/svg.image?E=200\text{ GPa}=2\times10^5\text{ N/mm}^2" />

<img src="https://latex.codecogs.com/svg.image?I=\frac{3.11\times10^7}{2\times10^5}=155.5\text{ mm}^4" />

Thus, a suitable cross section must have:

<img src="https://latex.codecogs.com/svg.image?I\geq155.5\text{ mm}^4" />

A small rectangular cross section satisfying this:

<img src="https://latex.codecogs.com/svg.image?I=\frac{bh^3}{12}" />

<img src="https://latex.codecogs.com/svg.image?b=5\text{ mm},\ h=10\text{ mm}" />

<img src="https://latex.codecogs.com/svg.image?I=\frac{5(10)^3}{12}=416.7\text{ mm}^4" />

This exceeds the required value, ensuring safety and minimal deflection.

Cross-sectional area:

<img src="https://latex.codecogs.com/svg.image?A=bh=50\text{ mm}^2" />

Thus, the nutcracker would look like this:

[image of the nutcracker and its cross section]

