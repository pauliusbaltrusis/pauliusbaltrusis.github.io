---
layout: default
title: Stem Loop Primers for miRNA Quantification
parent: RNA and Protein-based ddPCR Methods
has_children: true
nav_order: 8
---

# Stem Loop Primers for miRNA Quantification


miRNAs are short RNA molecules (~20 nucleotides) that pose unique challenges for detection and quantification using PCR. Their small size provides limited binding regions for reverse transcription (RT) primers, complicating the RT step. Additionally, the low melting temperature (Tm) of RT primers can reduce the efficiency of the RT reaction and lead to a low signal-to-noise ratio.

A simple yet elegant solution to overcome miRNA reverse transcription as well as create a detectable and quantifiable (with ddPCR) amplicon is via the use of the Stem Loop Primer(s).

Originally developed for qPCR by [Chen et al., 2005](https://academic.oup.com/nar/article/33/20/e179/1082564), stem loop primers bind to the miRNA via a variable stem structure, while the loop structure is used to stabilize the primer binding (compared to an unbound linear primer tail) and allow for a longer stem loop-miRNA oligo hybrid (once melted) to be used in the following detection & quantification step. Another substantial advantage of the approach is that it does not include an enzymatic (and potentially limiting) ligation step (like in [Ligation Probes for miRNA Quantification](/Mds/PCR-method-library/RNA-and-Protein-based-methods/Ligation-Probes-for-miRNA-Quantification.md)).

A more modern example of a study utilizing stem loop primer based, multiplex ddPCR quantification was conducted by [Busato et al., 2025](https://www.sciencedirect.com/science/article/pii/S0003267024012418), wherein up to 6 miRNAs were RT'ed using stem loop primers and then detected & quantified in a multiplex, simultaneous fashion using a precursor to a QX700 (formely Stilla Naica) system.


![SLP.jpeg](Stem%20Loop%20primers/SLP.jpeg)\
*source: [Chen et al., 2005](https://academic.oup.com/nar/article/33/20/e179/1082564), Figure 1*
