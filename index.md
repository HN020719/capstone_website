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

\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{shapes.geometric, arrows}

\tikzstyle{startstop} = [rectangle, rounded corners, minimum width=3cm, minimum height=1cm,text centered, draw=black, fill=red!30]
\tikzstyle{process} = [rectangle, minimum width=3cm, minimum height=1cm, text centered, draw=black, fill=blue!20]
\tikzstyle{decision} = [diamond, minimum width=3cm, minimum height=1cm, text centered, draw=black, fill=yellow!30]
\tikzstyle{arrow} = [thick,->,>=stealth]

\begin{document}

\begin{center}
    \begin{tikzpicture}[node distance=2.5cm]

        % Nodes
        \node (start) [startstop] {Start: Genotype & Expression Data};
        \node (vcf) [process, below of=start] {Extract Genotype from VCF};
        \node (modGenome) [process, below of=vcf] {Modify hg38 with Individual Variants};
        \node (onehot) [process, below of=modGenome] {Convert to One-Hot Encoding};
        \node (enformer) [process, below of=onehot] {Run Enformer for Gene Expression Prediction};
        \node (aggregate) [process, below of=enformer] {Aggregate Predictions \& Extract CAGE Tracks};
        \node (normalize) [process, below of=aggregate] {Log Transform \& Z-score Normalization};
        \node (adjust) [process, below of=normalize] {Adjust Predictions using Ridge Regression \& RF};
        \node (compare) [process, below of=adjust] {Compare vs True Expression \& PRS};
        \node (end) [startstop, below of=compare] {End: Evaluate Performance};

        % Arrows
        \draw [arrow] (start) -- (vcf);
        \draw [arrow] (vcf) -- (modGenome);
        \draw [arrow] (modGenome) -- (onehot);
        \draw [arrow] (onehot) -- (enformer);
        \draw [arrow] (enformer) -- (aggregate);
        \draw [arrow] (aggregate) -- (normalize);
        \draw [arrow] (normalize) -- (adjust);
        \draw [arrow] (adjust) -- (compare);
        \draw [arrow] (compare) -- (end);

    \end{tikzpicture}
\end{center}

\end{document}


## 🎯 Conclusion & Next Steps  

📌 **What’s Next?**  
- Possible future improvements  
- Open questions to explore  
---

## 📬 Get in Touch  
_(Provide a way for visitors to connect, such as a LinkedIn profile or email.)_  


