# Analyzing COVID RNA Sequences

This repository contains a Jupyter Notebook for analyzing COVID-19 genome sequences. The analysis includes metadata processing, sequence alignment, and comparisons between different variants such as Delta and Omicron.

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Analysis](#analysis)
  - [Metadata Processing](#metadata-processing)
  - [Sequence Alignment](#sequence-alignment)
  - [Results](#results)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [License](#license)

## Introduction

The project uses genomic data from SARS-CoV-2 to analyze and compare different variants. The notebook includes:

- Metadata processing using `pandas`
- Sequence alignment using Biopython's `Align.PairwiseAligner`
- Pairwise comparisons of genome sequences

## Data

The dataset includes genomic sequences and metadata for SARS-CoV-2 variants:

- **Reference genome**: `NC_045512.2` (Wuhan-Hu-1)
- **Delta variant**: `OM061695.1`
- **Omicron variant**: `OM095411.1`

### Sample Metadata

| Nucleotide Accession | Species Name                                   | Virus Genus       | Virus Family   | Isolate Name                                | Nucleotide Length | Geo Location          | Collection Date |
|-----------------------|-----------------------------------------------|-------------------|----------------|--------------------------------------------|-------------------|-----------------------|-----------------|
| NC_045512.2          | Severe acute respiratory syndrome coronavirus 2 | Betacoronavirus  | Coronaviridae | Wuhan-Hu-1                                 | 29903             | Asia; China           | 2019-12-01      |
| OM061695.1           | Severe acute respiratory syndrome coronavirus 2 | Betacoronavirus  | Coronaviridae | SARS-CoV-2/human/CHN/Delta-1/2021          | 29858             | Asia; China: Beijing  | 2021-08-10      |
| OM095411.1           | Severe acute respiratory syndrome coronavirus 2 | Betacoronavirus  | Coronaviridae | SARS-CoV-2/human/CHN/Omicron-1/2021        | 29788             | Asia; China: Beijing  | 2021-12-08      |

## Analysis

### Metadata Processing

The metadata was processed using `pandas` to extract relevant information such as:

- Collection dates
- Geographic locations
- Nucleotide lengths

### Sequence Alignment

Pairwise alignments were performed using the Needleman-Wunsch algorithm (`Align.PairwiseAligner`) to compare the reference genome with Delta and Omicron variants.

### Results

The alignment scores between the variants are as follows:

| Variant      | Reference Score | Delta Score | Omicron Score |
|--------------|-----------------|-------------|---------------|
| Reference    | 1.0000          | 0.9972      | 0.9940        |
| Delta        | 0.9972          | 1.0000      | 0.9968        |
| Omicron      | 0.9940          | 0.9968      | 1.0000        |

## How to Run

1. git clone https://github.com/your-username/covid-genome-analysis.gitcd](https://github.com/GMK2000GMK/Analyzing-COVID-RNA-Sequences.git covid-genome-analysis
1. pip install -r (packages)
1. jupyter notebook covid.ipynb

## Dependencies

The following Python libraries are required:

- `pandas`
- `numpy`
- `biopython`
- `matplotlib`

Install them using:

```
pip install pandas numpy biopython matplotlib
```
