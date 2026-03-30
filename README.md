# Transcriptomic and Network Analysis of Triple Negative Breast Cancer (TNBC)
RNA-seq based differential expression and network analysis using data from TCGA to identify key regulatory genes and pathways in TNBC.

## 🧬 Overview

Triple Negative Breast Cancer (TNBC) is an aggressive and molecularly heterogeneous subtype of breast cancer characterized by the absence of estrogen receptor (ER), progesterone receptor (PR), and HER2 expression. This limits the effectiveness of targeted therapies and contributes to poorer clinical outcomes.

This project presents an integrated multi-phase analysis of TNBC using data from The Cancer Genome Atlas (TCGA), combining transcriptomic, genomic, and clinical perspectives. The workflow progresses from RNA-seq based differential expression analysis to gene network construction, followed by mutation profiling and survival analysis.

By integrating multiple layers of biological information, this study aims to move beyond isolated gene-level observations and provide a systems-level understanding of TNBC, highlighting key regulatory genes, mutational patterns, and clinically relevant biomarkers.

---

## 📌 Objective

The objective of this study is to perform a comprehensive multi-layered analysis of Triple Negative Breast Cancer (TNBC) using TCGA data, integrating transcriptomic, genomic, and clinical insights through a structured analytical pipeline.

Specifically, this study aims to:

- Acquire and preprocess TNBC-specific data from TCGA  
- Identify significantly differentially expressed genes (DEGs) using DESeq2  
- Construct gene interaction networks to detect key hub genes  
- Analyze mutation profiles to identify frequently altered genes  
- Perform survival analysis to evaluate the clinical relevance of candidate genes  
- Integrate all findings to identify potential biomarkers and mechanistic drivers of TNBC  

The overarching goal is to establish an end-to-end analytical framework that links molecular alterations to clinical outcomes in TNBC.

---

## 🧬 Background

Triple Negative Breast Cancer (TNBC) accounts for approximately 15–20% of breast cancer cases and is associated with high rates of metastasis, recurrence, and clinical heterogeneity. At the molecular level, TNBC exhibits extensive variability across gene expression, mutational landscapes, and clinical outcomes.

Large-scale cancer genomics initiatives such as The Cancer Genome Atlas (TCGA) have enabled systematic exploration of these molecular alterations. RNA sequencing facilitates the identification of differentially expressed genes, while mutation data provides insights into genomic instability and driver alterations. Additionally, clinical data enables evaluation of patient survival and disease prognosis.

However, these data types are often analyzed independently, limiting the ability to derive integrated biological insights. Understanding TNBC requires connecting gene expression changes with mutational patterns and clinical outcomes to better identify key drivers of disease progression.

---

## 🧠 Research Gap

While numerous studies have investigated TNBC using RNA-seq, mutation profiling, or survival analysis individually, integrated analyses that combine these layers into a cohesive and interpretable framework remain limited.

Many approaches focus on identifying large sets of DEGs or frequently mutated genes without systematically linking them to gene interaction networks or clinical outcomes. This makes it challenging to prioritize key regulatory genes and assess their biological and clinical significance.

Furthermore, there is a need for structured, reproducible pipelines that connect transcriptomic, genomic, and clinical analyses into a unified workflow.

---

## 🧪 Methodology

This study employs a structured, multi-phase analytical pipeline to investigate TNBC using data from TCGA, integrating transcriptomic, genomic, and clinical analyses.

### 🔹 Phase 1: Data Acquisition

RNA-seq data, mutation data, and clinical metadata were obtained from TCGA-BRCA. TNBC samples were identified through receptor-based filtering (ER-, PR-, HER2-), and relevant datasets were curated for downstream analysis.

---

### 🔹 Phase 2: Differential Expression Analysis

Differential gene expression analysis was performed using DESeq2 in R. Data were normalized, and statistical testing was conducted to identify significantly dysregulated genes. Genes were filtered using thresholds of adjusted p-value (padj < 0.05) and |log2FoldChange| > 1. Visualization techniques such as volcano plots and heatmaps were generated.

---

### 🔹 Phase 3: Gene Network Analysis

Significant DEGs were used to construct gene interaction networks. Network metrics such as degree centrality were calculated to identify highly connected hub genes. Network visualization was performed to highlight key regulatory structures and interaction patterns.

---

### 🔹 Phase 4: Mutation Analysis

Mutation data were analyzed to identify frequently altered genes in TNBC samples. Mutation frequency and patterns were examined to highlight potential driver genes and complement transcriptomic findings.

---

### 🔹 Phase 5: Survival Analysis

Survival analysis was conducted to evaluate the clinical relevance of identified genes. Kaplan–Meier survival curves and statistical tests were used to assess associations between gene expression or mutation status and patient outcomes.

---

## 🔬 Workflow Overview

[TCGA-BRCA Data (RNA-seq + Mutation + Clinical)]
                      ->
[Data Acquisition & TNBC Sample Selection]
                      ->
[DESeq2 Differential Expression Analysis]
                      ->
[DEG Filtering]
                      ->
[Gene Network Construction]
                      ->
[Hub Gene Identification]
                      ->
[Mutation Analysis]
                      ->
[Survival Analysis]
                      |
[Integrated Biological Interpretation]

Each phase builds upon the previous step, enabling a transition from molecular data to clinically relevant insights in TNBC.
