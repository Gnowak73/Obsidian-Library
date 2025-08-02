---
tags:
  - Physics
  - CM
  - projectile
  - kinematics
  - charge
  - particles
  - resistance
  - air
  - drag
dg-publish: true
mathLink:
---
Subject: _CM_
Main\_Topic: _Projectile Motion and Charged Particles_
Applications: _Applications of Physics to kinematics and charged particles in fields_
Examples: _None_
Class: _Classical Mechanics 1_
Exam: _Exam 1_
Textbook: _None_
Closely\_Related\_To: _[[Newton's Laws of Motion]]_
Cont.\_ of: _None_ 
_
_

Let us begin by discussing some of the basic properties of the resistive force, or **drag**, $\bf{f}$ of the air, or other mediums, through which an object is moving. The most obvious fact about air resistance, well known to anyone who can ride a bicycle, is that it depends on the speed $v$, of the object concerned. In addition, the direction of the force due to motion through the air is opposite to the velocity $\bf{v}$. For certain objects, such as a nonrotating sphere, this is exactly true, and for many it is a good approximation. You should, however, be aware that there are situations where it is certainly not true: the force of the air on an airplane wing has a large horizontal component, called the **lift**. Nevertheless, let us assume that $\bf{f}$ and $\bf{v}$ point in opposite directions. That is, we for now will only consider objects where the horizontal component of the drag is $0$ (exactly or approximately). 

Let us first consider a projectile in the air:

![[Pasted image 20230918192809.png|center]]

We see that 
$$
{\bf{f}} = -f(v) \hat{\bf{v}}
$$
where $\hat{\bf{v}} = \frac{\bf{v}}{|\bf{v}|}$ is the unit vector in the direction of $\bf{v}$. The function $f(v)$ that gives us the magnitude of the air resistance varies with $v$ in a complicated way, especially as the object's speed approaches the speed of sound. However, at low speeds it is often a good approximation (originating from the [[Taylor Series]]) to write 
$$
f(v) = bv+cv^{2} = f_{lin}+f_{quad}
$$
where $f_{lin}$ and $f_{quad}$ stand for the linear and quadratic terms respectively. 

The physical origins of these two terms are quite different. The linear term arises from the viscous drag of the medium and is generally proportional to the viscosity of the medium and the linear size of the projectile. The quadratic term arises from the projectiles having to accelerate the mass of air with which it is continually colliding with and is proportional to the density of the medium and the cross-sectional area of the projectile. 

In particular, for a spherical projectile, the coefficients $b$ and $c$ in $f(v)$ have the form 
$$
b=\beta D \quad \text{and} \quad c = \gamma D^{2}
$$
where $D$ denotes the diameter of the sphere and the coefficients $\beta$ and $\gamma$ depend on the nature of the medium. For a spherical projectile in the air at STP, they have the approximate values 
$$
\beta = 1.6 \times 10^{-4} N \cdot \frac{s}{m^{2}}
$$
and 
$$
\gamma = 0.25 \ N\cdot \frac{s^{2}}{m^{4}}
$$

**Remark.**  Remember, these are ONLY valid for a sphere moving through air at STP. Nevertheless, they give at least a rough idea of the important of the drag force even for non-spherical bodies moving through gases at any normal temperatures and pressures.  

If often happens that we can neglect one of the terms in $f(v)$ compared to the other, and this simplifies the task of solving [[Newton's Laws of Motion]]. To decide whether this does happen in a given problem, and which term to neglect, we need to compare the sizes of the two terms 
$$
\frac{f_{quad}}{f_{lin}} = \frac{cv^{2}}{bv} = \frac{\gamma D}{\beta}v = \left(1.6 \times 10^{3} \ \frac{s}{m^{2}}\right)Dv
$$
if we use the values $\beta$ and $\gamma$ for a sphere in air. In a given problem, we have only to substitute the values of $D$ and $v$ into this expression to find out if one of the terms can be neglected.

First, there are objects for which the drag force is dominantly linear, and the quadratic force can be neglected -- notably very small liquid drops in the air, but also slightly larger objects in a very viscous fluid, such as a ball moving through molasses. On the other hand, for most projectiles, such as gold balls, cannonballs, and even humans in free fall, the dominant drag force is quadratic, and we can neglect the linear term.

###### Reynold's Number 
The liner drag $f_{lin}$ can be related to the viscosity of the fluid through which our projectile is moving, and the quadratic term $f_{quad}$ is similarly related to the inertia (and hence density) of the fluid. Thus one can relate the ratio $\frac{f_{quad}}{f_{lin}}$ to the fundamental parameters $\eta$, the viscosity, and $\rho$, the density. The result is that the ratio $\frac{f_{quad}}{f_{lin}}$ is roughly the same order of magnitude as the dimensionless number $R = Dv \frac{\rho}{\eta}$ called the **Reynold's Number**. 

---
### Linear Air Resistance 
Let us consider first a projectile for which the quadratic drag force is negligible, so that the force of air resistance is given by $f_{lin}$. Now, we consider the diagram

![[Pasted image 20230918195701.png|center]]

where we have the force due to gravity and the drag force. We can write using Newton's Second Law, the second order ODE
$$
m \ddot{\bf{r}} = m{\bf{g}} - b \bf{v}
$$
Since neither of the forces depend on the position, but the velocity, we instead write 
$$
m\dot{\bf{v}} = m{\bf{g}}-b\bf{v},
$$
a first order ODE for $\bf{v}$. This equation of motion can be easily separated into its components 
$$
\begin{gathered}
m\dot{v_{x}} = -bv_{x} \\
m v_{y} = -mg - b v_{y}
\end{gathered}
$$
Since these two equations are completely independent and separable, we can solve both separately using [[ODE First Order Methods]]. Note that this system of ODEs would be coupled if we had the quadratic drag instead. Anyways, we solve the horizontal motion ODE to get 
$$
v_{x}(t) = v_{x_{0}}e^{-bt} = v_{x_{0}}e^{\frac{-t}{\tau}}
$$
where $\tau = \frac{m}{b}$. We then integrate from $0$ to $t$ (to automatically take care of the constant of integration) using a dummy variable to get the function for position 
$$
\int\limits_{0}^{t}v_{x}(t')dt' = x(t) - x(0).
$$
Therefore
$$
x(t) = x(0) + \int\limits_{0}^{t}v_{x_{0}}e^{\frac{-t'}{\tau}}dt' = v_{x_{0}}\tau \left(1-e^{\frac{-t}{\tau}}\right)
$$
Note that $v_{x_{0}}\tau$ is the limit of $x(t)$ as $t \rightarrow \infty$, and is sometimes denoted as $x_{\infty}$.

The vertical motion ODE is then solved using [[ODE First Order Methods]] to get 
$$
v_{y}(t) = v_{y_{0}}e^{\frac{-t}{\tau}} + \frac{mg}{b}\left(1-e^{\frac{-t}{\tau}}\right)
$$
where $\frac{mg}{b} = v_{ter}$, the terminal velocity of the projectile. Integrating this function to get the position function, we get 
$$
y(t) = \int\limits_{0}^{t}v_{y}(t') \ dt' = v_{ter}t+(v_{y_{0}}-v_{ter}) \tau\left(1-e^{\frac{-t}{\tau}}\right)
$$
The equations for $x(t)$ and $y(t)$ can now be combined together to give us the orbit of any projectile in a linear medium. 

##### Trajectory and Range in Linear Medium 
Let us now try to determine the range and trajectory with the $x(t)$ and $y(t)$ found before. Except now, we will consider $y$ to be positive when going vertically upward, therefore we reverse the sign of $v_{ter}$. The two equations of the orbit become 
$$
\begin{gathered}
x(t) = v_{x_{0}}\tau\left(1-e^{\frac{-t}{\tau}}\right) \\
y(t) = (v_{y_{0}}+v_{ter}) \tau \left(1-e^{\frac{-t}{\tau}}\right)- v_{ter}t 
\end{gathered}
$$
we can solve each equation for $t$ and then substitute our answers to get 
$$
y = \frac{v_{y_{0}}+v_{ter}}{v_{x_{0}}}x + v_{ter} \tau\ln\left(1-\frac{x}{v_{x_{0}}\tau}\right)
$$
From this equation we would expect a very linear initial trajectory that turns parabolic and then asymptotic at $x=v_{x_{0}}\tau$ as seen in the natural logarithm. 

To find the horizontal range $R$, we look at the value of $x$ when $y$ is equal to $0$. Thus, $R$ is the solution of the equation 
$$
 \frac{v_{y_{0}}+v_{ter}}{v_{x_{0}}}R + v_{ter} \tau\ln\left(1-\frac{R}{v_{x_{0}}\tau}\right)=0
$$
This is a transcendental equation that cannot be solved analytically, that is, in terms of well known elementary functions. Thus, we may use a [[Taylor Series]] to expand the natural logarithm to approximate the range to a certain degree. First, we consider the Taylor Series for the logarithm
$$
\ln(1-x) = -\left(x + \frac{x^{2}}{2} + \frac{x^{3}}{3}+\ldots\right)
$$
We use this term to the third degree (provided at $\tau$ is large enough to make the other terms negligible) and substitute it to get 
$$
 \frac{v_{y_{0}}+v_{ter}}{v_{x_{0}}}R - v_{ter} \tau\left(\frac{R}{v_{x_{0}}\tau} + \frac{1}{2}\left(\frac{R}{v_{x_{0}}\tau}\right)^{2} + \frac{1}{3}\left(\frac{R}{v_{x_{0}}\tau}\right)^{3} \right)=0
$$
This equation can be quickly tidied up. First, the second term in the bracket cancels out the first term in the second. Next, every term contains a factor of $R$. This implies that there is the trivial solution $R=0$. Since we are not interesting in this solution, we assume $R \neq 0$ and divide out by $R$ to get 
$$
R = \frac{2 v_{x_{0}}v_{y_{0}}}{g} - \frac{2}{3 v_{x_{0}}\tau}R^{2}
$$
where $\frac{v_{ter}}{\tau}$ was replaced with $g$. The second term on the right is very small, since the numerator $R$ is certainly no more than $R_{vac}$ (the scenario for being in a vacuum) and we are assuming that $\tau$ in the denominator is very large. Therefore, as a first approximation we get 
$$
R \approx \frac{2v_{x_{0}}v_{y_{0}}}{g} = R_{vac}
$$
This is just what we expected: for low air resistance, the range is close to the vacuum scenario. However, we can get a better approximation with our quadratic equation we derived before. Thus, let us approximate that $R \approx R_{vac}$ and use a correction term from the quadratic to get 
$$
R \approx R_{vac}- \frac{2}{3 v_{x_{0}}\tau}(R_{vac})^{2} = R_{vac}\left(1- \frac{4}{3} \frac{v_{y_{0}}}{v_{ter}}\right)
$$
From this we can see how the correction of the air resistance depends on the ratio $\frac{v_{y_{0}}}{v_{ter}}$. If this ratio is $<<1$, we can assume that the air resistance is very small. If it is $1$ or more, air resistance is almost certainly important and our approximation is certainly no good anymore.

---
### Quadratic Air Resistance 
We now step forward to tackle the equations with quadratic air resistance in the form 
$$
m\dot{\bf{v}} = m{\bf{g}}+\bf{f}
$$
where ${\bf{f}}=-cv^{2}\hat{\bf{v}}$. 

Let us consider the scenario where the drag is separated completely in the $x$ and $y$ directions such that there is no interaction between the two (not the case when considering motion in the $xy$ plane). We begin once again by separating this equation into a vertical and horizontal equation of motion. We get the two equations 
$$
\begin{gathered}
m \frac{dv_{x}}{dt} = -cv_{x}^{2} \\
m \frac{dv_{y}}{dt} = mg - cv_{y}^{2}
\end{gathered}
$$
Both of these can be solved with [[ODE First Order Methods]], most notably separation of variables or by integration factor. 

Now, if we were to consider motion in the $xy$ plane, we get a nonlinear equation 
$$
m\ddot{\bf{r}}=m{\bf{g}} - cv^{2} \hat{\bf{v}}
$$
which is the coupled equation 
$$
\begin{gathered}
m\dot{v_{x}} = -c\sqrt{v_{x}^{2}+v_{y}^{2}}v_{x} \\
m\dot{v_{y}} = -mg-c\sqrt{v_{x}^{2}+v_{y}^{2}}v_{y}

\end{gathered}
$$
Note that these look close to the Eikonal Equation in [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]. Due to the coupled nonlinearity of these equations, there are currently no analytic solutions to solve this equation of motion exactly, and one must employ methods of numerical analysis or approximation.

We can see that this motion approaches a vertical asymptote as before. We can prove this by looking at the equation of motion and seeing that as a projectile moves downward, it will accelerate until reaching a terminal velocity $-v_{ter}$ as $t \rightarrow\infty$. At the same time $v_{x}$ continues to decrease and approach zero. Thus the square root in the coupled nonlinear differential equations approaches $v_{ter}$. In particular, when $t$ is large, we can approximate that 
$$
\dot{v_{x}} \approx \frac{-cv_{ter}}{m}v_{x} = -kv_{x}
$$
The solution of course is an exponential function, and we see that $v_{x}$ rapidly approaches zero (exponentially) as $t$ increases. This guarantees that $x$, which is the integral of $v_{x}$,
$$
x(t) = \int\limits_{0}^{t}v_{x}(t') \ dt'
$$
approaches a finite limit as $t \rightarrow \infty$ and the trajectory as a finite vertical asymptote. 

---
### Motion of a Charge in a Uniform Magnetic Field 
Another application of Newton's Laws is the motion of a charged particle in a magnetic field. I shall consider here a particle of charge $q$ (assuming the charge is positive), moving in a uniform magnetic field $\bf{B}$ that points in the $z$ firection as shown in the figure below. The net force on the particle is just the magnetic force (Lorentz Force)
$$
{\bf{F}} = q{\bf{v}} \times \bf{B}
$$

![[Pasted image 20230918215325.png|center]]

so the equation of motion can be written as 
$$
m\dot{\bf{v}} = q {\bf{v}} \times \bf{B}
$$
Now, we consider the components of $\bf{v}$ and $\bf{B}$, which are 
$$
{\bf{v}} = (v_{x},v_{y},v_{z})
$$
and 
$$
{\bf{B}} = (0,0,B),
$$
from which we can read off the components of ${\bf{v}}\times \bf{B}$: 
$$
{\bf{v}}\times {\bf{B}} = (v_{y}B,-v_{x}B,0)
$$
Thus, the first three components of our equation of motion are 
$$
\begin{gathered}
m\dot{v_{x}} = qBv_{y} \\
m\dot{v_{y}}=-qBv_{x} \\
m\dot{v_{x}}=0

\end{gathered}
$$
The last of these says simply that $v_{z}$ is constant, a result we anticipate since the magnetic force is always perpendicular to $\bf{B}$. Now, since the first two ODEs are coupled, let us consider a devious trick to solve them. We shall consider their solution as a two-dimensional vector $(v_{x},v_{y})$ which is just the projection of $\bf{v}$ onto the $xy$ plane and can be called the _transverse velocity_. 

To first simplify our ODEs, we make the substitution $\omega = \frac{qB}{m}$ which is known as the the **cyclotron frequency**. With this notation, our coupled equations become 
$$
\begin{gathered}
\dot{v_{x}} = \omega v_{y}\\
\dot{v_{y}} = - \omega v_{x}
\end{gathered}
$$
These two coupled differential equations can be solved in a host of different ways. Let us map our equations to the complex plan for a quite intricate solution. We define the complex number 
$$
\eta = v_{x}+iv_{y}
$$
Now, we can combine our coupled ODEs with this collective variable via 
$$
\dot{\eta}=\dot{v_{x}}+i\dot{v_{y}} = \omega v_{y}-i \omega v_{x} = -i \omega (v_{x}+iv_{y})
$$
or 
$$
\dot{\eta} = -i \omega \eta
$$
This ODE obviously has the solution 
$$
\eta = Ae^{-i \omega t}
$$

![[Pasted image 20230918221829.png|center]]

We see that this solution is simply a trajectory in the complex plane that goes counterclockwise about a circle of some radius $A$. Now, let us bring all of this together to interpret our solution.

We already know that $v_{z}$, the component of velocity along $\bf{B}$, is constant. The components $(v_{x},v_{y})$ traverse to $\bf{B}$ are represented by the complex number $\eta = v_{x}+iv_{y}$, and we have seen that this implies that $\eta$ has the time dependence $\eta = A e^{-i \omega t}$ , moving uniformly around the circle in the figure below. Now, the arrow shown in this figure, is a representation of the transverse velocity, which is turning clockwise with constant angular velocity $\omega = \frac{qB}{m}$ and with constant magnitude. Because $v_{z}$ is constant, this suggests that the particle undergoes a spiral or helical motion. To verify this we integrate to find the function of position.

![[Pasted image 20230918223957.png|center]]

A constant $v_{z}$ implies that 
$$
z(t) = z_{0}+v_{z_{0}}t
$$
The motion of $x$ and $y$ is most easily found by introducing another complex number 
$$
\xi = x+iy
$$
Now, we integrate $\eta$ with respect to time to get 
$$
\xi = \int\limits \eta \ dt = \frac{iA}{\omega}e^{-i \omega t} + \text{const.}
$$
Let us call this constant (which is a complex number) $z$ and substitute $\frac{iA}{\omega}=C$ to get 
$$
\xi = Ce^{-i \omega t} + z
$$
Now, we see that this is simply just the formula for a circle on the complex plane centered at $z$. Thus, our particle is moving in a uniform circular motion in the $xy$ plane centered at $z$. And $C$ is the complex number representing the distance from the initial point $x_{0}+iy_{0}$ to the center $z$ as $\xi(0) - z = C$. Since the angular frequency of this orbit is known, $\omega=\frac{qB}{m}$, we find that the radius of the orbit is (considering that we just found the trajectory is uniform circular motion): 
$$
r = \frac{v}{\omega} = \frac{mv}{qB} = \frac{p}{qB}
$$
