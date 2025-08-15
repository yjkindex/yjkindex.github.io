<!-- 引入 KaTeX 样式 -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.css" integrity="sha384-GvrOXuhMATgEsSwCs4smul74iXGOixntILdUW9XmUC6+HX0sLNAK3q71HotJqlAn" crossorigin="anonymous">

<!-- 引入 KaTeX 核心脚本和自动渲染插件 -->
<script src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.js" integrity="sha384-cpW21h6RZv/phavutF+AuVYrr+dA8xD9zs6FwLpaCct6O9ctzYFfFr4dgmgccOTx" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous"></script>

<!-- 配置自动渲染 -->
<script>
  document.addEventListener("DOMContentLoaded", function() {
    renderMathInElement(document.body, {
      delimiters: [
        {left: "$$", right: "$$", display: false},  // 块级公式
        {left: "$", right: "$", display: false},     // 行内公式
        {left: "\\(", right: "\\)", display: false}
        {left: "\\[", right: "\\]", display: false}
      ]
    });
  });
</script>

# Chapter 1

# Invitation: Pair Production in  $e^{+}e^{-}$  Annihilation

The main purpose of Part I of this book is to develop the basic calculational method of quantum field theory, the formalism of Feynman diagrams. We will then apply this formalism to computations in Quantum Electrodynamics, the quantum theory of electrons and photons.

Quantum Electrodynamics (QED) is perhaps the best fundamental physical theory we have. The theory is formulated as a set of simple equations (Maxwell's equations and the Dirac equation) whose form is essentially determined by relativistic invariance. The quantum- mechanical solutions of these equations give detailed predictions of electromagnetic phenomena from macroscopic distances down to regions several hundred times smaller than the proton.

Feynman diagrams provide for this elegant theory an equally elegant procedure for calculation: Imagine a process that can be carried out by electrons and photons, draw a diagram, and then use the diagram to write the mathematical form of the quantum- mechanical amplitude for that process to occur.

In this first part of the book we will develop both the theory of QED and the method of Feynman diagrams from the basic principles of quantum mechanics and relativity. Eventually, we will arrive at a point where we can calculate observable quantities that are of great interest in the study of elementary particles. But to reach our goal of deriving this simple calculational method, we must first, unfortunately, make a serious detour into formalism. The three chapters that follow this one are almost completely formal, and the reader might wonder, in the course of this development, where we are going. We would like to partially answer that question in advance by discussing the physics of an especially simple QED process—one sufficiently simple that many of its features follow directly from physical intuition. Of course, this intuitive, bottom- up approach will contain many gaps. In Chapter 5 we will return to this process with the full power of the Feynman diagram formalism. Working from the top down, we will then see all of these difficulties swept away.

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/f4b28542ab6d7e101afcb469b100dca40d163a966c75c3719baf460c95397fe9.jpg)  
Figure 1.1. The annihilation reaction  $e^{+}e^{-} \to \mu^{+}\mu^{-}$ , shown in the center-of-mass frame.

# The Simplest Situation

Since most particle physics experiments involve scattering, the most commonly calculated quantities in quantum field theory are scattering cross sections. We will now calculate the cross section for the simplest of all QED processes: the annihilation of an electron with its antiparticle, a positron, to form a pair of heavier leptons (such as muons). The existence of antiparticles is actually a prediction of quantum field theory, as we will discuss in Chapters 2 and 3. For the moment, though, we take their existence as given.

An experiment to measure this annihilation probability would proceed by firing a beam of electrons at a beam of positrons. The measurable quantity is the cross section for the reaction  $e^{+}e^{- } \to \mu^{+}\mu^{- }$  as a function of the center- of- mass energy and the relative angle  $\theta$  between the incoming electrons and the outgoing muons. The process is illustrated in Fig. 1.1. For simplicity, we work in the center- of- mass (CM) frame where the momenta satisfy  $\mathbf{p}^{\prime} = - \mathbf{p}$  and  $\mathbf{k}^{\prime} = - \mathbf{k}$ . We also assume that the beam energy  $E$  is much greater than either the electron or the muon mass, so that  $|\mathbf{p}| = |\mathbf{p}^{\prime}| = |\mathbf{k}| = |\mathbf{k}^{\prime}| = E \equiv E_{\mathrm{cm}} / 2$ . (We use boldface type to denote 3- vectors and ordinary italic type to denote 4- vectors.)

