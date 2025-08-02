---
tags: Math, graphing, Arcsin, Inverse_Functions, Trig
mathLink: $\arcsin(\sin(x))$
dg-publish: true
mathLink: 
---
Subject: _Algebra_
Main\_Topic: _Trig Functions_
Applications: _Graphing, Trig Functions_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

The graph of $\arcsin\sin x$ is not what you would expect. But we must remember one HUGE thing:
```ad-Remember
$f^{-1}(f(x))=x$ ONLY on one-one (bijective) mappings. 
```

If we take this into account, we see that for $x \in [\frac{-\pi}{2},\frac{\pi}{2}]$ (which is a bijective interval for $\arcsin$):
$$
\arcsin(\sin x) =x 
$$
**Remark.** This interval is what the inverse is defined on, so ALL intervals must be mapped back to this bijective one.

If we wanted to see what the function would look like outside of this one-one mapping, we have to use the periodicity of the $\sin$ function. Because any angle can be mapped back into this interval, we shift the intervals of $x$ back to $[\frac{-\pi}{2},\frac{\pi}{2}]$, then that angle is what we get from the $\arcsin$. It's easier to just see, so let us look at the interval $[\frac{\pi}{2},\frac{3\pi}{2}]$:
$$
\begin{gathered}
\frac{\pi}{2}\leq x \leq \frac{3\pi}{2} \\
\frac{-3\pi}{2}\leq -x \leq \frac{-\pi}{2} \\
\frac{-\pi}{2}\leq \pi-x \leq \frac{\pi}{2}
\end{gathered}
$$
Thus, for the interval $x \in [\frac{\pi}{2},\frac{3\pi}{2}]$, 
$$
\arcsin(\sin x) = \pi -x.
$$
This pattern continues for all $\frac{\pi}{2}$ intervals. 
$$

$$