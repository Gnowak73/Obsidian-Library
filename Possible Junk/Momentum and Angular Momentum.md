---
tags:
  - Physics
  - CM
  - momentum
  - Moment_of_Inertia
  - angular_momentum
  - Newton
  - rotation
  - rotational_motion
dg-publish: true
mathLink:
---
2Subject: _CM_
Main\_Topic: _Momentum and Angular Momentum_
Applications: _Physics_
Examples: _None_
Class: _Classical Mechanics 1_
Exam: _Exam 1_
Textbook: _None_
Closely\_Related\_To: _[[Newton's Laws of Motion]]_
Cont.\_ of: _None_ 
_
_

Using [[Newton's Laws of Motion]], we can see that as a long as all the internal forces for a system of particles obey Newton's third law, the rate of change of the system's total linear momentum ${\bf{P}}={\bf{p_{1}}}+\ldots+{\bf{p_{n}}}=\sum\limits \bf{p}_{\alpha}$ is determined entirely by the _external_ forces on the system:
$$
\dot{\bf{P}} = {\bf{F}}^{ext}
$$
where ${\bf{F^{ext}}}$ denotes the total external force on the system. Because of the third law, the internal forces all cancel out of the rate of change of the _total_ momentum. In particular, if the system is isolated we have the Principle of Conservation of Momentum.

```ad-Definition
**The Principle of Conservation of Momentum** states: if the net eternal force $\bf{F}^{ext}$ on a N-particle system is zero, the system's total mechanical momentum $\pmb{P}=\sum\limits m_{\alpha}\pmb{v}_{\alpha}$ is constant.
```

#### Rockets
A beautiful example of the use of momentum conservation is the analysis of rocket propulsion. The basic problem that is solved by the rocket is this: With no external agent to push on or be pushed by, how does an object get itself moving? Well, due to Newton's third law, if we were to be on a boat in a lake and say we throw our boot, then the boot will deliver an equal and opposite force, pushing us and the boat in the opposite direction as the boot. This recoil is in essence how a rocket works.

To analyze a rocket's motion, we must examine the total momentum. Consider a rocket with mass $m$, traveling in the positive $x$ direction and ejecting spend fuel at the exhaust speed $v_{ex}$ relative to the rocket. Since the rocket is ejecting mass, the rocket's mass $m$ is steadily decreasing. At time $t$, the momentum is $P(t)=mv$. A short time later at $t+dt$, the rocket's mass is $m+dm$, where $dm$ is negative, and its momentum is $(m+dm)(v+dv)$. The fuel ejected in the time $dt$ has mass $(-dm)$ and velocity $v-v_{ex}$ relative to the ground. 

![[Pasted image 20230927150800.png|center]]

Thus the total momentum (rocket plus the fuel just ejected) at $t+dt$ is 
$$
P(t+dt) = (m+dm)(v+dv) - dm(v-v_{ex}) = mv+m \ dv + dm \ v_{ex}
$$
where we have neglected the doubly small product $dm \ dv$. Therefore, the change in total momentum is 
$$
dP = P(t+dt)  - P(t) = m \ dv + dm \ v_{ex}
$$
If there is a net external force $F^{ext}$, this change of momentum is $F^{ext}dt$. Here, we shall assume that there are no external forces, so that $P$ is constant and $dP = 0$. Therefore,
$$
m \ dv = -dm \ v_{ex}
$$
dividing both sides by $dt$, we can rewrite this as 
$$
m\dot{v} = -\dot{m}v_{ex}
$$
where $-\dot{m}$ is the rate at which the rocket's engine is ejecting mass. This equation looks just like Newton's second law for an ordinary particle, except that the product $-\dot{m}v_{ex}$ on the right plays the role of the force. For this reason this product is often called the **Thrust**:
$$
\text{thrust} = -\dot{m}v_{ex}
$$
(since $\dot{m}$ is negative, this defines the thrust to be positive). This differential equation can be solved by separation of variables or any of the [[ODE First Order Methods]]. Doing so, we get the result
$$
v-v_{0} = v_{ex} \ln\frac{m_{0}}{m}
$$
where $v_{0}$ is the initial velocity and $m_{0}$ is the initial mass of the rocket (including fuel and payload). This result puts a significant restriction on the maximum speed of the rocket. The ratio $\frac{m_{0}}{m}$ is largest when all the fuel is burned and $m$ is just the mass of rocket plus payload.

#### Center of Mass
Let us consider a group of $N$ particles, $\alpha=1,\ldots,N$, with masses $m_{\alpha}$ and positions $\pmb{r}_{\alpha}$ measured relative to an origin $O$. The **center of mass** of this system is defined to be the position (relative to the same origin $O$)
$$
\pmb{R} = \frac{1}{M}\sum\limits_{\alpha=1}^{N}m_{\alpha}\pmb{r}_{\alpha} = \frac{m_{1}\pmb{r}_{1}+\ldots+m_{n}\pmb{r}_{n}}{M}
$$
where $M$ denotes the total mass of all of the particles, $M=\sum\limits m_{\alpha}$. The first thing to note about this definition is that it is a vector equation. The CM position is a vector $\pmb{R}$ with three components and the equation above is equivalent to three equations giving these three components:
$$
X = \frac{1}{M} \sum\limits_{\alpha=1}^{N}m_{\alpha}x_{\alpha}, \quad Y = \frac{1}{M}\sum\limits_{\alpha=1}^{N}m_{\alpha}y_{\alpha}, \quad Z = \frac{1}{M}\sum\limits_{\alpha=1}^{N}m_{\alpha}z_{\alpha}
$$
Either way, the CM position $\pmb{R}$ is a weighted average of the positions $\pmb{r}_{1},\ldots,\pmb{r}_{N}$ in which each position $\pmb{r}_{\alpha}$ is weighted by the corresponding mass $m_{\alpha}$. Let us consider the case of just two particles ($N=2$). In this case, the definition reads 
$$
\pmb{R} = \frac{m_{1}\pmb{r}_{1}+m_{2}\pmb{r}_{2}}{m_{1}+m_{2}}
$$
It is easy to verify that the CM position has several familiar properties. For example, you can show that the CM lies on the line joining the two particles. It is also easy to show that the distances of the CM from $m_{1}$ and $m_{2}$ are in the ratio $\frac{m_{2}}{m_{1}}$, so that the CM lies closer to the more massive particle. 

We can now write the total momentum $\pmb{P}$ of anu $N$-particle system in terms of the system's CM as follows:
$$
\pmb{P} = \sum\limits_{\alpha}P_{\alpha} = \sum\limits_{\alpha}m_{\alpha}\dot{\pmb{r}}_{\alpha} = M\dot{\pmb{R}}
$$
This remarkable result says that the total momentum of the $N$ particles is exactly the same as that of a single particle of mass $M$ and velocity equal to that of the CM. We get an even more striking result when we differentiate this. According to the momentum principle, the derivative of $\pmb{P}$ is just $\pmb{F}^{ext}$. Therefore, this implies that 
$$
\pmb{F}^{ext} = M \ddot{R}
$$
That is, the center of mass $\pmb{R}$ moves exactly as if it were a single particle of mass $M$, subject to the net external force on the system. This result is the main reason why we can often treat extended bodies, such as baseballs and planets, as if they were point particles. Provided a body is small compared to the scale of its trajectory, its CM position $\pmb{R}$ is a good representative of its overall location, and $\pmb{R}$ moves just like a point particle. 

Given the importance of the CM, you need to feel comfortable calculating the CM position for various systems. You may have had plenty of practice before such as in [[Moment of Inertia and Center of Mass]]. One important point to bear in mind is that when the mass in a body is distributed continuously, the sum in the definition of our CM goes over to an integral,
$$
\pmb{R} = \frac{1}{M}\int\limits\pmb{r} \ dm = \frac{1}{M}\int\limits \rho \pmb{r} \ dV
$$
where $\rho$ is the density of the body, and $dV$ denotes an element of volume, and the integral runs over the entire body. We shall be using similar integrals to evaluate the moment of inertia tensor later on.

#### Angular Momentum for a Single Particle
The **angular momentum** $l$ of a single particle is defined as the vector 
$$
\pmb{l} = \pmb{r}\times \pmb{p}
$$
Here, $\pmb{r}\times \pmb{p}$ is the vector product of the particle's position vector relative to the chosen origin $O$ and the momentum. Notice that because $\pmb{r}$ depends on the origin, so does $\pmb{l}$. The time rate of change of $\pmb{l}$ is easily found to be:
$$
\dot{\pmb{l}} = \frac{d}{dt}(\pmb{r}\times\pmb{p}) = (\dot{\pmb{r}} \times \pmb{p}) + (\pmb{r}\times\dot{\pmb{p}})
$$
(note that the product rule can be used for differentiating vector products as long as the vectors are kept in the right order). In the first term on the right, we can replace $\pmb{p}$ by $m\dot{\pmb{r}}$, and, because the cross product of any two parallel vectors is zero, the first term is zero. In the second term, we can replace $\dot{\pmb{p}}$ by the net force $\pmb{F}$ on the particle, and we get
$$
\dot{\pmb{l}} = \pmb{r} \times \pmb{F} \equiv \Gamma
$$
where $\Gamma$ denotes the net torque about $O$ on the particle, defined as $\pmb{r}\times \pmb{F}$. In other words, this equation above says that the rate of change of a particle's angular momentum about the origin $O$ is equal to the net applied torque about $O$. This is the rotational analog of the equation $\dot{\pmb{p}}=\pmb{F}$ for the linear momentum. 

```ad-Remember
Remember that in rotational motion, $\pmb{v}=\omega \times \pmb{r}$. This can be derived from polar coordiantes. 
```


###### Kepler's Second Law
The derivation of Kepler's second law using this rotational motion can be seen on page 92. in [[taylor-2005-classical-mechanics.pdf|Taylor CM textbook]]. 

##### Angular Momentum for Several Particles
Let us next discuss a system of $N$ particles, $\alpha=1,2,\ldots,N$ each with its angular momentum $\pmb{l}_\alpha=\pmb{r}_{\alpha}\times \pmb{p}_{\alpha}$ (with all of the $\pmb{r}_{\alpha}$ measured from the same origin $O$). We define the **total angular momentum** $L$ as 
$$
\pmb{L} = \sum\limits_{\alpha=1}^{N}\pmb{l}_{\alpha} = \sum\limits_{\alpha=1}^{N} \pmb{r}_{\alpha}\times \pmb{p}_{\alpha}
$$
Differentiating with respect to $t$ we find that 
$$
\dot{\pmb{L}} = \sum\limits_{\alpha}\dot{\pmb{l}}_{\alpha} = \sum\limits_{\alpha}\pmb{r}_{\alpha} \times \pmb{F}_{\alpha},
$$
where, as usual, $\pmb{F}_{\alpha}$ denotes the net force on particle $\alpha$. This result shows that the rate of change of $\pmb{L}$ is just the net torque on the whole system, an important result in its own right. However, we shift our interest to separate effects of the internal and external forces. We write $\pmb{F}_\alpha$ as 
$$
\text{net force on particle $\alpha$} = \pmb{F}_{\alpha} = \sum\limits_{\beta\neq \alpha} \pmb{F}_{\alpha \beta} + \pmb{F}^{ext}_{\alpha}
$$
where, as before, $\pmb{F}_{\alpha \beta}$ denotes the force exerted on particle $\alpha$ by particle $\beta$, and $\pmb{F}^{ext}_{\alpha}$ is the net force exerted on particle $\alpha$ by all agents outside our $N$-particle system. Substituting this into $\dot{\pmb{L}}$, we find that (remember that cross product is distributive)
$$
\dot{\pmb{L}} = \sum\limits_{\alpha}\sum\limits_{\beta \neq \alpha} \pmb{r}_{\alpha}\times \pmb{F}_{\alpha \beta} + \sum\limits_{\alpha}\pmb{r}_{\alpha}\times \pmb{F}^{ext}_{\alpha}
$$
This equation corresponds to the discussion of linear momentum in [[Newton's Laws of Motion]], and we can rework it in much the same way. We can regroup the terms of the double sum, pairing each term $\alpha \beta$ with the corresponding term $\beta \alpha$, to give 
$$
\sum\limits_{\alpha}\sum\limits_{\beta \neq \alpha} \pmb{r}_{\alpha}\times \pmb{F}_{\alpha \beta} = \sum\limits_{\alpha}\sum\limits_{\beta>\alpha} (\pmb{r}_{\alpha}\times \pmb{F}_{\alpha \beta} + \pmb{r}_{\beta} \times \pmb{F}_{\beta \alpha})
$$
If we assume that all the internal forces obey Newton's third law: $\pmb{F}_{\alpha \beta} = -\pmb{F}_{\beta \alpha}$, then we can rewrite this sum as 
$$
\sum\limits_{\alpha}\sum\limits_{\beta>\alpha}(\pmb{r}_{\alpha} - \pmb{r}_{\beta}) \times \pmb{F}_{\alpha \beta}
$$
To understand this sum, we must examine the vector $(\pmb{r}_{\alpha}-\pmb{r}_\beta)=\pmb{r}_{\alpha \beta}$, say. We see that $\pmb{r}_{\alpha \beta}$ is the vector pointing toward particle $\alpha$ from particle $\beta$. If, in addition to satisfying the third law, the forces $\pmb{F}_{\alpha \beta}$ are all _central_ (directed along the line joining the two centers), then the two vector $\pmb{r}_{\alpha \beta}$ and $\pmb{F}_{\alpha \beta}$ point along the same line, and their cross products is zero. 

We conclude that, provided our various assumptions are valid, the double sum is zero. The remaining single sum is just the net external torque, and we conclude that 
$$
\dot{\pmb{L}} = \pmb{\Gamma}^{ext}
$$
In particular, if the net external torque is zero, we have the 
```ad-Definition
**The Principle of Conservation of Angular Momentum**: if the net external torque on an $N$-particle system is zero, the system's total angular momentum $\pmb{L}=\sum\limits \pmb{r}_{\alpha} \times \pmb{p}_{\alpha}$ is constant. 
```

The validity of this principle depends on our two assumptions that all internal forces $\pmb{F}_{\alpha \beta}$ are central and satisfy the third law. Since these assumptions are almost always valid, the principle (as stated) is likewise. It is of the greatest utility in solving many problems. 

#### The Moment of Inertia 
It is worth noting that the calculation of angular momenta does not always require one to go back to the basic definition as stated before. The rather complicated sum can be expressed in terms of the moment of inertia and the angular velocity of rotation. Specifically, if $\omega$ is along the axis of rotation, we can write $\pmb{L}=I\pmb{\omega}$. In general, $I = \sum\limits m_{\alpha} r_{\alpha}^{2}$, where $r_{\alpha}$ is the distance of the mass $m_{\alpha}$ to the axis of rotation.

##### Angular Moment about the CM
The conservation of angular momentum and the more general result $\dot{\pmb{L}}=\pmb{\Gamma}^{ext}$ were derived on the assumption that all quantities were measured in an inertial frame, so that Newton's Second Law could be invoked. This required that both $\pmb{L}$ and $\pmb{\Gamma}^{ext}$ be measured about an origin $O$ fixed in some inertial frame. Remarkably, the same two results also hold if $\pmb{L}$ and $\pmb{\Gamma}^{ext}$ are measured about the center of mass$-$even if the CM is being accelerated and so is not fixed in an inertial frame. That is,
$$
\frac{d}{dt}\pmb{L}_{CM} = \pmb{\Gamma}^{ext}_{CM}
$$
and hence, if $\pmb{\Gamma}^{ext}_{CM}=0$, then $\pmb{L}_{CM}$ is conserved. We shall prove this result later. We mention is now because it allows a very simple solution to various problems.
