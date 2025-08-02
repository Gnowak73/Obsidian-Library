---
tags: 
dg-publish: true
mathLink: 
---
Subject: _None_
Main\_Topic: _None_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

What happens to a neutral atom when it is placed in an electric field $\mathbf{E}$? Well, we see that the positive and negative charges that make up the atom (the electrons and protons), interact with this field. The nucleus is pushed in the direction of the field, while the electron is pushed in the opposite direction. In principle, if the field is large enough, we can completely ionize the atom. With less extreme fields, however, equilibrium is established. 

The two opposing forces (the electric field and the mutual attraction of the atom) balance, polarizing the atom with a dipole moment $\mathbf{p}$ in the same direction as $\mathbf{E}$. Typically, this induced dipole is approximately proportional to the field (as long as the latter is not too strong):
$$
\mathbf{p} = \alpha \mathbf{E}
$$
The constant of proportionality $\alpha$ is called the **atomic polarization**. Its value depends on the detailed structure of the atom in question. 

For molecules this situation is not as simple, because frequently they polarize more readily in some directions than others. When the field is at the some angle to the axis, you must resolve it into parallel and perpendicular components (for a symmetric molecule that can be lined up appropriately), and multiply each by the pertinent polarizability: 
$$
\mathbf{p} = \alpha_{\perp} \mathbf{E}_{\perp} + \alpha_{\parallel} \mathbf{E}_{\parallel}
$$
In that case the induced dipole moment may not even be in the same _direction_ as $E$. For a completely asymmetric molecule, you actually get the system of equations between $\mathbf{E}$ and $\mathbf{p}$:
$$
p_{x} = \alpha_{xx}E_{x} + \alpha_{xy}E_{y} +\alpha_{xz}E_{z}
$$
$$
p_{y} = \alpha_{yx}E_{x} + \alpha_{yy}E_{y} +\alpha_{yz}E_{z}
$$
$$
p_{z} = \alpha_{zx}E_{x} + \alpha_{zy}E_{y} +\alpha_{zz}E_{z}
$$
The set of nine constants $\alpha_{ij}$ constitute the **polarizability tensor** for the molecule. Their values depend on the orientation of the axes you use, thought it is always possible to choose "principle" axes such that all the off diagonal terms vanish. 

#### Alignment of Polar Molecules
The neutral atom talked about before had no dipole moment to start with; $\mathbf{p}$ was induced by the applied field. Some molecules have built-in, permanent dipole moments. Now, we must account for what happens when these molecules are placed into electric fields. 

If the field is uniform, the force on the positive end $\mathbf{F}_{+}=q \mathbf{E}$, exactly cancels the force on the negative $\mathbf{F}_{-} = -q \mathbf{E}$. However, there will be a torque 
$$
\mathbf{N} = (\mathbf{r}_{+} \times \mathbf{F}_{+}) + (\mathbf{r}_{-} \times \mathbf{F}_{-})
$$
$$
= \frac{\mathbf{d}}{2} \times q \mathbf{E} + \frac{-\mathbf{d}}{2} \times -q \mathbf{E} = q \mathbf{d} \times E
$$
Thus, a dipole $\mathbf{p} = q \mathbf{d}$ in a uniform field $\mathbf{E}$ experiences a torque
$$
\mathbf{N} = \mathbf{p} \times \mathbf{E}
$$
Notice that $\mathbf{N}$ is in such a direction as to line $\mathbf{p}$ up _parallel_ to $\mathbf{E}$, so a polar molecule that is free to rotate will swing around until it points in the direction of the applied field. If the field is _non_ uniform, so that $\mathbf{F}_{+}$ does not exactly balance $\mathbf{F}_{-}$, then there will be a net force on the dipole in addition to the torque. This is not usually the case for dielectrics since it requires a significance variation of $\mathbf{E}$ in the space of one molecule. Nevertheless, the formula for the force on a dipole in a nonuniform field is of some interest: 
$$
\mathbf{F} = \mathbf{F}_{+} + \mathbf{F}_{-} = q (\mathbf{E}_{+} - E_{-}) = q \Delta \mathbf{E}
$$
where $\Delta \mathbf{E}$ represents the difference between the field at the plus end and the minus end. Assuming the dipole is very short, we may use an approximate for $E$ to be 
$$
\Delta E= \nabla E \cdot d = (\mathbf{d} \cdot \nabla) \mathbf{E}
$$
and thus we may write 
$$
\mathbf{F} = (\mathbf{p} \cdot \nabla) \mathbf{E}
$$
For a "perfect" dipole of infinitesimal length. The formula for the torque about the center of the dipole is still the same, however. The torque about any point would be $\mathbf{N}=(\mathbf{p}\times \mathbf{E}) + (\mathbf{r}\times \mathbf{F})$. 

