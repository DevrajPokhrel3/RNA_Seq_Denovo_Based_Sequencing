# RNA-Seq De Novo Assembly and Differential Expression Analysis Pipeline

This repository contains a pipeline for de novo transcriptome assembly and differential expression analysis from paired-end RNA-Seq data.

## Pipeline Overview

1. Concatenation of samples
2. FASTQ to FASTA conversion
3. De novo assembly using Trinity
4. Assembly statistics calculation
5. Abundance estimation with RSEM
6. Count matrix generation
7. Differential expression analysis with edgeR
8. Coding region identification using TransDecoder
9. Protein database creation and BLAST search

## Requirements

- Trinity (v2.6.6)
- RSEM
- Bowtie
- edgeR
- TransDecoder
- BLAST+
- assembly-stats
- Basic Unix tools (cat, paste, cut, sed, tr)
