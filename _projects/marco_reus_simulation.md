---
layout: project
title: Simulating Marco Reus's Unbelievable Trick
date: December 11 2014
image: https://cloud.githubusercontent.com/assets/4311090/12005453/2ece53de-ab6b-11e5-9c88-027f03b2bcbb.jpg
---
## Overview
+ If you google Marco Reus unbelievable trick you get a video where he kicks one ball into the air then kicks a second one which hits the first ball mid-flight and hits the first ball into the goal. The goal of this project was to simulate this in Mathematica.
+ The system is analogous to a particle in gravity but with various inital velocities and stating positions for each ball. I solved my Euler Lagrange Equations and equated them to the external force on the system which happens to be air resistance.
+ I then solved the resulting equations with NDSolve. I had to play around with the initial values of x1[t],x1’[t],y1[t],y1’[t],theta[t] and theta[t] to get initial conditions under which both balls would collide. To make sure my animation was right I plotted the corresponding solutions of NDSolve against time and I compared it to the parametricplot whhich shows the bodies trajectories. This way I knew that there was actually a time when both balls would collide, if you just animate they collide all the time.
+ I then added an impact condition which occurs when both balls are at the same height above the ground and the only distance between them is the sum of the 2 radii between the balls.
+ I found the time of Impact with NDSolve, substituted the time of impact into my solutions, solved the impact equations, updated my initial conditions and solved again.

[Here's the code](mailto: chu-chu@u.northwestern.edu)

<iframe width="560" height="315" src="https://www.youtube.com/embed/puz5LF2lGH8" frameborder="0" allowfullscreen></iframe>
