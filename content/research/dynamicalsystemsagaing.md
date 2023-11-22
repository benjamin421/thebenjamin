---
title: "A Dynamical Systems View of Aging"
date: 2022-06-23
draft: false
description: "Aggregated research showcasing the understanding gained by considering aging as a dynamic system."
slug: "dynamical-systems-aging"
subjects: ["Dynamical Systems", "Control Theory", "Free Energy Principle", "Aging"]
showDate: false
showHeadingAnchors: true
showAuthor: true
showReadingTime: false
showEdit: true
showSummary: true
showPagination: true

---

{{< lead >}}
Last updated — June 2022 | Aggregated research showcasing the understanding gained by considering aging as a dynamic system.
{{< /lead >}}

## Overview

Information presented here together my provide insight into how dynamical systems concepts can be useful tools to elucidate novel intervention strategies in aging. 

## Definitions / Concepts

**Limit Cycle**: In a limit cycle, a system's state oscillates around a fixed point or set of fixed points in a repeating pattern without ever reaching a true equilibrium. 

## Biological States as Attractors
### *Answering Schrödinger's question: A free-energy formulation*[^1]
>Biological systems are characterised by a random dynamical attractor—a set of attracting states that are frequently revisited. Indeed, the characteristics by which we define living systems are simply statements about the characteristic, attracting states in which we find them. This set of attracting states can be interpreted as the extended phenotype of the organism—its morphology, physiology, behavioural patterns, cultural patterns, and designer environments.

>Free energy minimisation dynamics vary across timescales, ranging from neurocognition in real-time (i.e., perception and action; learning and attention); neurodevelopment throughout the lifespan; epigenetic mechanisms that minimise free energy across generations (e.g., kin); and the process of adaptation, which involves the optimisation of human generative models over time and conspecifics via the inheritance of adaptive priors.

>Here, selection is simply nature’s way of performing Bayesian model optimisation by minimising the (variational) [[free energy]] of human phenotypes across different (Tinbergian) timescales (Fig. 4, panel C). Emphasis is placed on adaptive priors, which are (epi)genetically-specified expectations that have been shaped by selection to guide action-perception cycles toward adaptive or unsurprising states.

### *Competency in Navigating Arbitrary Spaces as an Invariant for Analyzing Cognition in Diverse Embodiments*[^2]
>For biological systems at any scale, the relevant attractors are those that implement allostasis within the current environment. The variational free energy (VFE) principle formulates this requirement for allostasis in information-theoretic terms: living systems behave so as to maximize their ability to predict their own future states. When we identify VFE with uncertainty and hence with (the probability of) prediction error, the minima of VFE become the maxima of predictive success. Uncertainty, and hence VFE, is distinct from metabolic load. Hence, we can ask about the metabolic cost of achieving an increment of predictive ability. The metabolic cost of generating predictions through the use of some computational model of the environment emphasizes that moving through the search space really is a search. It takes effort and resources, including memory resources. As cells or other systems become stressed (e.g., by lack of sufficient free-energy resources), their generative models can be expected to deteriorate toward stochastic defaults, and hence their searches can be expected to deteriorate toward random walks."

>Markov blankets as system–environment interfaces and VFE minimization as an inferential mechanism characterize all systems identifiable as such over time, including macromolecules, biomolecular pathways, individual cells (whether free-living or components of multicellular organisms), organs and tissues, individual organisms, communities of organisms, ecosystems, and even larger structures.

>Any organism—indeed, any physical system, classical or quantum—can be considered to behave in the Hilbert space that characterizes its MB.

### *Modeling somatic computation with non-neural bioelectric networks*[^3]
>Transient inputs that shift the endogenous bioelectric network states into alternate stable modes can permanently change regenerative and developmental morphology; because of this, mutations in ion channel genes are an important cause of human birth defects, while modulation of bioelectric circuit state has been used to repair brain structure.

