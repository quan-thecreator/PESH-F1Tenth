[[Durrant-Whyte_Bailey_SLAM-tutorial-I.pdf|text]]
# SLAM by Durrant 2006 Part 1
## Notes on the Abstract

There appear to be several reasons why this paper is a especial industry favorite as it clearly opens with the following hooks:
- targets small, mobile, embedded and low power systems of the time
- and discusses *implementation* in a ==tutorial== format

## Discourse
### Introduction
Starting with a definition, the Simultaneous Localisation and Mapping (SLAM) problem/problem scenario (more on this later) requires and the checks the possibility of a *"mobile robot"* incrementally building a map of its vicinity while also determining its location in the course, when placed into an unknown and un-cached environment. It is of an intrinsic essence of said problem to have very influential solution in the field of robotics, should they be found. Needless to say, this is a fundamental problem of robotic motion.

### The Problem
![[Pasted image 20231120122338.png]]
#### Defining variables
In the image above, the color filled icons represent what the robot perceives using its sensors or LiDAR instruments, while the icons without a fill represent true vectors and landmarks. Directed triangles represent the path the robot is taking, while all forms of lines represent motion vectors fitting a curve. The indicated variable $k$ represent the time instance at which the labeled vector is being considered. The unexplained variable $i$ is an iterator of the the closest landmark given a $k^{th}$ vector.

- 
## Citation
H. Durrant-Whyte and T. Bailey, "Simultaneous localization and mapping: part I," in IEEE Robotics & Automation Magazine, vol. 13, no. 2, pp. 99-110, June 2006, doi: 10.1109/MRA.2006.1638022.

#paper-review #SLAM