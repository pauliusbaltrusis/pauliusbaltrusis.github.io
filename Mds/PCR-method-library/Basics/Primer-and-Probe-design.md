---
layout: default
title: Primer and Probe design
parent: Basics
nav_order: 5
has_children: true
---
# Primer and Probe design

This chapter focuses on the basics of ddPCR and the tools available to help you design your very own ddPCR assay.

If you'd like to create a simple gene-target detection assay, you'll need:

  - Primer pair sequences
  - (Optional) Probe sequence

For singleplex detection (one target at a time), you can use a DNA intercalating dye like EvaGreen, where probes aren’t necessary, and primers alone suffice. However, for multiplexing, it’s recommended to develop primer-probe pairs from the outset.

**Tools for Primer and Probe Design**

The most well-known online tool for primer sequence development is [Primer3Plus](<https://www.primer3plus.com/index.html>). Paste your target locus sequence, set optimal amplicon sizes (60–200 bp; the shorter the amplicon - the better the reaction efficiency), and ensure:

    - Primer Tm ≤ 65°C
    - GC content: 40–60%
    - Avoid excessive G/C repeats.

Recommended Primer3Plus Settings:

    General Settings:
        - “Concentration of divalent cations” = 3.8 mM
        - “Concentration of dNTPs” = 0.8 mM
        - “Mispriming/Repeat Library” = your organism of interest.
    Advanced Settings:
        - “Thermodynamic parameters” and “Salt correction formula” = SantaLucia 1998.

To start designing primers, you'll need the gene locus sequence. You can find it via genome repositories like [NCBI](<https://www.ncbi.nlm.nih.gov/>) and more specifically [NCBI Genome Browser](<https://www.ncbi.nlm.nih.gov/gdv/?org=homo-sapiens>)

**Primer Design for EvaGreen Assays**

For EvaGreen assays, simply order primers and the correct supermix. Optimize your ddPCR assays (e.g., thermal gradient testing) to ensure specificity and efficiency before using them on *unknown* samples.

**Probe Design for Multiplexing**

If using probes, [Primer3Plus](<https://www.primer3plus.com/index.html>) can generate probe sequences flanked by forward and reverse primers. Make sure to modify the following settings first:

Recommended Primer3Plus Settings:

    Internal Oligo:
        - Set the oligo minimum to 15 bases.
        - Minimum probe Tm = 64°C, optimal Tm = 65°C, maximum Tm = 70°C (relax for high/low GC targets).
        - Oligo size: 13–30 nucleotides.

Also make sure to adhere to these [Bio-Rad-issued guidelines](<https://www.bio-rad.com/webroot/web/pdf/lsr/literature/Bulletin_6407.pdf>):

    - Probe Tm should be 3–10°C higher than primers.
    - GC content: 30–80%. Design probes to favor Cs over Gs.
    - Length: <30 nucleotides (longer probes or Tm enhancers are
    recommended if to achieve the required Tm. I would recommend shorter probes that still satisfy the 1. and 2. points above).
    - Avoid G at the 5’ end (quenches fluorescence).
    - Label probes with compatible fluorophores (e.g., FAM, HEX/VIC = QX200 or FAM, HEX/VIC, Cy5, Cy5.5, ROX and ATTO 590 = QX600) and quenchers (e.g., IOWA BLACK).


**Validating Primer and Probe Sequences**

1. Self-Annealing and Structural Issues:

Use [PCR Primer Stats](<https://www.bioinformatics.org/sms2/pcr_primer_stats.html>) to identify:

- GC clamps
- Self-annealing
- Hairpin formation

A few self-annealing base pairs are manageable, but excessive structures can reduce reaction efficiency.

2. Primer-Dimer Analysis:

Check forward-reverse primer interactions using [Multiple Primer Analyzer](<https://www.thermofisher.com/se/en/home/brands/thermo-scientific/molecular-biology/molecular-biology-learning-center/molecular-biology-resource-library/thermo-scientific-web-tools/multiple-primer-analyzer.html>). Input your sequences in fasta format and adjust:

    - Primer concentration: 900 nM.
    - Probe concentration: 250 nM.
    - Salt concentration: 53.8 mM (50 mM monovalent, 3.8 mM divalent).

This tool provides Tms, self-dimer stats, and other crucial metrics. Ensure primer Tms differ from probes by 3–10°C.

3. SNP Detection Probes Check-up:

For SNP assays, design two probes—one for wild type (e.g., AGG) and another for the mutant (e.g., ACG). Minimize cross-reactivity using [Oligo Analyzer](<https://www.idtdna.com/calc/analyzer>):

  - Input probe sequences individually.
  - Adjust oligo (0.25 μM), Na+ (50 mM), Mg++ (3.8 mM), and dNTP (0.8 mM) concentrations.
  - Click on **TM MISMATCH** (to the right)
  - Scroll down to the bottom, introduce a mismatch of your choosing in the probe sequence and click on **CALCULATE** at the bottom
  - Use Tm mismatches to evaluate the binding specificity of your probes and calculate the delta Tm between them (ideal: ≥2°C).

Place the SNP locus centrally in the probe sequence to maximize the mismatch's effect.

**Bio-Rad Custom Assay Builder**

Simplify evaluations with [Bio-Rad’s Custom Assay Builder](<https://www.bio-rad.com/digital-assays/custom-assay-builder>). Enter your ddPCR platform, supermix, and sequences to receive a suitability report with optimization recommendations.

**Final Steps**

Once designed, ensure your primers and probes:

  - Follow recommended guidelines.
  - Have minimal structural issues (in silico).

Test them in vitro for final validation. This ensures optimal performance before applying them to *unknown* samples.
