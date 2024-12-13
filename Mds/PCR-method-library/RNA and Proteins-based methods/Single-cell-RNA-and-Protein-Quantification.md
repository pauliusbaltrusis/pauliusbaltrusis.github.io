---
layout: default
title: Single-cell RNA & Protein Quantification
parent: RNA and Protein-based methods
has_children: true
nav_order: 6
---

# Single-cell RNA & Protein Quantification


A impressive method combining digital Proximity Ligation Assay (dPLA) and RT-ddPCR was introduced by [Albayrak et al. 2016](<https://www.cell.com/molecular-cell/fulltext/S1097-2765(16)00174-X>). This approach enables the simultaneous and quantitative measurement of both proteins and mRNA in individual cells, offering an unparalleled level of sensitivity and resolution. By merging these two techniques, the method provides a means to track key biomolecules, which are often co-regulators of cellular function, in a highly sensitive and absolute manner.

![image.png](Single-cell%20RNA%20&%20Protein%20Quantification/image.png)
*source: [Albayrak et al. 2016](<https://www.cell.com/molecular-cell/fulltext/S1097-2765(16)00174-X>)*

**Workflow Overview**

The method starts with single-cell sorting, typically achieved using fluorescence-activated cell sorting (FACS). Each sorted cell is lysed to generate a single-cell lysate, which is subsequently divided into two aliquots for separate analyses:

1. **Digital Proximity Ligation Assay:**
    - Used to detect and quantify individual protein molecules.
    - Oligonucleotide-conjugated antibodies are employed, enabling specific detection at the femtomolar level.
2.  **RT-ddPCR:**
    - Used to measure mRNA expression levels.
    - Ensures absolute quantification of RNA molecules at a single-cell resolution.

Both aliquots are then partitioned into droplets, allowing for absolute quantification and resulting in reliable detection of both RNA and proteins within the same cell.


**Key Findings from the Study**

In their analysis of CD147 expression in mammalian cells, the researchers uncovered several intriguing insights:

- **Protein Production Efficiency:**

    Approximately 1,000 proteins were found to be synthesized from a single mRNA molecule within a single cell.

- **Low Correlation Between mRNA and Protein Levels:**

    The study revealed a surprisingly weak correlation between mRNA and protein abundance within the same cell, challenging traditional assumptions about the tight coupling of transcription and translation. This finding highlights the complexity of post-transcriptional regulation and protein synthesis dynamics.


This dual quantification technique is especially valuable for single-cell analysis, providing a tool to study gene expression and protein synthesis dynamics simultaneously, which is critical for applications in cell biology and even cancer research. The study marks a significant advancement in the ability to perform multiplexed, quantitative single-cell measurements.
