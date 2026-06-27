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

---

# 📂 Repository Structure

The repository follows a modular design in which each analysis is organized into independent, reproducible components.

```text
Moroccan-Cannabis-Adaptation/
│
├── README.md                      # Project homepage
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
│
├── environment.yml                # Conda environment
├── requirements.txt               # Python packages
│
├── config/
│   ├── config.yaml
│   ├── samples.tsv
│   ├── populations.tsv
│   └── parameters.yaml
│
├── docs/
│   ├── Installation.md
│   ├── Pipeline.md
│   ├── Population_Genomics.md
│   ├── Local_Adaptation.md
│   ├── GWAS.md
│   ├── Figures.md
│   ├── FAQ.md
│   └── Troubleshooting.md
│
├── scripts/
│
│   ├── 01_Preprocessing/
│   ├── 02_Mapping/
│   ├── 03_Variant_Calling/
│   ├── 04_SNP_Filtering/
│   ├── 05_Population_Genomics/
│   ├── 06_Global_Phylogeny/
│   ├── 07_Local_Adaptation/
│   ├── 08_Functional_Annotation/
│   ├── 09_GWAS/
│   ├── 10_Genomic_Phenotypic_Integration/
│   ├── 11_Figure_Generation/
│   └── utilities/
│
├── workflow/
│
│   ├── Snakefile
│   ├── Nextflow.config
│   └── run_pipeline.sh
│
├── data/
│
│   ├── raw/
│   ├── cleaned/
│   ├── reference/
│   ├── annotation/
│   ├── metadata/
│   └── phenotype/
│
├── results/
│
│   ├── QC/
│   ├── Alignment/
│   ├── Variants/
│   ├── Population_Genomics/
│   ├── Diversity/
│   ├── Phylogeny/
│   ├── Selection/
│   ├── GWAS/
│   ├── Figures/
│   └── Supplementary/
│
├── example_data/
│
├── example_results/
│
├── manuscript/
│
└── supplementary/
```

---

# 💻 System Requirements

## Operating System

- Ubuntu 22.04 LTS (recommended)
- Ubuntu 20.04
- Rocky Linux
- CentOS 7+
- macOS (limited support)

---

## Hardware Requirements

### Minimum

| Resource | Requirement |
|----------|-------------|
| CPU | 8 cores |
| RAM | 32 GB |
| Storage | 500 GB |
| Operating System | Linux |

---

### Recommended

| Resource | Requirement |
|----------|-------------|
| CPU | 32–64 cores |
| RAM | 128–512 GB |
| Storage | 2 TB SSD |
| HPC Cluster | SLURM |

---

### Large Population Studies

| Samples | Recommended RAM |
|----------|----------------:|
| <50 | 32 GB |
| 50–150 | 128 GB |
| 150–500 | 256 GB |
| >500 | HPC recommended |

---

# 🧰 Software Requirements

## Core Bioinformatics Tools

| Software | Purpose |
|----------|---------|
| FastQC | Raw read quality assessment |
| MultiQC | Quality report aggregation |
| Trimmomatic | Adapter trimming |
| BWA-MEM | Genome alignment |
| SAMtools | BAM processing |
| Picard | Duplicate marking |
| GATK | Variant discovery |
| BCFtools | Variant processing |
| VCFtools | Population genetics |
| PLINK | Population genomics |
| ADMIXTURE | Ancestry inference |
| IQ-TREE | Phylogenetic inference |
| BEDTools | Genomic interval analysis |
| SnpEff / ANNOVAR | Variant annotation |
| eggNOG-mapper | Functional annotation |
| clusterProfiler | GO/KEGG enrichment |

---

## R Packages

- adegenet
- poppr
- hierfstat
- dartR
- SNPRelate
- ggplot2
- tidyverse
- data.table
- vegan
- lme4
- qqman
- GAPIT3
- circlize
- ComplexHeatmap
- ggtree
- patchwork

---

## Python Packages

- pandas
- numpy
- scipy
- matplotlib
- plotly
- scikit-allel
- biopython
- seaborn
- jupyter

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/<username>/Moroccan-Cannabis-Adaptation.git

cd Moroccan-Cannabis-Adaptation
```

---

## Create Conda Environment

```bash
conda env create -f environment.yml
```

Activate environment

```bash
conda activate cannabis
```

---

## Verify Installation

```bash
python --version

R --version

gatk --version

bwa

plink --version
```

---

# 📥 Input Data

The pipeline accepts multiple input types.

## Whole Genome Sequencing

```text
FASTQ (.fastq.gz)
```

paired-end Illumina reads

---

## Reference Genome

```text
FASTA (.fa)

