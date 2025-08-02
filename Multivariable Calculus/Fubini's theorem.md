---
tags: theorem, Math, Multivariable, Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Fubini's Theorem_
Applications: _Changing order of Integration and Summation_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
One may switch the order of integration if the double integral yields a finite answer when the integrand is replaced by its absolute value: 
$$
\int\limits \int_{X\times Y} f(x,y) \ d(x,y) = \int_{X}\left(\int_{Y}f(x,y) \ dy\right)\ dx = \int_{Y}\left(\int\limits_{X}f(x,y) \ dx\right) \ dy
$$
if 
$$
\int\limits \int_{X \times Y} |f(x,y)| \ d(x,y) < +\infty
$$
Tonelli made the improvement that the condition from _Tonelli's Theorem_:
$$
\int\limits \int_{X \times Y} |f(x,y)| \ d(x,y) =  \int_{X}\left(\int_{Y}|f(x,y)| \ dy\right)\ dx = \int_{Y}\left(\int_{X}|f(x,y)| \ dx\right) \ dy
$$

**Remark.**  As long as one of these absolute value integrals exists, so do the others. (This is because by Tonelli these conditions are all equation). Thus if any are $< +\infty$, then Fubini's theorem holds. 
