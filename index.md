---
layout: default
title: Incorporate Deep Learning Model to Better Predict Individual Gene Expression
---


## 🏠 Welcome!  

📌 **Quick Links:**  

---

## 🔍 Introduction  

Alzheimer’s Disease (AD) is a progressive neurodegenerative disorder, with **APOE** identified as the strongest genetic risk factor. Genome-wide association studies (GWAS) have uncovered genetic loci associated with AD, but they do not directly explain the impact of variants on gene expression. Expression quantitative trait loci (eQTL) analysis bridges this gap by linking genetic variants to transcriptional changes.

Recent advances in **deep learning** have enabled accurate prediction of gene expression from DNA sequences. Models like **Enformer** provide a powerful framework for understanding regulatory variants. Our study leverages deep learning to analyze how **SNPs within the APOE locus** influence gene expression and compares these predictions with eQTL findings to validate the model’s biological relevance.

---

## 🎯 Objectives  

- Investigate how **SNPs affect gene expression** in the **APOE locus**.  
- Utilize **deep learning (Enformer)** to predict transcriptional changes caused by SNPs.  
- Compare **eQTL analysis results** with **deep learning predictions** to validate findings.  
- Explore the potential integration of **Polygenic Risk Scores (PRS)** with deep learning for AD risk assessment.  

---

## 🛠 Methods  

### 📊 Data Processing  
- Use **GTEx gene expression data** and **1000 Genomes SNP data**.  
- Convert SNP data into **PLINK & VCF** formats for genetic variant analysis.  
- Extract genotype information and **modify DNA reference sequences** accordingly.  

### 🤖 Deep Learning Predictions (Enformer Model)  
- Construct **genotype-informed sequences** incorporating SNP variations.  
- Convert DNA sequences into **one-hot encoded tensors** for deep learning input.  
- Use **Enformer** to predict gene expression and compare with **GTEx expression data**.  

### 🔬 SNP Effect Quantification  
- Generate expression predictions for **reference vs. alternate alleles**.  
- Compute absolute signal differences to assess the impact of each SNP.  
- Align with **eQTL results** to validate predicted transcriptional effects.   

---

## 📊 Results & Impact  

---



## 🎯 Conclusion & Next Steps  

📌 **What’s Next?**  
- Possible future improvements  
- Open questions to explore  
---

## 📬 Get in Touch  
_(Provide a way for visitors to connect, such as a LinkedIn profile or email.)_  