GFF3

GTF
```

---

## Metadata

```text
samples.tsv
```

Example

| Sample | Population | Province | Latitude | Longitude |
|---------|------------|-----------|----------|-----------|
| Sample01 | AH | Al Hoceima | ... | ... |

---

## Phenotype Data

```text
traits.csv
```

Supported traits include

- Morphological traits
- Agronomic traits
- Biomass
- THC
- CBD
- CBN
- Flowering time
- Seed traits

---

# 📤 Pipeline Outputs

The workflow automatically generates

## Quality Control

- FastQC reports
- MultiQC reports

---

## Alignment

- Sorted BAM
- BAM index
- Alignment statistics

---

## Variant Discovery

- Raw VCF
- Filtered VCF
- SNP statistics

---

## Population Genomics

- PCA
- DAPC
- ADMIXTURE
- FST
- Diversity statistics
- LD decay
- IBD
- AMOVA

---

## Local Adaptation

- Sliding-window FST
- π-ratio
- Candidate genes
- GO enrichment
- KEGG enrichment

---

## GWAS

- Manhattan plots
- QQ plots
- Significant SNP tables
- Candidate genes

---

## Publication Outputs

- Publication-quality PDF figures
- High-resolution PNG images
- Supplementary tables
- Candidate gene tables

---

# ⚙️ Configuration Files

Pipeline behaviour is controlled through

```text
config/

config.yaml

parameters.yaml

samples.tsv

populations.tsv
```

Users generally only need to edit

- reference genome
- sample metadata
- population assignments
- phenotype files

---

# 🖥️ HPC Support

The pipeline is designed for High Performance Computing (HPC).

Supported schedulers

- SLURM
- PBS (minor modifications)
- SGE (minor modifications)

Example

```bash
sbatch run_pipeline.sh
```

Each analysis module can also be submitted independently.

---

# 📊 Typical Runtime

| Module | Approximate Time |
|---------|----------------:|
| Quality Control | 20 min |
| Alignment | 2–6 hr |
| Variant Calling | 8–24 hr |
| Filtering | 20 min |
| PCA | 2 min |
| ADMIXTURE | 5–60 min |
| IQ-TREE | 30 min |
| FST Scan | 10 min |
| GWAS | 15 min |
| Figure Generation | 5–20 min |

*Runtime depends on dataset size and computing resources.*

---

# 🔒 Reproducibility

This repository follows reproducible research principles.

- Conda-managed software environments
- Version-controlled scripts
- Fixed software dependencies
- Modular workflows
- Standardized directory layout
- Reproducible figure generation
- Complete documentation
- HPC-compatible execution

Every manuscript figure can be regenerated directly from the provided scripts using the documented input files.

---

---

# 🧬 Analysis Modules

The pipeline is organized into independent analysis modules. Each module can be executed separately or as part of the complete workflow.

| Module | Purpose | Main Tools | Outputs |
|----------|---------|------------|----------|
| **01_Preprocessing** | Quality assessment and read cleaning | FastQC, MultiQC, Trimmomatic | Clean FASTQ |
| **02_Mapping** | Align reads to reference genome | BWA-MEM, SAMtools, Picard | Sorted BAM |
| **03_Variant_Calling** | SNP and INDEL discovery | GATK | Raw VCF |
| **04_SNP_Filtering** | High-confidence SNP filtering | VCFtools, BCFtools, PLINK | Filtered VCF |
| **05_Population_Genomics** | Population structure and diversity | PLINK, ADMIXTURE, adegenet | PCA, DAPC, Diversity |
| **06_Global_Phylogeny** | Evolutionary relationships | IQ-TREE | Phylogenetic tree |
| **07_Local_Adaptation** | Detect genomic signatures of adaptation | VCFtools, BEDTools | FST, π-ratio |
| **08_Functional_Annotation** | Candidate gene annotation | eggNOG, clusterProfiler | GO & KEGG |
| **09_GWAS** | Genome-wide association analysis | GAPIT | Manhattan plots |
| **10_Genomic_Phenotypic_Integration** | Integrate genomic and phenotypic data | R | QST, Mantel, Circos |
| **11_Figure_Generation** | Publication-quality figures | ggplot2, patchwork | Figures 1–7 |

---

# 📊 Manuscript Figures Generated

The pipeline automatically generates publication-ready figures corresponding to the manuscript.

| Figure | Description | Pipeline Module |
|----------|-------------|----------------|
| **Figure 1** | Phenotypic and phytochemical variation | Phenotypic Analysis |
| **Figure 2** | Genetic diversity and population differentiation | Population Genomics |
| **Figure 3** | Population structure (PCA, DAPC, ADMIXTURE) | Population Structure |
| **Figure 4** | Global phylogeny | Phylogenetics |
| **Figure 5** | Local adaptation (FST, π-ratio, candidate genes, GO enrichment) | Local Adaptation |
| **Figure 6** | Genomic–phenotypic integration | Integration |
| **Supplementary Figures** | Quality control, SNP statistics, additional analyses | Various modules |

---

# 📈 Scientific Workflow

```text
Whole Genome Sequencing
           │
           ▼
