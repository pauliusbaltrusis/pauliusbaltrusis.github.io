---
layout: default
title: Basics of quantification & digital PCR assay design
parent: Basics
nav_order: 1
has_children: true
---
# Basics of quantification & digital PCR assay design

**Digital PCR (dPCR)** provides highly precise quantification of nucleic acids. Its core principles involve partitioning a sample into thousands of droplets, each acting as an individual reaction chamber. The dynamic amounts of positive and negative droplets as well as the average volume of the droplets are then used to predict the average target nucleic acid copy number using the Poisson distribution as the model that describes rare event detection.

For example, let’s image our 20 uL sample contains 6 copies of target DNA (gene X) that we want to detect and quantify. If we disperse our sample into a large number of small partitions, assuming the partitioning is **random** and **independent**, this process can be described using a Poisson distribution (see the image below). It does not really matter where the 6 copies of our target gene X end up: whether they all end up in different partitions or all in the same single partition (or something in between), the probability of each of these can be denoted as *p*. Let’s assume that we have 20 000 partitions. Then, since we only have 6 molecules it makes the most sense that they are most likely going to end up in different partitions, since there are so many of them (20 000). Of course, it is theoretically possible that they will all end up in the same partition, but given the sheer and overwhelming amount of the partitions (vs gene X molecules) and the fact that those 6 gene X molecules are floating around in a 20 uL solution (thus likely quite far apart from one another), this is extremely unlikely to be observed. So, if we repeatedly partitioned our 6 molecule sample many times (n times), we would be able to plot the probabilities (”Prob”) of seeing partitions with 0 gene X target molecules (”Copies”) each, 1 gene X molecule each, 2 gene X molecules each, 3, 4, 5 and 6. Perhaps not unexpectedly, most of our droplets after partitioning will be empty. Then, the second most common event will be droplets containing only 1 target X molecule each. Much less frequently we will see droplets containing >1 gene X molecule. Basically what we have now is the distribution describing the probability (or frequency) estimates for discrete events - that is, what’s the frequency of seeing negative droplets, single copy droplets, two copy droplets *etc etc.*

![g2.png](Basics%20of%20quantification%20&%20digital%20PCR%20assay%20design/g2.png)

*An illustration on how sample partitioning and Poisson distribution-based, average copy number per partition determination is carried out (theoretical example)*

Okay, so what of it (you might ask yourself)? Well, what we have just described is a Poisson distribution, and we can calculate it’s single parameter *lambda*, which will be our average copy number per droplet (CPD), using the following, simplified formula:

**𝐶𝑃𝐷=−ln⁡(𝑁_𝑛𝑒𝑔/𝑁_𝑡𝑜𝑡𝑎𝑙 )/𝑉_𝑑𝑟𝑜𝑝𝑙𝑒𝑡** (0.0003 copies/ul in our example case)

Where:

*N_neg - Number of negative droplets*

*N_total - Number of total droplets*

*V_droplet - Average droplet volume*

Using the ratio of the number of negative partitions to all partitions, divided by the average volume of the partition we can easily find the CPD. If we want to know the total number of copies in our initial sample we just multiply our CPD by the total number of partitions observed in that sample (for ddPCR that’s around 20 000):

𝐶𝑜𝑝𝑖𝑒𝑠/(20 𝑢𝑙)=𝐶𝑃𝐷×𝑁_𝑡𝑜𝑡𝑎𝑙 (≈20 000) (0.00003 x 20 ul = 6 copies)

**The most common ddPCR assay types**

**Copy number determination.** dPCR allows for the accurate and absolute quantification of gene (target) copies. One can even contrast and compare the measurements to a reference gene (which can be run in another channel) in order to see any discrepancies in copy number variations, such as gene (target) duplications. This simultaneous quantification of multiple targets within the same reaction is achieved by using sequence-specific hydrolysis probes labelled with different fluorescent dyes. Copy number determination methods are particularly useful in applications like quantifying plasmid copies in gene therapy, multiple (and simultaneous) pathogen detection or assessing gene amplification in cancers.

**Mutation detection.** dPCR is particularly advantageous because it can discriminate between wild-type and mutant alleles with exceptional sensitivity. By designing assays that target specific mutations, one can quantify the fraction of mutant DNA within a heterogeneous sample. This is especially valuable in personalized medicine approaches such as cancer diagnostics, where detecting low-abundance mutations can inform treatment decisions.

See the image below for a simple summary.

![13071_2023_5756_Fig2_HTML.png](Basics%20of%20quantification%20&%20digital%20PCR%20assay%20design/13071_2023_5756_Fig2_HTML.png)

source: [Baltrusis et al., 2023](<https://parasitesandvectors.biomedcentral.com/articles/10.1186/s13071-023-05756-7>)
