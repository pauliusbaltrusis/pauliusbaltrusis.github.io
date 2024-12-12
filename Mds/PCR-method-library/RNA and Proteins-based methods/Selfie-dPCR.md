# Selfie-dPCR

Owner: Paulius Baltrušis

The **Selfie digital PCR** approach, as described by [Podlesniy and Trullas, 2017]([https://www.nature.com/articles/s41598-017-08270-w](https://www.nature.com/articles/s41598-017-08270-w)), is a great method for absolute quantification of RNA transcripts (messenger RNA or other classes) relative to their encoding gene. This technique enables the direct calculation of the average number of RNA molecules transcribed per gene copy within a sample, making it an excellent tool for studying gene expression dynamics and transcriptional burst kinetics.

---

**How Selfie dPCR Works**

The process involves lysing cells from a sample to produce a rough lysate containing both genomic DNA (gDNA) and RNA. The lysate is then split into two duplicates:

1. **RT- Sample:** Contains the lysate but no reverse transcriptase, allowing quantification of only gDNA copies.
2. **RT+ Sample:** Contains the lysate and reverse transcriptase, enabling the conversion of RNA into complementary DNA (cDNA), which is then quantified alongside gDNA.

**Step-by-Step Workflow**

1. **Lysis and Primer Addition:**
    - A crude lysate is prepared by lysing cells to release both gDNA and RNA.
    - Both duplicates are supplemented with a gene-specific primer targeting the transcript of interest.
2. **Reverse Transcription:**
    - Reverse transcription is performed in the RT+ sample to convert RNA transcripts into cDNA. No reverse transcriptase is added to the RT- sample, ensuring that only gDNA is amplified.
3. **Partitioning and dPCR:**
    - Both RT- and RT+ samples are partitioned into droplets and analyzed using digital PCR.
    - In the RT- sample, only gDNA is detected and quantified.
    - In the RT+ sample, both gDNA and cDNA molecules are detected and quantified.
4. **Quantification:** 
- The number of RNA transcripts is calculated by subtracting the gDNA copy number (RT-) from the total copy number (RT+).
- To determine the average number of transcripts per gene copy, the RNA transcript count is divided by the gDNA count from the RT- sample:

Average Transcripts per Gene Copy=(RT+ copies - RT- copies)/RT- copies

![image.png](Selfie-dPCR%201261bbe397bb81929982f983e886e809/image.png)

*source: [Podlesniy and Trullas, 2017]([https://www.nature.com/articles/s41598-017-08270-w](https://www.nature.com/articles/s41598-017-08270-w))*

---

**Applications and Advantages**

Selfie dPCR is particularly useful for exploring:

- **Gene Expression Dynamics:**
    
    Provides insights into how actively a gene is transcribed under various conditions.
    
- **Transcriptional Burst Kinetics:**
    
    Measures the variability and frequency of transcriptional bursts in different cell types or states.
    
- **Absolute Quantification of Expression:**
    
    Unlike relative quantification methods (e.g., qPCR), Selfie dPCR offers precise, absolute measurements of transcript numbers per encoding gene.
    

---

By integrating reverse transcription directly into the digital PCR workflow, Selfie dPCR provides a straightforward yet effective way to quantify RNA transcript numbers per gene, offering robust insights into cellular and molecular biology processes.