Quality Control
           │
           ▼
Read Alignment
           │
           ▼
Variant Calling
           │
           ▼
High-quality SNP Dataset
           │
           ▼
────────────────────────────────────────────
Population Genomics
────────────────────────────────────────────

Population Structure

Genetic Diversity

Phylogenetic Analysis

Population Differentiation

           │
           ▼
────────────────────────────────────────────
Adaptive Evolution
────────────────────────────────────────────

Selection Scans

Candidate Genes

Functional Annotation

GWAS

Genotype–Phenotype Integration

           │
           ▼
Publication-quality Figures

           │
           ▼

Biological Interpretation
```

---

# 📁 Major Output Files

| Directory | Description |
|-----------|-------------|
| results/QC | Quality reports |
| results/Alignment | BAM files |
| results/Variants | VCF files |
| results/Diversity | Diversity statistics |
| results/Population_Genomics | PCA, DAPC, ADMIXTURE |
| results/Phylogeny | IQ-TREE outputs |
| results/Selection | FST and π-ratio |
| results/Annotation | Candidate genes |
| results/GWAS | GWAS outputs |
| results/Figures | Final figures |

---

# 🌱 Future Modules

The repository is actively expanding.

Planned additions include:

- XP-EHH
- iHS
- XP-CLR
- PBS
- LFMM
- BayPass
- Redundancy Analysis (RDA)
- Environmental association analyses
- Polygenic adaptation
- Landscape genomics
- Structural variant discovery
- Copy-number variation
- Pangenome analysis
- Transcriptome integration (RNA-seq)
- Epigenomic analyses

---

# 📚 Documentation

Detailed documentation is available in the **docs/** directory.

| Document | Description |
|-----------|-------------|
| Installation.md | Installation guide |
| Pipeline.md | Complete workflow |
| Population_Genomics.md | Population genomic analyses |
| Local_Adaptation.md | Selection scans |
| Functional_Annotation.md | GO & KEGG |
| GWAS.md | Genome-wide association |
| Figures.md | Figure generation |
| Troubleshooting.md | Frequently encountered issues |
| FAQ.md | Frequently asked questions |

---

# 🔬 Reproducible Research

This repository follows FAIR and reproducible research principles.

✔ Fully documented pipeline

✔ Modular analysis

✔ Open-source software

✔ Standardized directory structure

✔ Version-controlled scripts

✔ Conda environments

✔ HPC-compatible

✔ Publication-ready figures

✔ Comprehensive documentation

---

# 🤝 Contributing

Contributions are welcome.

You can contribute by:

- Improving documentation
- Reporting bugs
- Suggesting new analyses
- Optimizing scripts
- Adding visualization modules
- Supporting additional sequencing platforms

Please see **CONTRIBUTING.md** before submitting a pull request.

---

# 📖 Citation

If you use this repository in your research, please cite:

```text
Biswas K., et al.

Moroccan-Cannabis-Adaptation:
A reproducible pipeline for population genomics,
local adaptation, and genomic–phenotypic integration
in Cannabis sativa.

GitHub:
https://github.com/<username>/Moroccan-Cannabis-Adaptation

DOI:
(To be added after Zenodo release)
```

---

# 📜 License

This project is distributed under the **MIT License**.

See the **LICENSE** file for details.

---

# 🙏 Acknowledgements

This workflow was developed as part of a comprehensive genomic investigation of the Moroccan **Beldia** Cannabis landrace.

We acknowledge the contributions of collaborators, sequencing facilities, and the institutions supporting this research.

This repository is intended to provide a transparent, reproducible, and extensible framework for cannabis genomics, evolutionary biology, plant breeding, and conservation genetics.

---

# 📬 Contact

**Project Lead**

Manosh Kumar Biswas

GitHub:
https://github.com/<username>

Email:
kumar.biswas@um6p.ma

---

<div align="center">

## ⭐ If this repository is useful for your research, please consider giving it a star.

### 🌿 Advancing reproducible Cannabis genomics through open science.

</div>