>BEN networks have a layered architecture, a scheme that is widely adopted for ANNs but which also refects the tissue layering of many diferent types of body structures. In this scheme, a network consists of multiple layers of cells, with diferent choices for the inter-layer and intra-layer connectivity. Some layers have clearly designated roles—for example, the frst layer is the “input” and the last layer is the “output”. This follows the scheme of various biological systems with specifc roles assigned to the layers. For example, the retina is the “sensory” layer that directly receives signals from the environment and sends it to the upstream inter-neuron  layers that integrates the input. The layered architecture is inspired by biological counterparts as diverse as the mammalian visual cortex and cellular signaling networks, whose benefts include better organization and efficiency of information processing and prediction.

---
## Limit Cycles in Biological Systems
### *Shift of a limit cycle in biology: From pathological to physiological homeostasis*[^4]
>Biological systems may show homeostatic behaviors that are similar to the ones of forced dynamic systems with a stable limit cycle. For a large class of dynamic systems, it is shown that a shift of a pathological limit cycle over the physiological limit cycle can never be executed by means of a control with a desired periodicity. The above statement shows that the only possibility is to reduce as much as possible the dimensions of a small residual limit cycle. Moreover, it is possible to give some information about the structure of feedback laws that would allow the shift of the limit cycle. The fact that it is generally not possible to recover a physiological limit cycle from a pathological one, results into the fear of never or hardly ever reaching a physiological behavior, and it seems that any hope of therapeutics is given up. This leads to introduce the locking concept, which permits system parameters to change and provides the basis for an adaptive and iterative control, which allows a step by step approach and to finally reach the physiological limit cycle.

>Possible locking of nonlinear oscillators suggest a nonlinear adaptive control process of imbalances, since system parameters can change and iterative control allows a step-by-step approach to finally reach the physiological limit cycle.

### *Nonlinear adaptive control of adrenal-postpituitary imbalances and identifiability analysis*[^5]
> The aim of the control is to minimize the difference between the pathological evolution and the physiological one.

>So the only way to solve the control problem consists in reducing as much as possible a small residual limit cycle.

>The first step consists in searching the control to be applied to the pathological system in order to obtain a limit cycle as close as possible to the physiological one.

---

## Free Energy Guides Direction 
### *The Free Energy Principle drives neuromorphic development*[^6]
> Any system with morphological degrees of freedom and locally limited free energy will, under the constraints imposed by the free energy principle, evolve toward a neuromorphic morphology that supports hierarchical computations in which each “level” of the hierarchy enacts a coarse-graining of its inputs, and dually a fine-graining of its outputs. Such hierarchies occur throughout biology, from the architectures of intracellular signaltransduction pathways to the large-scale organization of perception and action processing in the mammalian brain.

### *Somatic multicellularity as a satisficing solution to the prediction-error minimization problem*[^7]
>Reproductive (proto-)stem cells construct multicellular bodies in order to reduce the variational free energy of information exchange with the immediate environment and hence to minimize prediction error as regards their own survival. From this FEP perspective, somatic multicellularity is a natural outcome of environmental challenges faced by free-living cells, with the primary genetic driver of multicellularity being the development of intercellular signals for cell-cycle arrest. In this “imperial” model of multicellularity, reproductively-competent stem and/ or germ cells produce reproductively-incompetent somatic cells in order to advance their own genetic interests by establishing an environment-facing cellular layer that reduces uncertainty and improves predictive power (and thus physiological adaptation) for the internal cells.

>Markov blankets in which every input node is connected by a path to some output node and vice-versa fully expose C to E, i.e. correspond to β = 1. Such blankets are in a natural sense “transparent” to VFE. States in which no path exists from any input node to any output node fully protect C from E, correspond to β = 0, and are in a natural sense “opaque.”

---

## Aging
### *Longitudinal analysis of blood markers reveals progressive loss of resilience and predicts human lifespan limit*[^8]
>We put forward arguments suggesting that such behavior is typical for complex systems near a bifurcation (disintegration) point and thus the progressive loss of resilience with age may be a dynamic origin of the Gompertz law.