Since both the electron and the muon have spin  $1 / 2$ , we must specify their spin orientations. It is useful to take the axis that defines the spin quantization of each particle to be in the direction of its motion; each particle can then have its spin polarized parallel or antiparallel to this axis. In practice, electron and positron beams are often unpolarized, and muon detectors are normally blind to the muon polarization. Hence we should average the cross section over electron and positron spin orientations, and sum the cross section over muon spin orientations.

For any given set of spin orientations, it is conventional to write the differential cross section for our process, with the  $\mu^{- }$  produced into a solid angle  $d\Omega$ , as

$$
\frac{d\sigma}{d\Omega} = \frac{1}{64\pi^{2}E_{\mathrm{cm}}^{2}} \cdot |\mathcal{M}|^{2}. \tag{1.1}
$$

The factor  $E_{\mathrm{cm}}^{- 2}$  provides the correct dimensions for a cross section, since in our units (energy)  $- 2 \sim (\mathrm{length})^{2}$ . The quantity  $\mathcal{M}$  is therefore dimensionless; it is the quantum- mechanical amplitude for the process to occur (analogous to the scattering amplitude  $f$  in nonrelativistic quantum mechanics), and we must now address the question of how to compute it from fundamental theory. The other factors in the expression are purely a matter of convention. Equation (1.1) is actually a special case, valid for CM scattering when the final state contains two massless particles, of a more general formula (whose form cannot be deduced from dimensional analysis) which we will derive in Section 4.5.

Now comes some bad news and some good news.

The bad news is that even for this simplest of QED processes, the exact expression for  $\mathcal{M}$  is not known. Actually this fact should come as no surprise, since even in nonrelativistic quantum mechanics, scattering problems can rarely be solved exactly. The best we can do is obtain a formal expression for  $\mathcal{M}$  as a perturbation series in the strength of the electromagnetic interaction, and evaluate the first few terms in this series.

The good news is that Feynman has invented a beautiful way to organize and visualize the perturbation series: the method of Feynman diagrams. Roughly speaking, the diagrams display the flow of electrons and photons during the scattering process. For our particular calculation, the lowest- order term in the perturbation series can be represented by a single diagram, shown in Fig. 1.2. The diagram is made up of three types of components: external lines (representing the four incoming and outgoing particles), internal lines (representing "virtual" particles, in this case one virtual photon), and vertices. It is conventional to use straight lines for fermions and wavy lines for photons. The arrows on the straight lines denote the direction of negative charge flow, not momentum. We assign a 4- momentum vector to each external line, as shown. In this diagram, the momentum  $q$  of the one internal line is determined by momentum conservation at either of the vertices:  $q = p + p' = k + k'$ . We must also associate a spin state (either "up" or "down") with each external fermion.

According to the Feynman rules, each diagram can be translated directly into a contribution to  $\mathcal{M}$ . The rules assign a short algebraic factor to each element of a diagram, and the product of these factors gives the value of the corresponding term in the perturbation series. Getting the resulting expression for  $\mathcal{M}$  into a form that is usable, however, can still be nontrivial. We will develop much useful technology for doing such calculations in subsequent chapters. But we do not have that technology yet, so to get an answer to our particular problem we will use some heuristic arguments instead of the actual Feynman rules.

Recall that in quantum- mechanical perturbation theory, a transition amplitude can be computed, to first order, as an expression of the form

$$
\langle \mathrm{final~state} | H_{I} | \mathrm{initial~state} \rangle , \tag{1.2}
$$

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/22354ee076dc06d5ec3184c235bed7569b2b36b9cd3151b52c8a0ef3ae0e2880.jpg)  
Figure 1.2. Feynman diagram for the lowest-order term in the  $e^{+}e^{-} \rightarrow \mu^{+}\mu^{-}$  cross section. At this order the only possible intermediate state is a photon  $(\gamma)$ .

where  $H_{I}$  is the "interaction" part of the Hamiltonian. In our case the initial state is  $|e^{+}e^{- }\rangle$  and the final state is  $\langle \mu^{+}\mu^{- }\vert$ . But our interaction Hamiltonian couples electrons to muons only through the electromagnetic field (that is, photons), not directly. So the first- order result (1.2) vanishes, and we must go to the second- order expression

$$
\mathcal{M} \sim \langle \mu^{+}\mu^{-} | H_{I} | \gamma \rangle^{\mu} \langle \gamma | H_{I} | e^{+}e^{-} \rangle_{\mu}. \tag{1.3}
$$

