---
layout: default
title: Dead Volume in ddPCR
parent: Basics
nav_order: 4
has_children: true
---
# Dead Volume in ddPCR

Dead volume is a concept that refers to the volume of the final sample input (in most Bio-Rad systems, e.g., QX200 or QX600, final input volume is either 20 uL (with manualDG) or 22 uL (with AutoDG)) that is lost (or otherwise goes unmeasured) by the end of the ddPCR analysis workflow. Typically, we assume that this occurs because some of the volume of the sample is not converted into analyzable droplets.

That is to say, if the final sample volume is 20 uL and the dead volume is approximately 15%, we can expect roughly 3 uL (out of 20) to be lost or unaccounted for by the time the sample undergoes the analysis. While this obviously affects the copy number measurements, it is important to stress that no system has the dead volume of 0%.

A great study showcasing the dead volume comparisons between different digital PCR systems is that by [Pitton et al., 2025](https://academic.oup.com/jambio/article/136/10/lxaf243/8266528?login=false), wherein the authors demonstrate the clear superiority of the Bio-Rad's QX AutoDG systems in terms of conserving the precious sample input in stark contrast to both Qiagen's QiAcuity and Stilla's older Naica systems.

![deadvol.jpeg](Dead%20volume/deadvol.jpeg)\
*source: [Pitton et al., 2025](https://academic.oup.com/jambio/article/136/10/lxaf243/8266528?login=false), Figure 4*
