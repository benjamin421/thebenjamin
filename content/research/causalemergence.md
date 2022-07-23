---
title: "Causal Emergence in Biological Networks"
date: 2022-07-23
draft: false
description: "What is the role of redundancy in gene regulatory networks, and how does it change over time and between species?"
slug: "causal-emergence-biological-networks"
subjects: ["Emergence", "Network Theory", "Aging"]
showDate: false
showHeadingAnchors: true
showAuthor: true
showReadingTime: false
showEdit: true
showSummary: true
showPagination: true

---

{{< lead >}}
Last updated — July 2022 | What is the role of redundancy in gene regulatory networks, and how does it change over time and between species?
{{< /lead >}}

## Overview
Causal Emergence is the conversion of redundant information to synergistic information.[^1] The below effects of course graining existing networks denotes a decrease in the uncertainty of state transitions across the networks. A promising area for continued exploration would be in the seeking of highly causal pathways/Markov chains across these networks that then serve to be extrapolated back down to original scale and perterbed to determine effects of intervention.[^2] Alternatively, these causal pathways can be enhanced with a literature search to determine corrolary phenotypes tied to involved genes and proteins. 

A key idea that I am exploring here is the role of redundancy in networks, and how it changes over time, especially in gene regulatory networks. My vague hypothesis is that as a byproduct of aging, redundant pathways in the GRNs of our cells are slowly erased through the build-up of epigenetic markers, serving to block certain interactions as a means of adhering to the free energy principal. 

An unaswered question I have in this regard is the direction of causality for promoting this build-up. It has been shown that there is a direct correlation between epigenetic markers and the regulation of intercellular communication through ion channels and gap junctions[^3],[^4],[^5], however it is unknown—_at least to me at present_—whether the buildup of these markers are themselves a downstream process effected by intercellular communication through these channels. This would imply that they serve as a feedback loop to eachother, wheras if the promotion of buildup was being prompted at the GRN/DNA level exclusively, then the changes in intercellular communication over time related to epigenetic marker buildup would be exclusively downstream of GRN interactions, and not causal. 

Intuition tells me that a feedback mechanism between the 2 is at play, and there is probably a more complicated answer than the two simplistic models that I have outlined above. For the sake of thinking about where to intervene however, I seek to answer the question of which is _more_ causal to the other. 

