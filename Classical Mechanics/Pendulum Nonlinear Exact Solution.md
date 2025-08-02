---
tags: Physics, CM, ODE, pendulum, nonlinear, exact, harmonic, motion
dg-publish: true
mathLink: 
---
Subject: _CM_
Main\_Topic: _Nonlinear Exact Solution for a Pendelum_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Newton's Laws of Motion]]_
Cont.\_ of: _None_ 
_
_

If we have the nonlinear differential equation 
$$
\ddot{\theta} + \frac{g}{l}\sin \theta = 0
$$
Let us first multiply both sides of this equation by a nonzero velocity:
$$
\ddot{\theta} \cdot \dot{\theta} + \frac{g}{l}\sin \theta \cdot \dot{\theta} = 0
$$
Note that $\theta$ is dependent on time, thus if we were to take the time partial derivative $\partial_{t} \dot{\theta}^{2}=2 \ddot{\theta}\dot{\theta}$, we can see that we can rewrite $\ddot{\theta}\dot{\theta}$ as simply $\frac{\partial_{t}\dot{\theta}^{2}}{2}$. We do something similar for the other term in the DE and now we write 
$$
\partial_{t} \frac{\dot{\theta^{2}}}{2} + \partial_{t}\left(\frac{-g}{l}\cos \theta\right) = 0
$$
which is 
$$
\partial_{t}\left[\frac{\dot{\theta}^{2}}{2} - \frac{g}{l}\cos \theta\right] = 0
$$
Now, we know that the partial time derivative must be acting on a constant such that 
$$
\frac{\dot{\theta}^{2}}{2} - \frac{g}{l} \cos \theta = C
$$
which can be simplified to 
$$
\dot{\theta}^{2} - k \cos \theta = C
$$
where $k=\frac{2g}{l}$. Now, let us consider that we have the initial conditions that $\theta(0)=\theta_{0}$ and $\dot{\theta(0)}=0$, this is because we would expect the angular velocity of the pendulum to be $0$ before we let go and it swings. We can once again see that 
$$
-k\cos(\theta_{0}) = C
$$
such that 
$$
\dot{\theta}^{2} - k\cos \theta = -k \cos (\theta_{0})
$$
which resolves to 
$$
\dot{\theta}^{2} = k[\cos \theta - \cos  \theta_{0}]
$$
Using the double angle formula from [[trig_cheat_sheet.pdf]], we get 
$$
\dot{\theta}^{2} = k\left[1-2\sin ^{2}\left(\frac{\theta}{2}\right)-1+2\sin^{2}\left(\frac{\theta_{0}}{2}\right)\right]
$$
$$
\dot{\theta}^{2} = 2k\left[\sin ^{2}\left(\frac{\theta}{2}\right) -\sin^{2}\left(\frac{\theta_{0}}{2}\right) \right]
$$
Now, let us redefine our constants to get 
$$
\dot{\theta}^{2} = r\left[k^{2}-\sin^{2}\left(\frac{\theta}{2}\right)\right]
$$
Now, let us take the square root on both sides. We will just pay attention to the positive branch since the negative branch will just having $-\theta$ in our solution.
$$
\dot{\theta} = \sqrt{r} \sqrt{k^{2}-\sin^{2}\left(\frac{\theta}{2}\right)}
$$
We assume that the term on the right is nonzero such that we can solve this separable differential equation
$$
\frac{\dot{\theta}}{\sqrt{k^{2}-\sin^{2} (\frac{\theta}{2}})}  = \sqrt{r}
$$
we integrate with respect to time on both sides 
$$
\int\limits \frac{\dot{\theta}}{\left(k^{2}-\sin^{2} \left(\frac{\theta}{2}\right)\right)} = \sqrt{r}\int\limits dt
$$
We would like to integrate with respect to the initial condition in order to solve this as an initial value problem. Thus we will integrate from $0$ to $\theta_{0}$. But why? 

We must consider the physical point of view for this to make sense. Well, if we consider the scenario where we start at an angle $\theta_{0}$ and then pendulum goes to $\theta=0$, which is perpendicular to the Earth. This will be $\frac{1}{4}$ of the period time $T$ since this represents only $\frac{1}{4}$ of an entire swing across and pendulum and back to the original position which we let the pendulum go at. Now, with this in mind, we are integrating over a quarter of the period time.
$$
\int\limits_{0}^{\theta_{0}} \frac{\dot{\theta}}{\left(k^{2}-\sin^{2} \left(\frac{\theta}{2}\right)\right)} = \sqrt{r}\int\limits_{0}^{\theta_{0}} dt
$$
Now we let $\sin\left(\frac{\theta}{2}\right)=k\sin(\eta)$ since we would like something where we can factor the $k$ out of the square root in the denominator. If we take the derivative on both sides we get 
$$
\cos \left(\frac{\theta}{2}\right) \frac{1}{2} d \theta = k \cos (\eta) d \eta
$$
Now, if we use the Pythagorean theorem we can get 
$$
d \theta =\frac{2k \cos(\eta)}{\left(\sqrt{1-\sin^{2}\left(\frac{\theta}{2}\right)}\right)} d \eta
$$
We then plug in $\theta=0$ and $\theta=\theta_{0}$ to find our bounds while working on the principle branch of sine. We get from our integral:
$$
T \frac{\sqrt{r}}{4} = \int\limits_{0}^{\frac{\pi}{2}} \frac{d \eta}{\sqrt{k^{2}-k^{2}\sin^{2}(\eta})} = \int\limits_{0}^{\frac{\pi}{2}} \frac{1}{|k|\sqrt{\cos(\eta)}} \cdot \frac{2k \cos(\eta)}{\left(\sqrt{1-\sin^{2}\left(\frac{\theta}{2}\right)}\right)} d \eta
$$
**Remark.**  Because we are working on the principle branch, and using how we are defining the interval of angles we are working on, we can say that $|k|=k$ since $\sin\left(\frac{\theta_{0}}{2}\right)>0$ on our interval. 

We can now simplify and get 
$$
T = \frac{8}{\sqrt{r}} \int\limits_{0}^{\frac{\pi}{2}} \frac{d \eta}{\sqrt{1-k^{2}\sin^{2}(\eta)}}
$$
Thus, our final solution is 
$$
T = 4\sqrt{\frac{l}{g}} K(k)
$$
where $K$ is the elliptic integral of the first kind!
