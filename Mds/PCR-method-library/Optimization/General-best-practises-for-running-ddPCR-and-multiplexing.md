---
layout: default
title: General best practises for running ddPCR and multiplexing
parent: Optimization
nav_order: 3
has_children: true
---

# General best practises for running ddPCR and multiplexing


**Multiplexing** in droplet digital PCR (ddPCR) allows you to simultaneously detect multiple targets in a single reaction, saving time and reagents while increasing throughput. However, successful multiplexing requires careful optimization, as it introduces complexities in primer/probe design and reaction conditions. The more in-depth guide to which experiments you should consider running after just having received your primers and probes you’ll find in [Optimization: Singleplex Multiplex ddPCR Reaction Optimization](/Mds/PCR-method-library/Optimization/Singleplex-Multiplex-ddPCR-Reaction-Optimization.md). Here’s just a few major points to consider when planning to run multiplex ddPCR experiments:

**Primer and Probe Design**

- **Target Specificity is important**: In order to ensure that each primer/primer-probe set specifically targets its intended sequence without cross-reacting with other targets in the mix, it’s always a good idea to use *in silico* tools to confirm e.g. that your primers are sequence-specific. The simplest of such tools - [NBLAST](<https://blast.ncbi.nlm.nih.gov/Blast.cgi>) can be used to blast your primer sequences against your organisms’ genome. In an ideal case, either only a single hit is obtained for your primer pair, or, at the very least, the first (and most specific) hit for each primer have significantly lower *E-values* compared to subsequent, unspecific (likely partial) hits.
- **Avoid Primer-Dimer Formation**: Make sure you design primers with similar annealing temperatures (ideally within ±1°C or up to ±3°C) to reduce off-target binding, amplification and minimize dimer formation.
- **Probes should be compatible**: This one is rather simple but, nevertheless, make sure you use probes labeled with distinct fluorophores (e.g., FAM, HEX, VIC) for each target (unless you are amplitude multiplexing) to allow discrimination in different fluorescence channels. Keeping in mind, different systems are calibrated for different fluorophores!
- **Choose Optimal Primer&Probe Length and GC Content**: In most cases, primers should be 18-25 nucleotides, and probes should be 20-30 nucleotides, with balanced GC content (40-60%). This helps maintain specificity and efficient binding under multiplex conditions. This is not to say that higher or lower GC contents or primer/probe lengths will not work - they likely will, but it’s best to stick to pre-established guidelines to ensure the least amount of optimization is necessary.

**Reaction Conditions**

- **Test Different Magnesium Concentrations**: Magnesium ions are important for polymerase activity and target binding. These ions become particularly important when conducting higher order multiplexing reactions, in order to ensure the polymerase enzymes are working at full capacity. You can test magnesium concentrations in increments (e.g., 3-5 mM) to optimize amplification efficiency.
- **Test Different dNTP Concentrations**: Similar to magnesium ions. dNTPs are the building blocks for the generation of target amplicon products and an excess of each dNTP ensures the polymerase is saturated and thus working at full capacity. Ensure the final concentration of dNTPs is optimized (especially for high order multiplexing reactions; eg., 0.2-0.25 mM of each dNTP).
- **Adjust the Thermal Cycling Parameters**: Start with the standard ddPCR cycling protocol, then adjust annealing/extension times and temperatures. Gradually increasing the extension time can enhance amplification for longer or GC-rich targets. Slighly higher cycle number (eg. 40→45) and/or lower ramp rate (1.5 degrees/s→2.0 degrees/s) can aid in reducing the amount of “rain” observed. In addition to cycle number and ramp rate, [Ip et al., 2024](<https://www.nature.com/articles/s41598-024-57016-y>) has presented evidence that increasing the denaturation temperature (94→96) helps resolve “rainy” clusters. For particularly long amplicon quantification (>1kbp) I suggest checking the entry on [Long Amplicon(LA) ddPCR)]().
- **Try some PCR Additives**: Sometimes, PCR additives like betaine, DMSO or DTT can help stabilize enzymes complexes or denature secondary structures, especially in GC-rich regions. If needed, titrate to the lowest effective concentration.

Typically, the above 4 reaction conditions do not need to be tested (unless making a proprietary/in-house PCR blend or working with long amplicons) and instead you can order a different supermix - one that’s intended for higher order multiplexing and contains higher final concentrations of ions, dNTPs and the polymerase.

**Droplet Formation and Stability**

- **Avoid Surfactants, Detergents and Carriers that Interfere with Droplets**: This is not multiplexing specific, but something that’s worth keeping in mind. It is a good idea to ensure that you have no (excessive) amounts of aggressive contaminants in your reaction mix that can destabilize droplets, as this can result in “leakage” (otherwise known as droplet shredding). In my 4,5 year-experience running ddPCR experiments, I have not observed any significant droplet shredding, even when directly running tissue lysates. That being said, excessively high concentrations of lysis agents can potentially result in reaction inhibition and/or droplet destabilization and should be avoided.

**Fluorescence Signal Separation**

- **Optimize Signal Intensity**: Although not conventionally necessary, probe (and primer, for that matter) concentration(s) can be adjusted for each target. Start with around 250 nM for each probe (900 nM - each primer), and adjust if needed. Typically, probes are run at 250 nM, while primers - at 900 nM. These can be adjusted to increase the cluster separation (positive from negative), especially when performing [amplitude multiplexing](/Mds/PCR-method-library/Basics/Amplitude-multiplexing.md).

**Validation and Optimization**

- **Run Singleplex Controls**: Before multiplexing, confirm each primer/probe set performs well in singleplex ddPCR to establish a baseline for efficiency and threshold setting.
- **Titrate Each Component in Multiplex**: After singleplex reaction optimization, run reactions with varying concentrations of primers and probes to find a balance where each target is effectively amplified and sufficient separation is obtained. Alternatively, stick to the working, pre-optimized primer and probe concentrations (that is 900 nM/250 nM for each primer/probe, respectively).
- **Check for Interference and Inhibition**: Run multiplex reactions with varying amounts of each target to test for competitive inhibition among targets. Spike-ins of different template types and amounts could be e.g. Template_1 100% + Template 2 10%/20%/40%/80%/100%. This may require iterative adjustments.
- **Set Appropriate Thresholds**: ddPCR allows for digital quantification, so define clear thresholds based on singleplex data (and ideally by running both positive and negative controls) to identify positive and negative droplets in each channel.

If you’d like a more in-depth guide to optimization, I have a created a short summary based on a paper by [Rowlands et al., 2019](<https://www.nature.com/articles/s41598-019-49043-x>) here: [Singleplex Multiplex ddPCR Reaction Optimization](/Mds/PCR-method-library/Optimization/Singleplex-Multiplex-ddPCR-Reaction-Optimization.md).

**Analysis and Data Interpretation**

- **Assess Cluster Quality**: In multiplex ddPCR, droplets should form distinct clusters (or “clouds”) for each target based on fluorescence intensity. Should you observe overlapping clusters, you may want to further optimize primer/probe concentrations or cycling parameters (eg., annealing temperature, ramp rate, extension time).
- **Assess thresholding using controls:** Use single-target (alternatively multiple-target) controls to correctly determine the threshold cut-offs for separating positive droplets from negative.

By following these steps and systematically optimizing each variable, you can achieve robust, reliable (singleplex/multiplex) ddPCR reactions for accurate quantification of (multiple) targets in your reaction setup.
