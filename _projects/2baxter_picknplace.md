---
layout: project
title: Baxter Pick and Place
date: October, 2015
image: https://github.com/MikhailTodes/portfolio/blob/gh-pages/public/images/baxter_final_pose.png?raw=true
---

## Overview
As a final project for the Embedded Systems course I took, we were required to use Rethink Robotics' Baxter for a pick and place application.

## Additional Components

The basic project requirement was for Baxter to pick up 6 objects and place them in a container on the side. Extra marks were given for the following:

* Picking up different shaped objects.
* Picking up different coloured objects.
* The speed at which Baxter could successfully pick and place the 6 items.
* Being able to move the objects around during the routine and allowing Baxter to reconfigure his movements dynamically. 
* Picking up objects in any orientation.

## The Strategy
The first task tackled was to build an IK (inverse kinematics) solver so that all Baxter's joint angles could be calculated in order to send his grippers (end effector) to whatever position was needed to pick up the object. 

The second task was the image processing. The camera in the wrist of Baxter's right hand was used to sweep across the top of the table and find the objects. Once an object was found, a bounding rectangle was drawn around it with the lowest border line being coloured red as apposed the yellow others. Baxter would then reconfigure the orientation of his gripper by adjusting until the gradient of the red line was zero.

Finally Baxter's arm was lowered to pick the object and place it in the container set to the side of the table. 

Baxter managed to successfully locate, orientate, pick, and place six objects of varying shapes, sizes, and colour in a time of 1m46s. An unbeaten time by any other challengers. 

For a few creativity points and a smile from the judges, Baxter was set to strike a cheerleaders pose with a big smile when there were no more objects detected for pick up.

## Code
The projet write up as well as all the code written can be found <a href="https://github.com/therrma2/Baxter-Pick-And-Place" target="_blank">here</a>.

## Video
<iframe width="560" height="315" src="https://www.youtube.com/embed/Uo60e5Leo50" frameborder="0" allowfullscreen></iframe>