This is a heuristic way of writing the contribution to  $\mathcal{M}$  from the diagram in Fig. 1.2. The external electron lines correspond to the factor  $|e^{+}e^{- }\rangle$ ; the external muon lines correspond to  $\langle \mu^{+}\mu^{- }\vert$ . The vertices correspond to  $H_{I}$ , and the internal photon line corresponds to the operator  $|\gamma \rangle \langle \gamma |$ . We have added vector indices  $(\mu)$  because the photon is a vector particle with four components. There are four possible intermediate states, one for each component, and according to the rules of perturbation theory we must sum over intermediate states. Note that since the sum in (1.3) takes the form of a 4- vector dot product, the amplitude  $\mathcal{M}$  will be a Lorentz- invariant scalar as long as each half of (1.3) is a 4- vector.

Let us try to guess the form of the vector  $\langle \gamma | H_{I} | e^{+}e^{- } \rangle_{\mu}$ . Since  $H_{I}$  couples electrons to photons with a strength  $e$  (the electron charge), the matrix element should be proportional to  $e$ . Now consider one particular set of initial and final spin orientations, shown in Fig. 1.3. The electron and muon have spins parallel to their directions of motion; they are "right- handed". The antiparticles, similarly, are "left- handed". The electron and positron spins add up to one unit of angular momentum in the  $+z$  direction. Since  $H_{I}$  should conserve angular momentum, the photon to which these particles couple must have the correct polarization vector to give it this same angular momentum:

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/2cd5784106107e506a7895be18ab880f88185e00e8cb015272ec6bec06028e14.jpg)  
Figure 1.3. One possible set of spin orientations. The electron and the negative muon are right-handed, while the positron and the positive muon are left-handed.

$e^{\mu} = (0,1,i,0)$ . Thus we have

$$
\langle \gamma |H_{I}|e^{+}e^{-}\rangle^{\mu}\propto e(0,1,i,0). \tag{1.4}
$$

The muon matrix element should, similarly, have a polarization corresponding to one unit of angular momentum along the direction of the  $\mu^{- }$  momentum  $\mathbf{k}$ . To obtain the correct vector, rotate (1.4) through an angle  $\theta$  in the  $xz$ - plane:

$$
\langle \gamma |H_{I}|\mu^{+}\mu^{-}\rangle^{\mu}\propto e(0,\cos \theta ,i, - \sin \theta). \tag{1.5}
$$

To compute the amplitude  $\mathcal{M}$ , we complex- conjugate this vector and dot it into (1.4). Thus we find, for this set of spin orientations,

$$
\mathcal{M}(RL\rightarrow RL) = -e^{2}\left(1 + \cos \theta\right). \tag{1.6}
$$

Of course we cannot determine the overall factor by this method, but in (1.6) it happens to be correct, thanks to the conventions adopted in (1.1). Note that the amplitude vanishes for  $\theta = 180^{\circ}$ , just as one would expect: A state whose angular momentum is in the  $+z$  direction has no overlap with a state whose angular momentum is in the  $- z$  direction.

Next consider the case in which the electron and positron are both right- handed. Now their total spin angular momentum is zero, and the argument is more subtle. We might expect to obtain a longitudinally polarized photon with a Clebsch- Gordan coefficient of  $1 / \sqrt{2}$ , just as when we add angular momenta in three dimensions,  $|\uparrow \downarrow \rangle = (1 / \sqrt{2})(|j = 1,m = 0\rangle +|j = 0,m = 0\rangle)$ . But we are really adding angular momenta in the four- dimensional Lorentz group, so we must take into account not only spin (the transformation properties of states under rotations), but also the transformation properties of states under boosts. It turns out, as we shall discuss in Chapter 3, that the Clebsch- Gordan coefficient that couples a 4- vector to the state  $|e_{R}^{- }e_{R}^{+}\rangle$  of massless fermions is zero. (For the record, the state is a superposition of scalar and antisymmetric tensor pieces.) Thus the amplitude  $\mathcal{M}(RR\rightarrow RL)$  is zero, as are the eleven

other amplitudes in which either the initial or final state has zero total angular momentum.

The remaining nonzero amplitudes can be found in the same way that we found the first one. They are

$$
\begin{array}{r l} & {\mathcal{M}(R L\rightarrow L R) = -e^{2}\left(1 - \cos \theta\right),}\\ & {\mathcal{M}(L R\rightarrow R L) = -e^{2}\left(1 - \cos \theta\right),}\\ & {\mathcal{M}(L R\rightarrow L R) = -e^{2}\left(1 + \cos \theta\right).} \end{array} \tag{1.7}
$$

Inserting these expressions into (1.1), averaging over the four initial- state spin orientations, and summing over the four final- state spin orientations, we find