#### Polarization
Now, after discussing the polarization of individual atoms and molecules, we want to answer the original question: what happens to a piece of dielectric material when it is placed in an electric field? If the substance consists of neutral atoms (or nonpolar molecules), the field will induce in each a tiny dipole moment, pointing in the same direction as the field. 

If the material is made of dipoles each permanent dipole will experience a torque, tending to line it up along the field direction. (Random thermal motions compete with this process, so the alignment is never complete, especially at higher temperatures). 

Note that these two mechanisms produce the same result: a lot of little dipoles pointing along the direction of the field, and the material becomes **polarized**. A convenient measure of this effect is 
$$
\mathbf{P} = \text{dipole moment per unit volume}
$$
which is called the **polarization**. Now, the two mechanisms stated are not as clear cut as presented. Even in polar molecules there will be some polarization by displacement (thought it generally is a lot easier to rotate a molecule than to stretch it, so the second mechanisms dominates). But lets forget for a moment about the cause of the polarization and look at what a polarized material itself produces. 

#### The Field of a Polarized Object
Suppose that we have a piece of polarized material. The dipole moment per unit volume $\mathbf{P}$ is given. Question: what is the field produced by this object? Well, we know what the field of an individual dipole looks like, so why not chop the material up into infinitesimal dipoles. For a single dipole $\mathbf{p}$:
$$
V(\mathbf{r}) = \frac{1}{4\pi \epsilon_{0}} \frac{\mathbf{p} \cdot \hat{\mathbf{r_{r}}}}{r_{r}^{2}}
$$
where $\mathbf{r}_{r}$ is the vector from the dipole to the point at which we are evaluating the potential. In the present context, we have a dipole moment $\mathbf{p} = \mathbf{P}d \tau'$ in each volume element $d \tau'$, so the total potential is 
$$
V(\mathbf{r}) = \frac{1}{4\pi \epsilon_{0}} \int_{V}  \frac{\mathbf{P}(\mathbf{r}') \cdot \hat{\mathbf{r}_{r}}}{r_{r}^{2}} d \tau'
$$
That does it, in principle. But let us note that 
$$
\nabla'\left(\frac{1}{r_{r}}\right) = \hat{\frac{\mathbf{r}_{r}}{r_{r}^{2}}}
$$
where the differentiation is with respect to the _source coordinates_ $(\mathbf{r}')$, we have 
$$
V = \frac{1}{4 \pi \epsilon_{0}} \int_{V} \mathbf{P} \cdot\nabla'\left(\frac{1}{r_{r}}\right) d \tau'
$$
Integrating by parts, using the 5th product rule from [[EM Vector Analysis]], gives 
$$
V = \frac{1}{4 \pi \epsilon_{0}}\left[\int_{V} \nabla' \cdot \left(\frac{\mathbf{P}}{r_{r}}\right)d \tau' - \int_{V} \frac{1}{r_{r}}(\nabla' \cdot \mathbf{P}) d \tau' \right]
$$ or, invoking the divergence theorem,
$$
V = \frac{1}{4\pi \epsilon_{0}} \oint_{S} \frac{1}{r_{r}} \mathbf{P} \cdot d \mathbf{a}' - \frac{1}{4\pi \epsilon_{0}}\int_{V} \frac{1}{r_{r}}(\nabla' \cdot \mathbf{P}) d \tau'
$$
The first term looks like the potential of a surface charge, 
$$
\sigma_{b} := \mathbf{P} \cdot\hat{\mathbf{n}}
$$
where $\hat{\mathbf{n}}$ is the normal unit vector, while the second term looks like the potential of a volume charge, 
$$
\rho_{b} := -\nabla \cdot \mathbf{P}
$$
With these definitions, we then write the integrals as 
$$
V(\mathbf{r}) = \frac{1}{4\pi \epsilon_{0}} \oint_{S} \frac{\sigma_{b}}{r_{r}} da' + \frac{1}{4\pi \epsilon_{0}} \int_{V} \frac{\rho_{b}}{r_{r}} d \tau'
$$
This means that the potential (and hence also the field) of a polarized object is the same as that produced by a volume charge density $\rho_{b}=-\nabla \cdot \mathbf{P}$ plus a surface charge density $\sigma_{b} = \mathbf{P} \cdot \hat{\mathbf{n}}$. Instead of integrating the contributions of all the infinitesimal dipoles, we could first find those **bound charges**, and then calculate the fields _they_ product, in the same way we calculate the field of any other volume and surface charges (for example, Gauss's law). 

#### Physical Interpretation of Bound Charges
Now, we found that the field of a polarized object is identical to the field that would be produced by a certain distribution of "bound charges," $\sigma_{b}$ and $\rho_{b}$. But this conclusion emerged in the course of abstract manipulations integrals and not physical intuition. Actually, we see that $\rho_{b}$ and $\sigma_{b}$ represent perfectly genuine accumulations of charge. 

The basic idea is very simple: suppose we have a long string of dipoles. Along the line, the head of one effectively cancels the tail of its neighbor, but at the ends there are two charges left over: plus at the right-hand end and minus at the left. It is as if we had peeled off an electron at one end and carried it all the way down to the other end, though in fact no single electron made the whole trip (a lot of tiny displacements add up to one large one). We call the net charge at the end **bound** charge to remind ourselves that it cannot be removed; in a dielectric every electron is attached to a specific atom or molecule. But apart from that, bound charge is no different from any other kind. 

To calculate the amount of bound charge resulting from a given polarization, examine a "tube" of dielectric parallel to $\mathbf{P}$. The dipole moment of the tiny chunk is $P(Ad)$, where $A$ is the cross-sectional area and $d$ is the length of the chunk. In terms of the charge at the end, this same dipole moment can be written as $qd$. The bound charge that piles up at the right-hand end of the tube is therefore 
$$
q = PA 
$$
If the ends have been sliced off perpendicularly, the surface charge density is 
$$
\sigma_{b} = \frac{q}{A} = P
$$
For an oblique cut, the charge is still the same, but $A =A_{end} \cos \theta$, so 
$$
\sigma_{b} = \frac{q}{A_{end}} = \mathbf{P} \cdot \hat{\mathbf{n}}
$$
The effect of polarization, then, is to paint a bound charge $\sigma_{b}=\mathbf{P}\cdot \hat{\mathbf{n}}$ over the surface of the material. This is exactly what we found by more rigorous means. But now we know where the bound charge comes from. 

If the polarization is nonuniform, we get accumulations of bound charge within the material, as well as one the surface. A glance at the figure 

![[Pasted image 20241027222320.png|center|300]]

suggests that a diverging $\mathbf{P}$ results in a pileup of negative charge. Indeed, the net bound charge $\int \rho_{b} d \tau$ in a given volume is equal and opposite to the amount that has been pushed out through the surface. The latter (by the same reasoning that we used prior) is $\mathbf{P} \cdot \hat{\mathbf{n}}$ per unit area, so 
$$
\int\limits_{V} \rho_{b}d \tau = -\oint_{S}\mathbf{P}\cdot d \mathbf{a} = -\int_{V} (\nabla \cdot \mathbf{P}) d \tau
$$
Since this is true for _any_ volume, we have 
$$
\rho_{b}= -\nabla \cdot \mathbf{P}
$$
confirming, again, the more rigorous conclusion we made prior. 

#### The Electric Displacement 
Before, we found that the effect of polarization is to produce accumulations of bound charge, $\rho_{b} = -\nabla \cdot \mathbf{P}$ within the dielectric and $\sigma_{b}=\mathbf{P}\cdot\hat{\mathbf{n}}$ on the surface. The field due to polarization of the medium is just the field of this bound charge. We are now ready to put it all together: the field attributable to bound charge plus the field due to everything else (which, for want of a better term, we call **free charge***, $\rho_{f}$). the free charge might consist of electrons on a conductor or ions embedded in the dielectric material or whatsoever; any charge, in other words, that is **not** associated with $\mathbf{P}$. Within the dielectric, the total charge density can be written 
$$
\rho = \rho_{b}+\rho_{f},
$$
and Gauss's law reads 
$$
\epsilon_{0}\nabla \cdot \mathbf{E} = \rho = \rho_{b} + \rho_{f} = -\nabla \cdot \mathbf{P} + \rho_{f},
$$
where $\mathbf{E}$ is now the **total field**, not just the part generated by polarization. It is convenient to combine the two divergence terms: 
$$
 \nabla \cdot (\epsilon_{0}\mathbf{E} + \mathbf{P}) = \rho_{f}
 $$
 The expression in parenthesis, designated by the letter $\mathbf{D}$ 
 $$
 D := \epsilon_{0} \mathbf{E} + \mathbf{P}
$$
is known as the **electric displacement**. In terms of $\mathbf{D}$, Gauss's law reads
$$
\nabla \cdot \mathbf{D} = \rho_{f}
$$
or in integral form
$$
\oint \mathbf{D} \cdot d \mathbf{a} = Q_{f_{encl}}
$$
where $Q_{f_{enc}}$ denotes the total **Free** charge enclosed in the volume. This expression is particularly useful in the context of dielectrics, because it makes reference only to free charges, and free charge is the stuff we control. Bound charges comes along for the ride. 

Now, it may appear that the surface bound charge was left out when deriving Gauss's law in this form, which is true. However, we cannot apply Gauss's law precisely at the surface of a dielectric, for here $\rho_{b}$ blows up, taking the divergence of $\mathbf{E}$ with it. But everywhere else the logic is sound, and if fact if we picture the edge of the dielectric as having some finite thickness, within which the polarization tapers off to zero, then there is no surface bound charge; $\rho_{b}$ varies rapidly but smoothly within this "skin," and Gauss's law can be safely applied _everywhere_. At any rate, the integral form is free from this "defect." 

#### A Deceptive Parallel  
Note that the equation we derived ($\nabla \cdot \mathbf{D} = \rho_{f}$), looks just like Gauss's law, only the total charge density $\rho$ is replaced by the _free_ charge density $\rho_{f}$, and $\mathbf{D}$ is substituted for $\epsilon_{0}\mathbf{E}$. For this reason, you may be tempted to conclude that $\mathbf{D}$ is "just lie $\mathbf{E}$", except that its source is $\rho_{f}$ instead of $\rho$. "To solve problems involving dielectrics, you just forget all about the bound charge$-$calculate the field as normally would, but only call the answer $\mathbf{D}$ instead of $\mathbf{E}$." 

This reasoning is seductive, but the conclusion is false; in particular, there is no "Coulomb's law" for $\mathbf{D}$. The parallel between $\mathbf{E}$ and $\mathbf{D}$ is more subtle than that. 

For the divergence alone is insufficient to determine a vector field; you need to know the curl as well. One tends to forget this in the case of electrostatics because the curl of $\mathbf{E}$ is always zero. But the curl of $\mathbf{D}$ is **not** always zero: 
$$
\nabla \times D = \epsilon_{0}(\nabla \times \mathbf{E}) + (\nabla \times \mathbf{P}) = \nabla \times \mathbf{P},
$$
and there is no reason, in general, to suppose that the curl of $\mathbf{P}$ vanishes. Sometimes it does, but more often it does not. Thus, there is no "potential" for $\mathbf{D}$. 

**Advice:**  When you are asked to compute the electric displacement, first look for symmetry. If the problem exhibits spherical, cylindrical, or plane symmetry, then you can get $\mathbf{D}$ directly from usual Gauss's law methods. (Evidently in such cases $\nabla \times \mathbf{P}$ is zero, but since symmetry alone dictates the answer, you're not really obliged to worry about the curl.) If the requisite symmetry is absent, you must think of another approach, and, in particular, you must **not** assume that $\mathbf{D}$ is determined exclusively by the free charge. 

#### Boundary Conditions
The electrostatic boundary conditions can be recast in terms of $\mathbf{D}$. We may write 
$$
{D}^{\perp}_{above} - {D}^{\perp}_{below} = \sigma_{f}
$$
while the discontinuity in parallel components may be written as 
$$
\mathbf{D}^{\parallel}_{above} - \mathbf{D}^{\parallel}_{below} = \mathbf{P}^{\parallel}_{above} - \mathbf{P}^{\parallel}_{below}
$$
In the presence of dielectrics, these are sometimes more useful than the corresponding boundary conditions on $\mathbf{E}$:
$$
E^{\perp}_{above} - E^{\perp}_{below} = \frac{\sigma}{\epsilon_{0}}
$$
and 
$$
\mathbf{E}^{\parallel}_{above} - \mathbf{E}^{\parallel}_{below} = 0
$$

#### Linear Dielectrics 
Before, we did not commit ourselves as to the cause of $\mathbf{P}$, but only with the effects of polarization. From the qualitative discussion prior, though, we know that the polarization of a dielectric ordinarily results from an applied electric field, which lines up the atomic or molecular dipoles. For many substances, in fact, the polarization is **proportional** to the field, provided $\mathbf{E}$ is not too strong: 
$$
\mathbf{P} = \epsilon_{0}\chi_{e} \mathbf{E}
$$
the constant or proportionality $\chi_{e}$, is called the **electric susceptibility** of the medium. The value of $\chi_{e}$ depends on the microscopic structure of the substance in question (and also on external conditions such as temperature. I shall call material that obey this equation **linear dielectrics**. 

Note that $\mathbf{E}$ in the equation is the total field; it may be due in part to free charges and in part to the polarization itself. If, for instance, we put a piece of dielectric into an external field $\mathbf{E}_{0}$, we cannot compute $\mathbf{P}$ directly from this equation; the external field will polarize the material, and this polarization will produce its own field, which then contributes to the total field, and this in turn modifies the polarization, which... breaking out of this infinite regress is not always easy. You'll see some examples in a moment. The simplest approach is to begin with the _displacement_, at least in those cases where $\mathbf{D}$ can be deduced directly from the free charge distribution. 

In linear media we have 
$$
\mathbf{D} = \epsilon_{0}\mathbf{E} + \mathbf{P} = \epsilon_{0} \mathbf{E} + \epsilon_{0} \chi_{e} \mathbf{E} = \epsilon_{0}(1+ \chi_{e})\mathbf{E},
$$
so $\mathbf{D}$ is also proportional to $\mathbf{E}$:
$$
\mathbf{D} = \epsilon \mathbf{E}
$$
where
$$
\epsilon := \epsilon_{0}(1 + \chi_{e})
$$
This new constant $\epsilon$ is called the **permittivity** of the material. (In a vacuum, where there is no matter to polarize, the susceptibility is zero, and the permittivity is $\epsilon_{0}$. That's why $\epsilon_{0}$ is called the **permittivity of free space**. I dislike the term, since it suggests that the vacuum is just a special kind of linear dielectric, which it is not). If you remove a factor of $\epsilon_{0}$, the remaining dimensionless quantity
$$
\kappa = 1 + \chi_{e} = \frac{\epsilon}{\epsilon_{0}}
$$
is called the **relative permittivity**, or the **dielectric constant**, of the material. 

You might suppose that linear dielectrics escape the defect in the parallel between $\mathbf{E}$ and $\mathbf{D}$. Since $\mathbf{P}$ and $\mathbf{D}$ are now proportional to $\mathbf{E}$, does it not follow that their curls must vanish? Unfortunately, it does not, for the line integral of $\mathbf{P}$ around a closed path that _straddles the boundary between one type of material and another_ need not be 0. The reason is that the proportionality factor $\epsilon_{0}\chi_{e}$ is different on the two sides. 

Of course, if the space is entirely filled with a homogeneous linear dielectric, then this objection is void; in this rather special circumstance, 
$$
\nabla \cdot \mathbf{D} = \rho_{f}, \quad \nabla \times \mathbf{D} = 0
$$
so $\mathbf{D}$ can be found from the free charge just as though the dielectric were not there: 
$$
\mathbf{D} = \epsilon_{0}\mathbf{E}_{vac}
$$
where $\mathbf{E}_{vac}$ is the field the same free charge distribution would produce in the absence of any dielectric. Thus, 
$$
\mathbf{E} = \frac{1}{\epsilon}\mathbf{D} = \frac{1}{\kappa} \mathbf{E}_{vac}
$$
For objects, like crystals, which are generally easier to polarize in some directions rather than others, we replace our polarization equation with the system 
$$
P_{x} = \epsilon_{0}(\chi_{e_{xx}}E_{x} + \chi_{e_{xy}}E_{y} + \chi_{e_{xz}}E_{z})
$$
$$
P_{y} = \epsilon_{0}(\chi_{e_{yx}}E_{x} + \chi_{e_{yy}}E_{y} + \chi_{e_{yz}}E_{z})
$$
$$
P_{z} = \epsilon_{0}(\chi_{e_{zx}}E_{x} + \chi_{e_{zy}}E_{y} + \chi_{e_{zz}}E_{z})
$$
The nine coefficients of $\chi_{e}$ create up the **susceptibility tensor**. 

#### Boundary Value Problems with Linear Dielectrics
In a (homogeneous isotropic) linear dielectric, the bound charge density $\rho_{b}$ is proportional to the free charge density $\rho_{f}$: 
$$
\rho_{b} = -\nabla \cdot \mathbf{P} = - \nabla \cdot \left(\epsilon_{o} \frac{\chi_{e}}{\kappa} \mathbf{D}\right) = -\left(\frac{\chi_{e}}{1+\chi_{e}}\right)\rho_{f}
$$
In particular, unless free charge is actually embedded in the material, $\rho=0$, and any net charge must reside at the surface. Within such a dielectric, then, the potential obeys Laplace's equation, and all the machinery of before carries over. It is convenient to rewrite the boundary conditions in a way that makes reference only to the free charge. 

From our boundary conditions we expressed prior, we may write 
$$
\epsilon_{above}E^{\perp}_{above} - \epsilon_{below}E^{\perp}_{below} = \sigma_{f}
$$
or, in terms of the potential,
$$
\epsilon_{above}\frac{\partial V_{above}}{\partial n} - \epsilon_{below} \frac{\partial V_{below}}{\partial n} = -\sigma_{f},
$$
whereas the potential itself is, of course, continuous
$$
V_{above} = V_{below}
$$
#### Energy in Dielectric Systems
It takes work to charge up a capacitor:
$$
W = \frac{1}{2}CV^{2}
$$
If the capacitor is filled with linear dielectric, its capacitance exceeds the vacuum value by a factor of the dielectric constant, 
$$
C = \kappa C_{vac}
$$
Evidently, the work necessary to charge a dielectric filled capacitor is increased by the same factor. The reason is pretty clear: you have to pump on more (free) charge, to achieve a given potential, because part of the field is cancelled off by the bound charges. 

The general form for the energy stores in any electrostatic system is 
$$
W = \frac{\epsilon_{0}}{2}\int\limits |\mathbf{E}|^{2}d \tau
$$
The case of the dielectric-filled capacitor suggests that this should be changed to 
$$
W = \frac{\epsilon_{0}}{2}\int\limits \kappa |\mathbf{E}|^{2} d \tau = \frac{1}{2} \int\limits \mathbf{D} \cdot \mathbf{E} d \tau
$$
in the presence of linear dielectrics. To _prove_ it, suppose the dielectric material is fixed in position, and we bring in the free charge, a bit at a time. As ${\rho_{f}}$ is increased by an amount $\Delta \rho_{f}$, the polarization will change and with it the boundary charge distribution; but we're only interested in the work done on the incremental _free_ charge
$$
\Delta W = \int\limits (\Delta \rho_{f}) V d \tau
$$
Since $\nabla \cdot \mathbf{D}=\rho_{f}$, $\Delta \rho_{f} = \nabla \cdot (\Delta \mathbf{D})$, where $\Delta \mathbf{D}$ is the resulting change in $\mathbf{D}$, so 
$$
\Delta W = \int\limits [\nabla \cdot(\Delta \mathbf{D})] \ V d \tau
$$
Now, 
$$
\nabla \cdot [(\Delta D)V] = [\nabla \cdot (\Delta \mathbf{D})]V + \Delta \mathbf{D} \cdot(\nabla V)
$$
and hence, by integration by parts,
$$
\Delta W = \int\limits\nabla \cdot [(\Delta \mathbf{D})V] d \tau + \int\limits(\Delta \mathbf{D}) \cdot \mathbf{E} d \tau 
$$
The divergence theorem turns the first integral into a surface integral, which vanishes if we integrate over all space. Therefore, the work done is equal to 
$$
\Delta W = \int\limits (\Delta \mathbf{D}) \cdot \mathbf{E} d \tau
$$
So far, this applies to _any_ material. Now, if the medium is a linear dielectric, then $\mathbf{D} = \epsilon \mathbf{E}$, so 
$$
\frac{1}{2} \Delta(\mathbf{D} \cdot \mathbf{E}) = \frac{1}{2} \Delta(\epsilon |\mathbf{E}|^{2}) = \epsilon(\Delta \mathbf{E}) \cdot \mathbf{E} = (\Delta \mathbf{D}) \cdot \mathbf{E}
$$
(for infinitesimal increments). Thus
$$
\Delta W = \Delta \left(\frac{1}{2} \int\limits \mathbf{D} \cdot \mathbf{E} d \tau \right)
$$
Thus, the total work done, then, as we built the free charge up from zero to the final configuration, is 
$$
W = \frac{1}{2}\int\limits \mathbf{D} \cdot \mathbf{E}\ d \tau$$
as anticipated. Note that this formula and the formula for general electrostatic systems is different, as the first formula did not include the work involved with stretching and twisting the dielectric molecules during polarization. The first formula only works if we are putting charge after charge in place on the system. But physically, we only bring in the free charges one by one, and the dielectric responds as it sees fit. Thus, each added free charge changes the configuration of bound charges and thus we have molecules or atoms twisting and rotating as discussed previously in polarization. We must account for these when determining the work of the system, so it is most proper that we use the equation derived. 

It is sometimes alleged that this formula for work represent the energy even for nonlinear dielectrics; but this is false. Also note that for _dissipative systems_ the whole notion of "stored energy" loses its meaning, because the work done depends not only on the final configuration but on _how it got there_. In particular, you get nonsensical results if you try to apply this equation to electrets, with frozen-in polarization.

#### Forces on Dielectrics
Just as a conductor is attracted into an electric field, so too is a dielectric, and for essentially the same reason: the bound charge tends to accumulate near the free charge of the opposite sign. But the calculation of forces on dielectrics is quite tricky. Consider the case of a slab of linear dielectric material, partially inserted between the plates of a parallel-plate capacitor. We have always presented that the field is uniform inside a parallel-plate capacitor, and zero outside. 

If this were literally true, there would be no net force on the dielectric at all, since the field everywhere would be perpendicular to the plates. However, there is in reality a **fringing field** around the edges, which for most purposes can be ignored, but in this case is responsible for the whole effect. 

![[Pasted image 20241028134623.png|center|400]]


![[Pasted image 20241028134644.png|center|300]]

Indeed, the field could not terminate abruptly at the edge of the capacitor, for if it did, the line integral of $\mathbf{E}$ around the closed loop shown above would not be zero. It is this nonuniform fringing field that pulls the dielectric into the capacitor. 

Fringing fields are notoriously difficult to calculate; luckily, we can avoid this altogether, but following this ingenious method. Let $W$ be the energy of the system. It depends, of course, on the amount of overlap)\. If I pull the dielectric out of an infinitesimal distance $dx$, the energy is changed by an amount equal to the work done: 
$$
dW = F_{me}dx
$$
where $F_{me}$ is the force I must exert, to counteract the electrical force $F$ on the dielectric: $F_{me} = -F$. Thus the electrical force on the slab is
$$
F = - \frac{dW}{dx}
$$
Now, the energy stored in the capacitor is 
$$
W = \frac{1}{2}CV^{2}
$$
and the capacitance in this case is 
$$
C = \frac{\epsilon_{0}w}{d}(\kappa l - \chi_{e}x)
$$
where $l$ is the length of the plates. Let's assume that the total charge on the plates $Q=CV$ is held constant as the dielectric moves. In terms of $Q$, 
$$
W = \frac{1}{2} \frac{Q^{2}}{C}
$$
so 
$$
F = \frac{-dW}{dx} = \frac{1}{2} \frac{Q^{2}}{C^{2}} \frac{dC}{dx} = \frac{1}{2}V^ 2  \frac{dC}{dx}
$$
But 
$$
\frac{dC}{dx} = - \frac{\epsilon_{0} \chi_{e} w}{d}
$$
and hence 
$$
F = - \frac{\epsilon_{0} \chi_{e} w}{2d} V^{2}
$$
(the minus sign indicates that the force is in the negative $x$ direction, so the dielectric is being pulled into the capacitor). It is an **infamous blunder** to use the equation $W= \frac{1}{2}CV^{2}$ with constant $V$ rather than the equation $W = \frac{1}{2} \frac{Q^{2}}{C}$ with constant $Q$, in computing the force. 

Of course, it is possible to maintain the capacitor at a fixed potential, by connecting it up to a battery. But in that case the _battery also does work_ as the dielectric moves such that 
$$
dW = F_{me} dx + V dQ
$$
where $V dQ$ is the work done by the battery. 

Please understand: the force on the dielectric cannot possibly depend on whether you plan to hold $Q$ or $V$ constant. It is determined entirely by the distribution of charge, free and bound, at the moment in question. It's simpler to _calculate_ the force assuming constant $Q$, because then you don't have to worry about the work done by the battery; but if you insist, it can be done either way. 

Notice that we were able to determine the force without knowing anything about the fringing fields that are ultimately responsible for it. Of course, it's built into the whole structure of electrostatics that $\nabla \times \mathbf{E} = 0$, and hence that the fringing fields must be present; we're not really getting something from nothing here: just cleverly exploiting the internal consistency of the theory. The energy stored in the fringing fields themselves stays constant, as the slab moves; what does change is the energy inside of the capacitor, where the field is nice and uniform. 

