# Moroccan-Cannabis-Adaptation
A reproducible population genomics and local adaptation pipeline for Cannabis sativa
<div align="center">

# 🌿 Moroccan-Cannabis-Adaptation

### A reproducible pipeline for population genomics, local adaptation, and genomic–phenotypic integration in *Cannabis sativa*

[![Linux](https://img.shields.io/badge/Linux-Ubuntu-blue?logo=linux)]()
[![Python](https://img.shields.io/badge/Python-3.10+-yellow?logo=python)]()
[![R](https://img.shields.io/badge/R-4.3+-blue?logo=r)]()
[![Conda](https://img.shields.io/badge/Conda-supported-brightgreen?logo=anaconda)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()
[![Status](https://img.shields.io/badge/Status-Active_Development-orange)]()

---

**End-to-end Whole Genome Sequencing (WGS) analysis pipeline**

**FASTQ → Variant Discovery → Population Genomics → Local Adaptation → GWAS → Publication-quality Figures**

---

*A comprehensive workflow developed for the genomic characterization of the Moroccan Beldia Cannabis landrace and adaptable to other Cannabis populations and diploid plant species.*

</div>

---

# 📖 Overview

**Moroccan-Cannabis-Adaptation** is a fully reproducible population genomics pipeline designed for whole-genome resequencing (WGS) analysis of *Cannabis sativa*.

The repository provides a complete workflow beginning with raw Illumina sequencing reads and ending with publication-ready figures, candidate adaptive genes, genome-wide association results, and genomic–phenotypic integration.

The pipeline combines modern bioinformatics tools with statistical genomics approaches to investigate:

- Population structure
- Genetic diversity
- Evolutionary history
- Local adaptation
- Quantitative trait divergence
- Candidate adaptive loci
- Functional annotation
- Genome-wide association studies (GWAS)

Although originally developed for Moroccan Cannabis populations, the workflow is modular and can be adapted for many diploid plant species.

---

# 🎯 Scientific Objectives

This pipeline was developed to answer the following biological questions:

- How is genetic diversity distributed among Cannabis populations?
- What is the genomic structure of Moroccan Cannabis?
- How much gene flow occurs among populations?
- Which genomic regions are under local adaptation?
- Which genes are likely targets of selection?
- Which loci contribute to cannabinoid and agronomic traits?
- How are genomic and phenotypic divergence connected?
- How does Moroccan Cannabis compare with worldwide germplasm?

---

# ✨ Key Features

## Population Genomics

- Principal Component Analysis (PCA)
- Discriminant Analysis of Principal Components (DAPC)
- ADMIXTURE ancestry estimation
- Maximum Likelihood phylogeny
- Linkage Disequilibrium (LD)
- Isolation-by-Distance (IBD)
- AMOVA

---

## Genetic Diversity

- Nucleotide diversity (π)
- Expected heterozygosity (He)
- Observed heterozygosity (Ho)
- Inbreeding coefficient (FIS)
- Tajima's D
- Pairwise FST

---

## Local Adaptation

- Sliding-window FST
- π-ratio
- Candidate gene identification
- Functional annotation
- GO enrichment
- KEGG enrichment

Optional modules

- XP-EHH
- iHS
- LFMM
- Redundancy Analysis (RDA)

---

## Genomic–Phenotypic Integration

- Quantitative trait differentiation (QST)
- QST vs FST
- Mantel test
- GWAS
- Candidate adaptive loci
- Integrated evolutionary interpretation

---

## Publication Outputs

The workflow automatically generates:

- Publication-quality figures
- Supplementary figures
- Summary tables
- Candidate gene lists
- GWAS results
- GO enrichment tables
- Diversity statistics
- Population structure analyses

---

# 🚀 Pipeline Workflow


# 📊 Pipeline Modules

| Module | Description |
|---------|-------------|
| Quality Control | FastQC & MultiQC |
| Read Processing | Adapter trimming |
| Genome Alignment | BWA-MEM |
| Variant Discovery | GATK |
| SNP Filtering | VCFtools, PLINK |
| Population Structure | PCA, DAPC, ADMIXTURE |
| Diversity Statistics | π, He, Ho, FIS, Tajima's D |
| Population Differentiation | FST, AMOVA |
| Selection Scans | FST, π-ratio |
| Candidate Genes | BEDTools |
| Functional Annotation | GO & KEGG |
| GWAS | GAPIT |
| Integration | QST, Mantel, Circos |

---

# 📦 Expected Outputs

The pipeline produces:

✅ High-quality SNP datasets
✅ Population structure analyses
✅ Genetic diversity statistics
✅ Phylogenetic trees
✅ Selection scan results
✅ Candidate adaptive genes
✅ Functional enrichment analyses
✅ GWAS results
✅ Publication-ready figures
✅ Supplementary tables

---

# ⚡ Quick Start

Clone the repository

```bash
git clone https://github.com/<username>/Moroccan-Cannabis-Adaptation.git

cd Moroccan-Cannabis-Adaptation
```

Create Conda environment

```bash
conda env create -f environment.yml

conda activate cannabis
```

Run the pipeline

```bash
bash run_pipeline.sh
```

or execute individual modules

```bash
scripts/
01_Preprocessing/
02_Mapping/
03_Variant_Calling/
04_Filtering/
05_Population_Genomics/
06_Local_Adaptation/
07_GWAS/
08_Figures/
```

---

# 📚 Documentation

Comprehensive documentation is available in the **docs/** directory.

| Document | Description |
|-----------|-------------|
| Installation.md | Installation guide |
| Pipeline.md | Complete workflow |
| Population_Genomics.md | Population genomic analyses |
| Local_Adaptation.md | Selection scans |
| GWAS.md | Genome-wide association |
| Figures.md | Figure generation |
| Troubleshooting.md | Common issues |