---
### What I'm doing
1. Use provided list of GenAge Genes from [here](https://genomics.senescence.info/download.html) for base gene dataset.
2. Use [STRING](https://string-db.org/cgi/input?sessionId=brdWSUC1G4au&input_page_show_search=off) to create a graph of these genes and their pathways with wieghted edges. 
3. Use [this package](https://github.com/jkbren/einet) to determine effective information for this graph[^6]: 
{{< highlight html "linenos=table,hl_lines=5" >}}
from ei_net import effective_information
import networkx as nx
import numpy as np 
G = nx.GRAPH()  
EI_micro = effective_information(G)   
print("EI micro: %.6f"%EI_micro)
{{< /highlight >}}
4. Create a macro graph using the same package. More details on how to do this [here](https://besjournals.onlinelibrary.wiley.com/doi/10.1111/2041-210X.13805).
5. Return difference between effective information across 2 graphs as well as e:
{{< highlight html "linenos=table,hl_lines=1" >}}
eff_gain = (EI_macro-EI_micro)/np.log2(N)
print("Effectiveness gain: %.6f"%eff_gain)
Effectiveness gain: {VALUE}
{{< /highlight >}}
6. Repeat until no more macro nodes are found. 

---

## Before:

![Image of initial human gene network](/img/original.png)
_Human — Aging, Original_

## After:

![Image of iteration 7 from human gene network](/img/v7.png)
_Human — Aging, Iteration 7_

---
# Results from GenAge Dataset

## Humans — Aging

**Initial Effectiveness: 0.335729**

| Run                                | Nodes               | Edges               |Effective Information               | Effectiveness Gain               | 
| ---------------------------------------| ----------------------| ----------------------|----------------------| ----------------------|
| Original   | 306   | 7862 | 2.7722478691230394 | N/A |
| 1   | 215   | 6730 | 2.8410909848914425 | 0.008337 |
| 2   | 188   | 5574 | 2.850469 | 0.009473 |
| 3   | 188   | 5148 | 2.852802 | 0.009755 |
| 4   | 177   | 4645 | 2.855296 | 0.010057  |
| 5   | 163   | 3913 | 2.860143 | 0.010644  |
| 6   | 144   | 2960 | 2.860143 | 0.010644  |
| 7   | 136   | 2620 | 2.874134 | 0.012339  |

**Final Effectiveness:  0.405523737036814**

## Humans — Senescence

**Initial Effectiveness: 0.486386**

| Run                                | Nodes               | Edges               |Effective Information               | Effectiveness Gain               | 
| ---------------------------------------| ----------------------| ----------------------|----------------------| ----------------------|
| Original   | 259   | 2585 | 3.899266239854304 | N/A |
| 1   | 184   | 2355 | 3.99960383896453 | 0.012516 |
| 2   | 180   | 2262 | 4.002437 | 0.012869 |
| 3   | 176   | 2155 | 4.003378 | 0.012987 |
| 3   | 174   | 2066 | 4.004505 | 0.013127 |

**Final Effectiveness:  0.53802705908**

---
If an intervention works for a macronode, with 2 different internal causal pathways, then we may be able to identify more fine grained interventions: 

>Additionally, what nodes get grouped into a macro-nodes tells us what interventional targets are meaningful within the system. Consider that of the two macro-nodes in the system {μ1, μ2}, each requires the activation of exogenous canWnt II. However, their set of underlying nodes are differentiated solely by the concurrent activation of Foxc1_2, which is not upregulated in μ1 and is upregulated in μ2. This tells us that it is solely Foxc1_2, rather than any other element in the network, that determines which causal path the network takes as long as exogenous canWnt II is activated. The macro-nodes capture which differences are actually relevant to the intrinsic workings of the system itself.
cc: https://www.tandfonline.com/doi/full/10.1080/19420889.2020.1802914

---
## Mus Musculus (Mouse)

**Initial Effectiveness: 0.434615**

| Run                                | Nodes               | Edges               |Effective Information               | Effectiveness Gain               | 
| ---------------------------------------| ----------------------| ----------------------|----------------------| ----------------------|
| Original   | 130   | 1056 | 3.0520255784285086 | N/A |
| 1   | 92   | 928 | 3.133283 | 0.011571 |
| 2   | 86   | 803 | 3.138779 | 0.009473 |
| 3   | 83   | 767 | 3.139050 | 0.012392 |

**Final Effectiveness: 0.48975792415**

---

## Drosophila (Fruit Fly)

**Initial Effectiveness: 0.546897**

| Run                                | Nodes               | Edges               |Effective Information               | Effectiveness Gain               | 
| ---------------------------------------| ----------------------| ----------------------|----------------------| ----------------------|
| Original   | 187   | 1303 | 4.127372843455749 | N/A |
| 1   | 128   | 930 | 4.294786 | 0.022183 |
| 2   | 122   | 853 | 4.29722214296244 | 0.022506 |
| 3   | 83   | 767 | 3.139050 | 0.012392 |

**Final Effectiveness: 0.62002380607**

---

## Caenorhabditis elegans

**Initial Effectiveness: 0.559496**

| Run                                | Nodes               | Edges               |Effective Information               | Effectiveness Gain               | 
| ---------------------------------------| ----------------------| ----------------------|----------------------| ----------------------|
| Original   | 825   | 10655 | 5.420533831393049  | N/A |
| 1   | 620   | 9491 | 5.567058824717181 | 0.015124 |
| 2   | 611   | 853 | 5.568796385519166 | 0.015303 |
| 3   | 609   | 9450 | 5.569021173547727 | 0.015327 |

**Final Effectiveness: 0.602037**

---
## Saccharomyces cerevisiae (Incomplete)

**Initial Effectiveness: 0.535618**

| Run                                | Nodes               | Edges               |Effective Information               | Effectiveness Gain               | 
| ---------------------------------------| ----------------------| ----------------------|----------------------| ----------------------|
| Original   | 931   | 14689 | 5.282608841216231  | N/A |
| 1   | 761   | 15840 | 5.408062463177776 | 0.012720 |


**Final Effectiveness: 0.565002**

---


### Open Questions / Areas to Explore
1. **Causal emergence difference in other portions of the total GRN network.** 

Due to data/computational constraints, I have defaulted to examining causal emergence in a series aging phenotype networks in different species.

2. **Find out where to get data for and how to model bioelectric communication networks to then course grain for causal emergence.**  
 
The challenge in doing this to compare results to an analysis at the GRN level is that the effective information returned at the bioelctric network scale would be a far broader representation of uncertainty in state change than the single cell phenotype network. 

- One solution to compare these 2 scales effectively may be to continue exploring causal emergence in different GRNs for different phenotypes across species, and create some sort of index of the average changes in causal emergence across all these different GRNs to then compare to results at the intercellular communication network scale. 
    
- Over time, as this index would grow, it could be used as a new tool for discovering novel points with which to anchor bioelctric networks to downstream transcriptional effects. 

- **Currently diving into [BETSE](https://github.com/betsee/betse) to accomplish this.**

---

## To Do
1. Run against human and mouse genes from different dataset: https://ngdc.cncb.ac.cn/aging/age_related_genes
2. Rerun against yeast genes from GenAge dataset 
3. Test Resilience and Prospective Resilience of all generated networks: https://github.com/jkbren/presilience

---

## Tools 
Greedy Algorithm for identifying subgraphs: https://github.com/jkbren/einet

>The greedy algorithm used for finding causal emergence in networks is structured as follows: for each node, vi, in the shuffled node list of the original network, collect a list of neighboring nodes, {vj} ∈ Bi, where Bi is the Markov blanket of vi (in graphical models, the Markov blanket, Bi, of a node, vi , corresponds to the “parents,” the “children,” and the “parents of the children” of vi). *This means that {vj} ∈ Bi consists of nodes with outgoing edges leading into 10 Complexity vi, nodes that the outgoing edges from vi lead into, and nodes that have outgoing edges leading into the out-neighbors of vi. For each node in {vj} , the algorithm calculates the EI of a macroscale network after vi and vj are combined into a macronode, vM. If the resulting network has a higher EI value, the algorithm stores this structural change and, if necessary, supplements the queue of nodes, {vj}, with any new neighboring nodes from vj’s Markov blanket that were not already in {vj}. If a node, vj, has already been combined into a macronode via a grouping with a previous node, vi , then it will not be included in new queues, {vj }′ , of later nodes to check. *The algorithm iteratively combines such pairs of nodes until every node, vj, in every node, vi’s Markov blanket, is tested.

Protien and gene regulatory interaction db: https://string-db.org/

---

### Data Availability
Aging Genes for Multiple Species: https://genomics.senescence.info/genes/index.html

Senescence Genes for Humans: https://genomics.senescence.info/cells/

---

### Citation
In academic work, please cite this essay as:

_Anderson, Benjamin, “Causal Emergence in Biological Networks”, TheBenjam.in (2022-07-23), available at https://www.thebenjam.in/research/._

[^1]: Varley Thomas F. and Hoel Erik 2022 Emergence as the conversion of information: a unifying theory _Phil. Trans. R. Soc. A._ 380: 20210150.20210150
[^2]: Brennan Klein, Erik Hoel, Anshuman Swain, Ross Griebenow, Michael Levin, Evolution and emergence: higher order information structure in protein interactomes across the tree of life, Integrative Biology, Volume 13, Issue 12, December 2021, Pages 283–294, https://doi.org/10.1093/intbio/zyab020
http://doi.org/10.1098/rsta.2021.0150
[^3]: Masahito Oyamada, Kumiko Takebe, Yumiko Oyamada,
Regulation of connexin expression by transcription factors and epigenetic mechanisms, Biochimica et Biophysica Acta (BBA) - Biomembranes,
Volume 1828, Issue 1, 2013, Pages 118-133, ISSN 0005-2736,
https://doi.org/10.1016/j.bbamem.2011.12.031.
[^4]: Tseng, A.-S. and Levin, M. (2012), Transducing Bioelectric Signals into Epigenetic Pathways During Tadpole Tail Regeneration. Anat Rec, 295: 1541-1551. https://doi.org/10.1002/ar.22495
[^5]: Pai, V. P., Martyniuk, C. J., Echeverri, K., Sundelacruz, S., Kaplan, D. L., & Levin, M. (2015). Genome-wide analysis reveals conserved transcriptional responses downstream of resting potential change in Xenopus embryos, axolotl regeneration, and human mesenchymal cell differentiation. Regeneration (Oxford, England), 3(1), 3–25. https://doi.org/10.1002/reg2.48
[^6]: Klein, B., Swain, A., Byrum, T., Scarpino, S. V. & Fagan, W. F. (2022). Exploring noise, degeneracy and determinism in biological networks with the einet package. Methods in Ecology and Evolution, 13, 799– 804. https://doi.org/10.1111/2041-210X.13805