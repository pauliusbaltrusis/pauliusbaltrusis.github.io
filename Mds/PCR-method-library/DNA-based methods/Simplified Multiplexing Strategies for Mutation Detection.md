# Simplified Multiplexing Strategies for Mutation Detection

Owner: Paulius Baltrušis

When detecting multiple mutations, the conventional approach involves designing **mutation-specific probes**, each tagged with a distinct fluorophore (e.g., FAM, HEX). These probes are engineered to bind uniquely to sequences with specific mutations or wild-type alleles. In a single ddPCR reaction, different fluorophore signals correspond to different mutations. However, this method is limited by the number of fluorescent channels available in the ddPCR system.

If the goal is to identify whether *any* mutation is present without specifying which one, a simpler approach can be used:

- **Multiple Probes with the Same Fluorophore**: Design several probes (closely located within the same amplicon and flanked by a single primer pair) targeting different mutations. All probes are labeled with the same fluorophore (e.g., FAM). In this setup, a signal in the fluorophore’s channel indicates the presence of at least one mutation, but the specific mutation responsible is not determined.

This strategy is used in [Bio-Rad’s ddPCR KRAS G12/G13 Screening Kit]([https://www.bio-rad.com/en-se/sku/1863506-ddpcr-kras-g12-g13-screening-kit?ID=1863506](https://www.bio-rad.com/en-se/sku/1863506-ddpcr-kras-g12-g13-screening-kit?ID=1863506)), which detects seven SNPs in the KRAS gene at codons 12 and 13. The kit employs a set of primers and multiple probes, all labeled with FAM, to identify whether any of the SNPs are present. However, it does not distinguish between individual SNPs. The part A of the illustration below demonstrates this approach.

Another alternative is the **drop-off probe strategy**: The drop-off probe targets a mutation-prone hotspot and is complementary to the wild-type sequence. If a mutation disrupts the probe-binding site, the probe cannot hybridize, leading to a "drop-off" in fluorescence. A positive signal indicates the absence of mutations, while a drop-off suggests the presence of one or more mutations in the hotspot.

This approach requires only one fluorophore and is particularly effective for screening mutation-prone regions. An example is shown in **B**.

*source:*

Both strategies enable efficient screening for mutations in a hotspot without the need for:

- Extensive optimization to differentiate fluorescence clusters for each mutation.
- Running multiple reactions with distinct primer-probe sets.
    
    ![simplified multiplex.png](Simplified%20Multiplexing%20Strategies%20for%20Mutation%20De%201261bbe397bb802cbd5ec0b73d5c89b7/simplified_multiplex.png)
    

These methods are ideal for identifying the presence of *any* mutation in a hotspot when the specific identity of the mutation is less critical, such as in initial screening workflows. For a reference study, check out *[Decraene et al., 2018]([https://pubmed.ncbi.nlm.nih.gov/29122835/](https://pubmed.ncbi.nlm.nih.gov/29122835/))*