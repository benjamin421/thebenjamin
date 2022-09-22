---
title: "The Free Energy Theory of Aging"
date: 2022-09-05
draft: false
description: "Using the free energy principle to denote the model structure of the aging process."
slug: "free-energy-theory-aging"
subjects: ["Causal Emergence", "Free Energy Principle", "Aging"]
showDate: false
showHeadingAnchors: true
showAuthor: true
showReadingTime: false
showEdit: true
showSummary: true
showPagination: true

---

{{< lead >}}
Last updated — September 2022 | Using the free energy principle to denote the model structure of the aging process.
{{< /lead >}}

## Introduciton
I have been captured by ideas in aging and longevity reseach for as long as I can remember. In high school outside the debate classroom, I would rally peers to join me for discussions on heretical ideas that seemed far beyond reach, but to which I may have caught a recent article hinting at the purported possibility of the idea. We talked about ideas from Cold Fusion, to Witricity, Myostatin treatments and more. None captured my attention more however than those discussions that covered the subject of radical longevity and the aging process. 

Over time, I've come to a conclusion that I find to be unique based on my conversations with others in this field. 

I am a biomedical engineering dropout accredited only by discipline and experience, focusing on the biology of aging in my spare time. I have been fortunate enough to pressure test these ideas through conversations in person with the top aging researchers in the field at the inaugural [GRC Systems Aging Conference](https://www.forbes.com/sites/alexzhavoronkov/2022/06/29/a-week-at-the-most-secretive-conference-on-aging/?sh=3ad11077201d) in May, 2022. 

When bringing this concept up, the top comments I recieved were that is was viable and an unexplored direction, however given the fact that it was relatively unexplored, conversations could only go so far. It is for this reason that I am taking the next step to pressure test the idea here. 

---

## The Free Energy Theory of Aging

There is an idea from neuroscience referred to as the free energy principle. What this principle says is that systems that are evolving through time, evolve and adapt in ways that minimize the amount of energy required to do the same things over and over again. 

This is sort of similar to the idea of Hebbian Learning which is commonly remembered by the saying: 'neurons that fire together, wire together.'

As these systems adapt to minimize energy allocated for their most common processes, this comes at an alternate cost. That cost is in the resilience to other stressors that system might have to deal with.[^1] 

I was introduced to the idea of the free energy principle when I read a paper called *The math is not the territory*[^2]. I had come across a personality on Twitter named Mel Andrews, aka [@bayesianboy](https://twitter.com/bayesianboy), and at the time, it was their pinned tweet. I was captured by the title, and so added it to my bookmarks to read in the near future.

In Andrews' paper, they talk about the free energy principle's background in neuroscience, it's increased adaptation in other verticals, and proposes:

> ...that the FEP be reserved to designate a model structure, to which philosophers and scientists add various construals...

...rather than a model in and of itself exclusive to neuroscience. 

By the time I finished reading this paper, I had become convinced that this idea explained something that I had been circling the drain on for a long time. 

### Background
Before I read this paper, I had been doing program analyses on gene regulatory networks and protein interactomes to find out their causal emergence properties.[^3] Causal Emergence is an idea from [Eric Hoel](https://twitter.com/erikphoel) suggesting that macro scale representations of systems can reduce the noise in causal relationships, thereby increasing the causal determinism of the system in it's new macro representation.[^4]

Macro scale networks contain more effective information than a microscale network. Effective information is the assessment of the causal power of a cause, *c* to produce an effect, *e* for all possible transitions between all possible causes and effects. 

I was intrigued by this idea because it sounded like one that might be productively applied to increasing our understanding of gene regulatory networks, which are often very complex, and therefore hard to track causality across their interactions. Extremely fine grained causal models in these networks obscure more data than they provide insight due to inherent noise. Intrinsic noise in a biological system manifests as uncertainty between state transitions.[^5]

> Biological networks have the lowest effectiveness values. This is because redundancy, degeneracy and noise are high. This is a strong indicator of biological informative connectivity taking place at a higher scale.[^6]

Hoel has since released another paper[^7] expanding on his idea. In it, he talks about how what may be happening by means of causal emergence is the transition from redundant information to synergistic information at a higher scale. It is here from my exposure to the language of 'redundant and synergistic information' that got my brain thinking about the complexities of interactions in their original form as 'redundant', i.e. multiple ways of achieving the same end. 

This leads to the certainty paradox inside of our internal biological networks. The paradox is that redundancy in connectivity is desirable since it is protective from node failures.

For example, if a harmful intervention enters the network that disrups pathway A -> B -> C, then the network can still bring about the homeostatic outcome by routing this interaction through A -> D -> C.

![Image of redundant pathway explanation](/img/redundancy.png)

Over time, examples like the one pictured above become less and less the case. Our biological networks decrease in complexity[^8], and futhermore their redundancy throughout time. With this decrease in redundancy comes too a decrease in resilience to potential stressors and harmful interventions. 

![Image of decrease in redundancy over time](/img/katephoto.png)
_Photo courtesy of [Kate Crosby](https://scholar.google.com/scholar?q=author:%22Crosby%20Kate%22) after I explained these ideas._

The closest theory of aging I've come across that aligns with the ideas that I've described up to this point is David Sinclair's Information Theory of Aging. In Sinclair's theory he states that the loss of epigenetic markers disrupts youthful gene expression patterns, leading to cellular disfunction and senescence. 

Despite my appreciation for this corollary draw between what I've explained above and how it may be caused by this loss of epigenetic markers, what I believe is missing from Sinclair's theory is an explanation as to *why* our body has adapted over time to loose these markers—and with them, our youth. 

Finally, I can return to why all this is relevant to the free energy principle. 

### The Main Idea
I believe that by using the free energy principle to denote the model structure of the aging process, we can gain a new level of understanding as to why these changes are taking place in our bodies and bringing about less resilient phenotypes at large.

That new level of understanding is:

**Loss of epigenetic markers are the means by which our body adheres to the free energy principle: decreasing transition uncertainty by adapting them towards a more energy minimizing state of function.**

This energy minimizing state of function comes at the cost of resilience to stressors, and I believe aging as a whole. 

### Conclusion and Paths Forward
I am only just starting to use this additional context from the free energy principle in order to come to new areas of exploration for how to intervene upon this process. 

I wanted to share these ideas as soon as I had them clearly formulated enough that it may be valuable to someone exploring similar veins of biology.

In biology, we look for policies to control interactions. 

The model I outline above is the policy, and here are some potential control mechanisms to bring about our desired effect: 
- Up/down regulation of genes
- Optogenetic stimulation of neurons
- Transcranial magnetic simulation
- Randomized drug trial
- ***Modulation on endogenous bioelectric networks**
- Genetic knock-out/knock-in

I have became excited by one potential control mechanism in particular. In the [Allen Discovery Center](https://allencenter.tufts.edu/) at Tufts University, [Michael Levin](https://twitter.com/drmichaellevin) and his lab are mapping causal relationships between electrochemical gradients and transcriptional processes.

The electrochemical gradient consists of the free energy potential difference across the cell membrane in 2 places:
1) Small molecule concentrations (chemical potential differences)
2) Moving charged molecules (electrical potential differences)

They refer to these causal relationships between the multi and single cellular levels of operation as intracellular signalling-dependent transcription.[^9] In these cases, electrochemical gradient states are shown to be causally upstream to single cellular dynamics to create transcription predictions that can then be associated with epigenetic processes.

The path forward I am currently exploring are places where Levin and his team have shown intracellular signalling-dependent transcription to be prevalent between the electrochemical gradient and histone deacetylation specifically.

> If epigenetic mechanisms are important for guiding regeneration, how might these mechanisms link to upstream bioelectric controls? One system in which such a pathway has been elucidated is the orientation of the early embryonic left-right axis by an endogenous Left to Right voltage gradient. Recent work demonstrated that a histone de-acetylation mechanism converts the very early voltage gradient into asymmetric gene expression at much later stages by rightward electrophoretic transport of serotonin—a cofactor for a histone deacetylase...Moreover, pharmacological reduction of HDAC activity using the inhibitor, sodium butyrate, also induced heterotaxia, characterized by increased histone acetylation and aberrant expression of the conserved left-right asymmetry marker, Nodal related 1 (Xnr-1) gene.[^10]

Histone deacylation is a mechanism by which lost epigenetic markers are reintroduced via the removal of acyl groups on the surface of histones, thereby reintroducing redundancy to the gene regulatory network. 

I highlight more examples like this in my review of [Bioelectricity as an upstream causal factor in aging]({{< ref "bioelectricityaging" >}}).

**What else I'm doing now:**
- Familiarizing myself with [BETSE](https://github.com/betsee/betse) in order to model the above hypothesis in silico and eventually in vivo. 
- Learning non equilibrium approaching thermodynamics
- Learning non linear control theory

*I am putting this out as a calling card, not an etching in stone. Please, if you have input, feedback—critical or otherwise, or are interested in collaborating, [send me a note](mailto:me@benjaminbanderson.com).*

It's **time** to build. 

---

### Citation
In academic work, please cite this essay as:

_Anderson, Benjamin, “The Free Energy Theory of Aging”, TheBenjam.in (2022-09-05), available at https://www.thebenjam.in/research/._

---

### Changelog
*September 7, 2022* — Expanded the ending discussion on intracellular signalling-dependent transcription and added a new citation. 

*September 22, 2022* — Altered opening. Added a new citation. 

[^1]: Maxwell James Désormeau Ramstead, Paul Benjamin Badcock, Karl John Friston, Answering Schrödinger's question: A free-energy formulation, Physics of Life Reviews, Volume 24,2018, Pages 1-16, ISSN 1571-0645,
https://doi.org/10.1016/j.plrev.2017.09.001

[^2]: Andrews, M. The math is not the territory: navigating the free energy principle. Biol Philos 36, 30 (2021). https://doi.org/10.1007/s10539-021-09807-0

[^3]: Anderson, Benjamin, “Causal Emergence in Biological Networks”, TheBenjam.in (2022-07-23), available at https://www.thebenjam.in/research/.

[^4]: Comolatti, Renzo & Hoel, Erik. (2022). Causal emergence is widespread across measures of causation. 

[^5]: Erik Hoel & Michael Levin (2020) Emergence of informative higher scales in biological systems: a computational toolkit for optimal prediction and control, Communicative & Integrative Biology, 13:1, 108-118, DOI: 10.1080/19420889.2020.1802914

[^6]: Klein, Brennan & Hoel, Erik. (2020). The Emergence of Informative Higher Scales in Complex Networks. Complexity. 2020. 1-12. 10.1155/2020/8932526. 

[^7]: Varley Thomas F. and Hoel Erik 2022 Emergence as the conversion of information: a unifying theoryPhil. Trans. R. Soc. A.3802021015020210150
http://doi.org/10.1098/rsta.2021.0150

[^8]: Lipsitz LA, Goldberger AL. Loss of 'Complexity' and Aging: Potential Applications of Fractals and Chaos Theory to Senescence. JAMA. 1992;267(13):1806–1809. doi:10.1001/jama.1992.03480130122036

[^9]: Friston Karl, Levin Michael, Sengupta Biswa and Pezzulo Giovanni 2015 Knowing one's place: a free-energy approach to pattern regulation J. R. Soc. Interface. 12: 20141383. 20141383 https://doi.org/10.1098/rsif.2014.1383

[^10]: Tseng, A.-S. and Levin, M. (2012), Transducing Bioelectric Signals into Epigenetic Pathways During Tadpole Tail Regeneration. Anat Rec, 295: 1541-1551. https://doi.org/10.1002/ar.22495