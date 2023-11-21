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

- $\vec{x_k}$ is the state vector of the robot at time $k$
- $\vec{u_k}$ is the change vector applied at $k-1$ to change $\vec{x_{k-1}}$ to $\vec{x_k}$
- $\vec{m_i}$ is a offset/erorr vector from the estimated to true location of a landmark given landmark of identity $i$, assuming the true location is *time invariant*
- $z_{i,k}$ is an observation pertaining to the ==location== **of** the $i^{th}$ landmark at time $k$. When referring to a set or history of such measurements, it is conventional short hand to denote them as $z_k$
##### Set definitions
- $X_{0:k} = {\lbrace x_0,x_1,...,x_k \rbrace}= {\lbrace X_{1:k-1},x_k \rbrace} \rightarrow$  The history of robot locations
- $U_{1:k} = {\lbrace u_1,u_2,...,u_k \rbrace}= {\lbrace U_{1:k-1},u_k \rbrace} \rightarrow$  The history of control vectors
- $m$ is the set of all landmarks
- $Z_{1:k} = {\lbrace z_1,z_2,...,z_k \rbrace}= {\lbrace Z_{1:k-1},z_k \rbrace} \rightarrow$  The historical set of all landmark observations

### Probabilistic SLAM
The probability distribution given time $k$:
$$
P(x_{k},m \vert Z_{1:k},U_{1:k},x_0)
$$
This distribution describes the *joint* end density of the coplanar  measurements of landmark location and vehicle state (losing a dimension or two of vehicle state vector.) Since a vehicle control vector is improbable to be perfectly implemented in a real-world situation, and the change in measurements, a temporally recursive computations are desirable. 
It is important to understand that this distribution is possible when *given* the set $U_{0:k}$, the control vectors *including* $u_{k}$.  This can be read as the probability of a random $\vec{p_k}$ taking on the desired value of $\vec{x_k}$ in *conjunction* with $i_n$ number of random vectors taking on the values in set $m$  given observations and adjustment control vectors and a initial positional state vector $x_0$. Importantly, this is a computation of the probability of *both* observing the correct landmarks *in* the map, *and* possessing the desired state $x_k$.
In direct corollary, there exist two vital probabilistic models:

Model | Distribution 
-- | -- 
Observation | $P(z_{k}\vert x_k,m)$
Motion | $P(x_{k}\vert x_{k-1},u_k)$


## Citation
H. Durrant-Whyte and T. Bailey, "Simultaneous localization and mapping: part I," in IEEE Robotics & Automation Magazine, vol. 13, no. 2, pp. 99-110, June 2006, doi: 10.1109/MRA.2006.1638022.

# Credits
Author of this note: Krishna Ayyalasomayajula

#paper-review #SLAM #krishna #literature-review