---
layout: default
title: Control sample types in ddPCR
parent: Basics
nav_order: 3
has_children: true
---
# Control sample types in ddPCR

Arguably the most crucial part of any experiment is the control samples! ddPCR shares a number of similar control sample types with qPCR that should be run at the discretion of the user. I will provide an overview of some of the most common ones:

**Positive Controls**

The purpose of positive control(s) is to verify that the ddPCR assay is working as expected. In addition, positive control(s) can help determine if there’s issues with inhibition, assay design or contamination. For example, for mutation detection assays a positive control would be a fragment of DNA containing the mutation you are expecting to detect, whereas for copy number detection - it would simply be the actual target sequence you are trying to detect.

**Negative Control**

Negative control(s), on the other hand, are there to detect if your assay cross-reacts with an unspecific DNA. This control type essentially challenges your assay’s specificity, or how well your assay performs in a more complex environment where there are multiple types of DNA, not all of which are meant to be detected. So, a sample that lacks the target DNA but contains non-specific DNA, e.g. gDNA from a different species that lacks the targeted locus or wild-type only DNA for mutation detection, can be used. If amplification occurs in this (these) control(s), it indicates unspecific binding by primers/probe(s).

**Negative Template Control (NTC)**

NTCs are there to check for non-specific amplification (sample cross-contamination, extensive primer-dimer formation, etc.) or contamination of the PCR reagents. This control type typically contains all PCR components except for the template DNA (typically buffer or nuclease-free water is added instead). Simply put, NTCs test that the assay does not produce any false positives due to contamination or primer-dimer formation.

**No-RT Control (RNA only)**

No-RT control is generally used in experiments where RNA is reverse-transcribed to cDNA. This control omits the reverse transcriptase enzyme to confirm that the observed amplification is from cDNA and not from contaminating genomic DNA (gDNA). If amplification is detected, it suggests the presence of gDNA in the RNA prep. Although not a very common control type in ddPCR specifically (since the ddPCR supermix for RNA is a 1-step kit), it can be used to estimate the initial contamination with gDNA in your RNA preps if you are running a two-step protocol where you I. reverse transcribe your samples and II. use the generated cDNA as input in your subsequent ddPCR reactions.

**gDNA Control (RNA only)**

Sometimes, however, you might want to spike in some a priori measured quantities of gDNA in your RNA/cDNA preps in order to determine whether your assays can amplify contaminating genomic DNA and thus generate a detectable signal. This control type uses genomic DNA as a template to verify that primers or probes do not cross-react with gDNA, which is especially important in RNA-based assays where only cDNA should be amplified (in e.g. intron-spanning assays).

Both positive and negative controls are really important when taking the first steps in the characterization of your custom assay and become less important as you benchmark and describe your assay. Whereas NTCs are always useful, since they give insight on what background the assay generates when it’s in the mix by itself (without a target) as well as indicating whether or not there is some contamination of reagents. NTCs are also important in the very first runs where you are testing your assay, since this control type is used for the calculation of limit of blank (LoB), limit of detection (LoD) and limit of quantification (LoQ). No-RT control is a rather rare control type but is quite more often used in two-step (especially qPCR) protocols where the goal is evaluate if a new raw sample type (whether it’s a different tissue or different cells, etc.) or a new RNA extraction procedure retains gDNA (which can further generate false-positives) in the RNA preps. gDNA control is similarly a rare control type, which is typically used to generate a yes or no answer to whether or not a cDNA-specific assay can also cross-detect the gDNA spiked in by the user.

By running appropriate controls along side the unknown samples you will have a much easier time telling what’s positive and what’s negative.

Some of the more advanced control types that can effectively answer questions related to the efficiency of your ddPCR are the following:

**Cell (Containing the Target) Spike-In**

The purpose of this spike-in is to validate the detection of the target in a complex sample matrix, such as a biological sample (It can also serve as a positive control for gDNA/pDNA/RNA).

Typically, a known number of cells that contain the target sequence are added (spiked) into the sample either before or after the nucleic acid extraction. If added prior to nucleic acid extraction, this spike-in can serve to estimate the efficiency of the extraction and the accuracy of the subsequent detection. If the target containing cells are spiked in in the pre-ddPCR samples, this type of control will test if the assay can accurately detect and quantify the target in the presence of cellular material, allowing you to monitor potential issues such as poor lysis efficiency or sample handling errors.

**Known RNA Spike-In Prior to One-Step RT-ddPCR**

The purpose of this control is to monitor the efficiency of RNA extraction, reverse transcription, and PCR amplification.

Generally, a known quantity of external RNA is spiked into the sample before either the RNA extraction and/or one-step reverse transcription (RT) and ddPCR process. This control evaluates the efficiency of RNA extraction and reverse transcription, confirming that these processes were successful and (relatively) free of inhibitors.

**DNA Spike Prior to DNA Extraction (Extraction Spike-In)**

The simple purpose here is to assess the efficiency of the DNA extraction process.

To achieve that, a known amount of DNA is spiked into the sample before DNA extraction. This control allows you to determine how much DNA was recovered after extraction, helping to evaluate whether the extraction method is efficient and if there was any loss of DNA during the process.

**PCR Efficiency/Quantification Spike-In (Inhibition Determination)**

The goal behind this control type is to assess PCR efficiency and detect any potential inhibitors in the sample that could affect amplification.

For this, a known quantity of a control sequence (often synthetic) is added to the PCR reaction. This control checks the efficiency of the PCR process and reveals if any components in the sample are inhibiting amplification. A reduced or absent signal from the spike-in suggests the presence of inhibitors, which could lead to inaccurate quantification of the target sequence.

Although these control types are generally run more rarely, they can uncover potential issues with either sample handling or the inhibition/lower-efficiency of upstream enzymatic reactions.
