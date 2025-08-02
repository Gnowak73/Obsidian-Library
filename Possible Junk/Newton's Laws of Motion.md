---
tags:
  - Newton
  - motion
  - Physics
  - CM
dg-publish: true
mathLink:
---
Subject: _CM_
Main\_Topic: _Newton's Laws of Motion_
Applications: _Physics_
Examples: _None_
Class: _Classical Mechanics 1_
Exam: _Exam 1_
Textbook: _None_
Closely\_Related\_To: _[[ODE Second Order Methods]],[[Wave Equation D'Alambert]],[[Projectiles and Charged Particles]],[[Momentum and Angular Momentum]]_
Cont.\_ of: _None_ 
_
_

Newton's three laws of motion are formulated in terms of four crucial underlying concepts: the notions of space, time, mass, and force. We will look at each of these in order.

##### Space 
Each point $P$ of a three-dimensional Euclidean space ([[Vector Space]]) in which we live can be labeled by a position vector $\bf{r}$ which specifies the distance and direction of $P$ from a chosen origin. In Euclidean geometry, we introduce three unit vectors for the orthogonal axis, such that we can write 
$$
{\bf{r}} = x \hat{\bf{x}}+y\hat{\bf{y}}+z\hat{\bf{z}} = \sum\limits_{i=1}^{3}r_{i}\bf{e}_{i}.
$$
Sometimes $\hat{\bf{x}},\hat{\bf{y}},\hat{\bf{z}}$ are denoted by $\bf{i},\bf{j},\bf{k}$ or $\bf{e}_{1},\bf{e}_{2},\bf{e}_{3}$ as seen in the sum above. We can also write in component form,
$$
{\bf{r}}=(x,y,z)
$$
The rules of vector operations follow as before in [[Vector Space]], along with the definitions for projections, inner products, cross products, etc. in [[Vector Inner Product]] and [[Vector Linear Algebra]]. 

###### Differentiation of Vectors
The definition of the derivative of a vector is closely analogous to that of a scalar, such that 
$$
\frac{d \bf{r}}{dt} = \lim_{\Delta t \rightarrow 0} \frac{\Delta {\bf{r}}}{\Delta t} = \lim_{\Delta t \rightarrow 0} \frac{{\bf{r}}(t+\Delta t)-{\bf{r}}(t)}{\Delta t} = \lim_{t \rightarrow \Delta t} \frac{{\bf{r}}(t)-{\bf{r}}(\Delta t)}{t-\Delta t}
$$
Thus, we simply do the ordinary derivative, component wise (if its cartesian coordinates). Everything such as the product rule, chain rule, etc. is directly applicable to vectors. It is worth noting, however, that when we differentiate vector, we also differentiate the unit vectors. Hence, for cartesian coordinates, since the unit vectors are constant, we simply differentiate component wise. This is not true, however, for polar coordinates or other curvilinear coordinates. 

##### Time
The classical view of time is that there is a single universal parameter $t$ on which all observers agree. That is, if all observers are equipped with accurate clocks, all property synchronized, then they will all agree as to the time which any even occurs. Even though this is not true for relativity, for classical mechanics this mechanism is accurate. 

##### Reference Frames 
All physically equivalent frames are "inertial", in other words, they do not accelerate. And yes, rotating frames do count as acceleration in the radial direction from the centripetal force and angularly because the velocity vector is constantly changing direction. Newton's laws are built in the assumption of inertial frames. However, we can still use inertial frames, we just have to mind using either a pseudoforce or a nonstandard formulation of Newton's Laws. 

#### Newton's Laws

**Newton's First Law:**  In the absence of forces, a particle moves with constant velocity $\bf{v}$

**Newton's Second Law:**  For any particle of mass $m$, the net force $\bf{F}$ on the particle is always equal to $m$, the mass, times the particle's acceleration, $\bf{a}$. 
$$
{\bf{F}} = m {\bf{a}} = \frac{d \bf{p}}{dt}
$$
where ${\bf{p}}=m{\bf{v}}$. 

**Newton's Third Law:**  Every force has an equal and opposite reaction. 

**Remark.**  From Newton's Second Law, we can derive the conservation of momentum. 

##### Newton's Second Law in Polar Coordinates
As stated before, we can rewrite Newton's Second Law using a different vector basis. Let us say we are working in polar coordinates, then the position vector is ${\bf{r}}=r \hat{\bf{r}}$. Now, using our knowledge from [[Vectors, 1-Forms]], we could write 
$$
{\bf{F}} = m {\bf{a}} = m \frac{d^{2} {\bf{r}}}{dt^{2}} =\frac{d}{dt}\left( m \frac{dr}{dt} {\hat{\bf{r}}}+mr \frac{d{\hat{\bf{r}}}}{dt} \right) = m \frac{d^{2}r}{dt^{2}} \hat{\bf{r}}+m \frac{dr}{dt} \frac{d\hat{\bf{r}}}{dt} + m \frac{dr}{dt} \frac{d \hat{\bf{r}}}{dt} + mr \frac{d^{2}\hat{\bf{r}}}{dt^{2}} 
$$
$$
=m \frac{d^{2}r}{dt^{2}} \hat{\bf{r}} + m \frac{dr}{dt}\dot{\theta}\hat{\bf{\theta}} + m \frac{dr}{dt}\dot{\theta}\hat{\bf{\theta}} + mr\ddot{\theta} \hat{\bf{\theta}} + \dot{\theta} \frac{d \hat{\bf{\theta}}}{dt} 
$$
$$
=m \frac{d^{2}r}{dt^{2}} \hat{\bf{r}} + m \frac{dr}{dt}\dot{\theta}\hat{\bf{\theta}} + m \frac{dr}{dt}\dot{\theta}\hat{\bf{\theta}} + mr\ddot{\theta} \hat{\bf{\theta}} - \dot{\theta}^{2} \hat{\bf{r}}
$$
Now, we can write 
$$
{\bf{F}} = m {\bf{a}} = m\left( \frac{d^{2}r}{dt^{2}}-r \dot{\theta}^{2}\right)\hat{\bf{r}} + m\left(  2\frac{dr}{dt}\dot{\theta} + r\ddot{\theta}\right)\hat{\bf{\theta}}
$$
From this we can easily tell what the components of the acceleration are. If we were to assume that there a uniform circular motion with $\frac{dr}{dt}=0, \frac{d^{2}r}{dt^{2}}=0$, we can readily derive the formula for the centripetal force. 





