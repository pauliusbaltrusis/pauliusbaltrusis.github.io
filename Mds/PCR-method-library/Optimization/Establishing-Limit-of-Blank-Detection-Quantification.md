# Establishing Limit of Blank/Detection/Quantification for your assay

Owner: Paulius Baltrušis

To ensure the robustness and reliability of your ddPCR assay, it is critical to define and validate key analytical parameters, such as the **Limit of Blank (LoB)**, **Limit of Detection (LoD)**, and **Limit of Quantification (LoQ)**. These metrics are foundational for accurate assay interpretation, particularly in applications such as rare mutation detection, pathogen quantification, or low-abundance target analysis.

This brief entry provides step-by-step guidelines for determining these limits, following general best practices. Let’s begin with some definitions first:

- **Limit of Blank (LoB):** The highest apparent concentration of target sequence measured in a sample that does not contain the target sequence (NTC). LoB establishes the assay’s background signal (and the presence of any false positive(s)).
- **Limit of Detection (LoD):** The lowest concentration of the target sequence that can be reliably distinguished from the LoB, with a predefined probability of detection.
- **Limit of Quantification (LoQ):** The lowest concentration of the target sequence that can be quantified with acceptable, predetermined variance, or coefficient of variation (CV*) (e.g. 20%).

In order to establish **LoB**, do the following:

1. Run your ddPCR assay with (e.g., 20) NTC replicates
2. Calculate the **LoB** using the formula:

LoB=mean(NTC)+1.645×SD(NTC)

Where:

- mean - Mean target concentration in NTC (blank) replicates.
- SD - Standard deviation of target in NTC (blank) replicates.

For the **LoD**, the following can be done:

1. Since, LoD is calculated by utilizing the measured LoB and testing replicates with a low concentration of the target, you can create serial dilutions of the target sequence (using a positive control, e.g. gBlock) around the anticipated LoD. Make sure to include at least 3 concentrations near the threshold and run multiple replicates (e.g., 20).
2. Calculate the LoD using the formula below:

LoD = LoB + 1.645(SD low concentration of target)

Where:

- LoB - previously established LoB for this assay
- SD low concentration of target - standard deviation in samples with low concentrations of the target sequence

For the **LoQ**, you can do this:

1. The LoQ can range from being equivalent to the LoD to a much higher concentration value but is never lower than the LoD. Using the previous dilution experiment to establish the LoD, you can identify the concentration at which the precision, typically expressed as CV*, is equal or below to a predetermined value - e.g., 20%. 

*CV is calculated (for each dilution) by dividing the standard deviation by the mean concentration of the target sequence in your replicates. For example, let’s imagine that for dilution X, you consistently get around 10 copies/ul of the target sequence. Your standard deviation is 0.4 copies/ul. Then, CV (%) = (0.4/10) * 100% = 4 %.

The image below summarizes the differences between **LoB**, **LoD** and **LoQ** and what each of these parameters represent. For more info, you can also refer to this [Bio-Rad Bulletin 7183 Ver A]([https://dna.uga.edu/wp-content/uploads/sites/51/2021/03/Droplet-Digital-PCR-Guide.pdf](https://dna.uga.edu/wp-content/uploads/sites/51/2021/03/Droplet-Digital-PCR-Guide.pdf)).

![image.png](Establishing%20Limit%20of%20Blank%20Detection%20Quantificati%201511bbe397bb80a2b777dddc7d4984c8/image.png)

source: [Bio-Rad Bulletin 3674]([https://www.bio-rad.com/sites/default/files/2024-08/Bulletin_3674.pdf](https://www.bio-rad.com/sites/default/files/2024-08/Bulletin_3674.pdf))