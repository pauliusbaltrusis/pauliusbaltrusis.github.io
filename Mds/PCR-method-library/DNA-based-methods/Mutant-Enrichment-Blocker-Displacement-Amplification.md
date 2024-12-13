---
layout: default
title: Mutant enrichment via Blocker Displacement Amplification
parent: DNA-based ddPCR Methods
has_children: true
nav_order: 6
---

# Mutant enrichment via Blocker Displacement Amplification

Blocker Displacement Amplification (BDA) is a technique used to selectively enrich and amplify rare DNA variants, particularly those present at very low frequencies in a sample. The method was first reported in a study by [Wu et al., 2017](<https://www.nature.com/articles/s41551-017-0126-5>). The method was developed to address the challenges of detecting rare mutations in the presence of overwhelming wild-type DNA, a common issue in applications such as cancer liquid biopsies and low-frequency genetic variant analysis.

BDA operates by using a blocker oligonucleotide and a unique amplification strategy. The blocker oligonucleotide is designed to bind to wild-type sequences with high specificity, preventing their amplification during the PCR process. These blockers are not amplified themselves (due to blocked 3’ end), but they efficiently block the extension of wild-type templates by the DNA polymerase. Meanwhile, the temperature-robust design of BDA allows for precise discrimination between wild-type and mutant sequences even in challenging regions of the genome, such as those with high GC content or complex secondary structures.

The key innovation of BDA is its ability to selectively amplify mutant sequences while suppressing the wild-type sequences. As the wild-type DNA is effectively "blocked" by the oligonucleotides, the amplification process focuses on the rare mutant sequences. This results in a significant enrichment of rare variants, improving their detectability by more than 100-fold. In their initial study [Wu et al., 2017](<https://www.nature.com/articles/s41551-017-0126-5>) designed the blocker oligo to selectively “displace” one of the primers (based on the presence or absence of any mutation within the binding site of the blocker), thus dampening the amplification of the wt-allele and enriching the amplification of sequences containing mutations in the site where the blocker binds.

The BDA technique was not only shown to detect rare variants with high sensitivity and be temperature robust but also have the capacity to be multiplexed and thus detect multiple variants at the same time, at several loci in the genome.

See the image below for a general overview of the BDA approach to wild-type amplification suppression (left) and mutant/variant sequence enrichment (right).

![BDA.png](Mutant%20enrichment%20Blocker%20Displacement%20Amplificati/BDA.png)

*BDA mediated suppresion of WT template amplification and MT template amplification enrichment*