>...equilibrium solution of the organism growth problem appears to be unstable in the long run and the organism state dynamics measured by DOSI exhibits deviations from the stationary solution beyond the age of ~40 years old.

>According to the theory, the development of any organism is the result of a competition between the production of new tissue and life-sustaining activities. The total amount of the energy available scales as the fractional power of the body mass _m_3/4 according to the universal allometric Kleiber–West law[46](https://www.nature.com/articles/s41467-021-23014-1#ref-CR46),[47](https://www.nature.com/articles/s41467-021-23014-1#ref-CR47). On the one hand, the energy requirements for the organism maintenance increase linearly as the body mass grows and hence the initial excess metabolic power drives the growth of the organism until it reaches the dynamic equilibrium corresponding to the mature animal state.

>Aging leads to a gradual decrease in the activation energy and barrier curvature and an exponential increase in the probability of barrier crossing. The stochastic activation into a dynamically unstable (frail) state is associated with acquisition of multiple morbidities and certain death of an organism.

### *Unsupervised learning of aging principles from longitudinal data*[^9]
>The association of the fluctuations along the dominant PC with the slowest dynamic process (aging, in our case) has deep roots in the dynamic systems theory and critical phenomena[14](https://www.nature.com/articles/s41467-022-34051-9#ref-CR14). The transition from stability to instability in networks with the network graphs not possessing specific symmetries is typically associated with co-dimension 1 (or saddle-node) bifurcations[20](https://www.nature.com/articles/s41467-022-34051-9#ref-CR20),[21](https://www.nature.com/articles/s41467-022-34051-9#ref-CR21). Such transitions are characterized by the loss of stability along a single direction in the state vector space, approximately coinciding with the first principal component.

---

### Citation
In academic work, please cite this essay as:

_Anderson, Benjamin, “A Dynamical Systems View of Aging”, TheBenjam.in (2022-06-23), available at https://www.thebenjam.in/research/._

[^1]: Maxwell James Désormeau Ramstead, Paul Benjamin Badcock, Karl John Friston, Answering Schrödinger's question: A free-energy formulation, Physics of Life Reviews, Volume 24, 2018, Pages 1-16, ISSN 1571-0645, https://doi.org/10.1016/j.plrev.2017.09.001
[^2]: Fields C, Levin M. Competency in Navigating Arbitrary Spaces as an Invariant for Analyzing Cognition in Diverse Embodiments. Entropy. 2022; 24(6):819. https://doi.org/10.3390/e24060819
[^3]: Manicka, S., Levin, M. Modeling somatic computation with non-neural bioelectric networks. Sci Rep 9, 18612 (2019). https://doi.org/10.1038/s41598-019-54859-8
[^4]: Daniel Claude; Shift of a limit cycle in biology: From pathological to physiological homeostasia*. Chaos 1 March 1995; 5 (1): 162–166. https://doi.org/10.1063/1.166099
[^5]: Claude, D., & Nadjar, N. (1994). Nonlinear adaptive control of adrenal-postpituitary imbalances and identifiability analysis. Mathematical biosciences, 121(2), 155–192. https://doi.org/10.1016/0025-5564(94)90069-8
[^6]: Chris Fields et al 2022 Neuromorph. Comput. Eng. 2 042002
DOI 10.1088/2634-4386/aca7de
[^7]: Chris Fields, Michael Levin. (2020) Does regeneration recapitulate phylogeny? Planaria as a model of body-axis specification in ancestral eumetazoa. Communicative & Integrative Biology 13:1, pages 27-38.
[^8]: Pyrkov, T.V., Avchaciov, K., Tarkhov, A.E. et al. Longitudinal analysis of blood markers reveals progressive loss of resilience and predicts human lifespan limit. Nat Commun 12, 2765 (2021). https://doi.org/10.1038/s41467-021-23014-1
[^9]: Avchaciov, K., Antoch, M.P., Andrianova, E.L. et al. Unsupervised learning of aging principles from longitudinal data. Nat Commun 13, 6529 (2022). https://doi.org/10.1038/s41467-022-34051-9