$$
\frac{d\sigma}{d\Omega} = \frac{\alpha^{2}}{4E_{\mathrm{cm}}^{2}}\big(1 + \cos^{2}\theta \big), \tag{1.8}
$$

where  $\alpha = e^{2} / 4\pi \simeq 1 / 137$ . Integrating over the angular variables  $\theta$  and  $\phi$  gives the total cross section,

$$
\sigma_{\mathrm{total}} = \frac{4\pi\alpha^{2}}{3E_{\mathrm{cm}}^{2}}. \tag{1.9}
$$

Results (1.8) and (1.9) agree with experiments to about  $10\%$ ; almost all of the discrepancy is accounted for by the next term in the perturbation series, corresponding to the diagrams shown in Fig. 1.4. The qualitative features of these expressions—the angular dependence and the sharp decrease with energy—are obvious in the actual data. (The properties of these results are discussed in detail in Section 5.1. )

# Embellishments and Questions

We obtained the angular distribution predicted by Quantum Electrodynamics for the reaction  $e^{+}e^{- }\rightarrow \mu^{+}\mu^{- }$  by applying angular momentum arguments, with little appeal to the underlying formalism. However, we used the simplifying features of the high- energy limit and the center- of- mass frame in a very strong way. The analysis we have presented will break down when we relax any of our simplifying assumptions. So how does one perform general QED calculations? To answer that question we must return to the Feynman rules.

As mentioned above, the Feynman rules tell us to draw the diagram(s) for the process we are considering, and to associate a short algebraic factor with each piece of each diagram. Figure 1.5 shows the diagram for our reaction, with the various assignments indicated.

For the internal photon line we write  $- i g_{\mu \nu} / q^{2}$ , where  $g_{\mu \nu}$  is the usual Minkowski metric tensor and  $q$  is the 4- momentum of the virtual photon. This factor corresponds to the operator  $|\gamma \rangle \langle \gamma |$  in our heuristic expression (1.3).

For each vertex we write  $- i e\gamma^{\mu}$ , corresponding to  $H_{I}$  in (1.3). The objects  $\gamma^{\mu}$  are a set of four  $4\times 4$  constant matrices. They do the "addition of angular

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/99dbfe58f0e51756fc2d16321fe6ac3d880fe798097928ebdfe4c2a15218d40c.jpg)  
Figure 1.4. Feynman diagrams that contribute to the  $\alpha^{3}$  term in the  $e^{+}e^{-} \rightarrow \mu^{+}\mu^{-}$  cross section.

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/7c2fb3ff669904366fedbf033d3a94200d2d0bba0823838d36a89c0ec4a35b34.jpg)  
Figure 1.5. Diagram of Fig. 1.2, with expressions corresponding to each vertex, internal line, and external line.

momentum" for us, coupling a state of two spin- 1/2 particles to a vector particle.

The external lines carry expressions for four- component column- spinors  $u, v$ , or row- spinors  $\bar{u}, \bar{v}$ . These are essentially the momentum- space wavefunctions of the initial and final particles, and correspond to  $|e^{+}e^{- }\rangle$  and  $\langle \mu^{+}\mu^{- }|$  in (1.3). The indices  $s, s^{\prime}, r$ , and  $r^{\prime}$  denote the spin state, either up or down.

We can now write down an expression for  $\mathcal{M}$ , reading everything straight off the diagram:

$$
\begin{array}{l}{{{\mathcal{M}}=\bar{v}^{s^{\prime}}(p^{\prime})(-i e\gamma^{\mu})u^{s}(p)\left(\frac{-i g_{\mu\nu}}{q^{2}}\right)\bar{u}^{r}(k)\left(-i e\gamma^{\nu}\right)v^{r^{\prime}}(k^{\prime})}}\\ {{~=\frac{i e^{2}}{q^{2}}\big(\bar{v}^{s^{\prime}}(p^{\prime})\gamma^{\mu}u^{s}(p)\big)\big(\bar{u}^{r}(k)\gamma_{\mu}v^{r^{\prime}}(k^{\prime})\big).}}\end{array} \tag{1.10}
$$

(1.10)

It is instructive to compare this in detail with Eq. (1.3).

