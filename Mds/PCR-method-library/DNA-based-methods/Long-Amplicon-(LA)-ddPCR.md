---
layout: default
title: Long Amplicon (LA) ddPCR
parent: DNA-based ddPCR Methods
has_children: true
nav_order: 5
---

# Long Amplicon (LA) ddPCR

Droplet digital PCR (ddPCR) is primarily designed to amplify and detect short target sequences, with optimal efficiency achieved for amplicons up to ~200 base pairs ([Bio-Rad’s ddPCR applications guide](<https://www.bio-rad.com/webroot/web/pdf/lsr/literature/Bulletin_6407.pdf>). However, longer amplicons can also be successfully amplified and quantified, as demonstrated in multiple studies.

**Case Study 1: Long Amplicon Multiplexing for TP53 Variants**

[Lasham et al., 2020](<https://www.mdpi.com/2072-6694/12/3/769>) quantified seven *TP53* splice variants ranging from 0.85 kb to 1.85 kb and employed amplitude multiplexing to detect multiple isoforms within a single channel. Key insights for success included:

- **High-temperature primers and probes**: Design with melting temperatures ≥60 °C.
- **Double-quenched probes**: Use ZEN™ & Iowa Black™ FQ quenchers to minimize background fluorescence.
- **Optimized cycling protocols**: Test two-step (combined annealing/extension) and three-step (separate annealing and extension) cycling methods to improve fluorescence amplitude.
- **Extended amplification**: Use longer extension times (4–6 minutes) and high cycle numbers (up to 50 cycles) for robust amplification of long targets.

---

**Case Study 2: LaddPCR for Gene-Translocation Detection**

[Krumbolz et al., 2019](<https://onlinelibrary.wiley.com/doi/10.1111/jcmm.14321>) explored long-amplicon ddPCR (laddPCR) to detect gene translocation fusions using amplicons up to 1.33 kb. Their findings reinforced the importance of:

- **Double-quenched probes**: Improved droplet separation and signal clarity.
- **Three-step cycling**: Separate denaturation, annealing, and extension steps provided superior amplification efficiency for long, repeat-rich sequences.

---

**Practical Recommendations**

In summary, for successful detection and quantification of long amplicons (>200 bp):

1. Design primers and probes with high melting temperatures to ensure stability.
2. Use advanced double-quenching strategies to reduce background noise.
3. Experiment with two-step or three-step cycling protocols to optimize signal strength.
4. Test longer extension times and higher cycle numbers to improve amplification of longer targets.

With appropriate optimization, ddPCR can reliably handle amplicons exceeding the conventional 200 bp limit, opening possibilities for detecting complex genetic features like splice variants and gene fusions.