To derive the cross section (1.8) from (1.10), we could return to the angular momentum arguments used above, supplemented with some concrete knowledge about  $\gamma$  matrices and Dirac spinors. We will do the calculation in this manner in Section 5.2. There are, however, a number of useful tricks that can be employed to manipulate expressions like (1.10), especially when one wants to compute only the unpolarized cross section. Using this "Feynman trace technology" (so- called because one must evaluate traces of products of  $\gamma$ - matrices), it isn't even necessary to have explicit expressions for the  $\gamma$ - matrices and Dirac spinors. The calculation becomes almost completely mindless, and the answer (1.8) is obtained after less than a page of algebra. But since the Feynman rules and trace technology are so powerful, we can also relax some of our simplifying assumptions. To conclude this section, let us discuss several ways in which our calculation could have been more difficult.

The easiest restriction to relax is that the muons be massless. If the beam energy is not much greater than the mass of the muon, all of our predictions should depend on the ratio  $m_{\mu} / E_{\mathrm{cm}}$ . (Since the electron is 200 times lighter than the muon, it can be considered massless whenever the beam energy is large enough to create muons.) Using Feynman trace technology, it is extremely easy to restore the muon mass to our calculation. The amount of algebra is increased by about fifty percent, and the relation (1.1) between the amplitude and the cross section must be modified slightly, but the answer is worth the effort. We do this calculation in detail in Section 5.1.

Working in a different reference frame is also easy; the only modification is in the relation (1.1) between the amplitude and the cross section. Or one can simply perform a Lorentz transformation on the CM result, boosting it to a different frame.

When the spin states of the initial and/or final particles are known and we still wish to retain the muon mass, the calculation becomes somewhat cumbersome but no more difficult in principle. The trace technology can be generalized to this case, but it is often easier to evaluate expression (1.10) directly, using the explicit values of the spinors  $u$  and  $v$ .

Next one could compute cross sections for different processes. The process  $e^{+}e^{- } \rightarrow e^{+}e^{- }$ , known as *Bhabha scattering*, is more difficult because there is a second allowed diagram (see Fig. 1.6). The amplitudes for the two diagrams must first be added, then squared.

Other processes contain photons in the initial and/or final states. The

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/da7c1a99a620461ec1d347d34d322c3466a6ad493fa20eb2cfafd3804af2bfc6.jpg)  
Figure 1.6. The two lowest-order diagrams for Bhabha scattering,  $e^{+}e^{-} \to e^{+}e^{-}$ .

![](https://cdn-mineru.openxlab.org.cn/result/2025-08-11/62d18ea5-59f8-4512-82a9-74b56cbc4a9e/bdfc55378c10126c1b6b17714672dd37b93778a54fcd53fac65620c4fb6101b8.jpg)  
Figure 1.7. The two lowest-order diagrams for Compton scattering.

paradigm example is Compton scattering, for which the two lowest- order diagrams are shown in Fig. 1.7. The Feynman rules for external photon lines and for internal electron lines are no more complicated than those we have already seen. We discuss Compton scattering in detail in Section 5.5.

Finally we could compute higher- order terms in the perturbation series. Thanks to Feynman, the diagrams are at least easy to draw; we have seen those that contribute to the next term in the  $e^{+}e^{- } \to \mu^{+}e^{- }$  cross section in Fig. 1.4. Remarkably, the algorithm that assigns algebraic factors to pieces of the diagrams holds for all higher- order contributions, and allows one to evaluate such diagrams in a straightforward, if tedious, way. The computation of the full set of nine diagrams is a serious chore, at the level of a research paper.

In this book, starting in Chapter 6, we will analyze much of the physics that arises from higher- order Feynman diagrams such as those in Fig. 1.4. We will see that the last four of these diagrams, which involve an additional photon in the final state, are necessary because no detector is sensitive enough to notice the presence of extremely low- energy photons. Thus a final state containing such a photon cannot be distinguished from our desired final state of just a muon pair.

The other five diagrams in Fig. 1.4 involve intermediate states of several virtual particles rather than just a single virtual photon. In each of these diagrams there will be one virtual particle whose momentum is not determined by conservation of momentum at the vertices. Since perturbation theory requires us to sum over all possible intermediate states, we must integrate over all possible values of this momentum. At this step, however, a new difficulty appears: The loop- momentum integrals in the first three diagrams, when performed naively, turn out to be infinite. We will provide a fix for this problem, so that we get finite results, by the end of Part I. But the question of the physical origin of these divergences cannot be dismissed so lightly; that will be the main subject of Part II of this book.

We have discussed Feynman diagrams as an algorithm for performing computations. The chapters that follow should amply illustrate the power of this tool. As we expose more applications of the diagrams, though, they begin to take on a life and significance of their own. They indicate unsuspected relations between different physical processes, and they suggest intuitive arguments that might later be verified by calculation. We hope that this book will enable you, the reader, to take up this tool and apply it in novel and enlightening ways.