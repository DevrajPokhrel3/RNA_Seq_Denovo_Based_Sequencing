# 🧬 De novo RNA-seq Assembly and Differential Expression Analysis

This repository documents a **de novo RNA-seq transcriptome analysis** pipeline using **Trinity**, **RSEM**, **edgeR**, **TransDecoder**, and **BLAST+**.  
It is designed for tumor-free and tumor-bearing *Drosophila melanogaster* larvae samples.  

---

## 📂 Dataset Information
- **Organism:** *Drosophila melanogaster*  
- **Conditions:**  
  - Control (tumor-free larvae)  
  - Treated (tumor-bearing larvae)  
- **Input Data:** Adapter-trimmed paired-end FASTQ files  

---

## 🔧 Tools & Dependencies
Make sure the following tools are installed before running the pipeline:  
- [Trinity](https://github.com/trinityrnaseq/trinityrnaseq)  
- [RSEM](https://deweylab.github.io/RSEM/)  
- [Bowtie](http://bowtie-bio.sourceforge.net/index.shtml)  
- [edgeR (R package)](https://bioconductor.org/packages/release/bioc/html/edgeR.html)  
- [TransDecoder](https://github.com/TransDecoder/TransDecoder)  
- [BLAST+](https://blast.ncbi.nlm.nih.gov/Blast.cgi)  
- `samtools`  
- `assembly-stats`  

---

## 🚀 Workflow Overview

### Steps
1. Concatenate FASTQ samples  
2. Convert FASTQ → FASTA  
3. Perform **de novo assembly** with Trinity  
4. Calculate assembly statistics (`assembly-stats`)  
5. Estimate transcript abundance with RSEM  
6. Generate count matrix (`abundance_estimates_to_matrix.pl`)  
7. Perform differential expression with **edgeR**  
8. Predict coding regions with **TransDecoder**  
9. Functional annotation with **BLASTp** (against UniProt)  

---

## 📊 Outputs
- **Assembly:** `Trinity.fasta`, `Assembly_Statistics.txt`  
- **Abundance Estimates:** RSEM output directories  
- **Count Matrix:** `abundance_count.isoform.counts.matrix`  
- **Differential Expression:** edgeR results (`DE_results.txt`)  
- **Predicted ORFs:** TransDecoder `.pep` and `.cds` files  
- **Functional Annotation:** BLAST results (`result.txt`)  

---

## 📖 References
- [Trinity RNA-seq](https://github.com/trinityrnaseq/trinityrnaseq)  
- [RSEM](https://deweylab.github.io/RSEM/)  
- [edgeR Bioconductor](https://bioconductor.org/packages/release/bioc/html/edgeR.html)  
- [TransDecoder](https://github.com/TransDecoder/TransDecoder)  
- [BLAST+](https://blast.ncbi.nlm.nih.gov/Blast.cgi)  

---

## ✍️ Author
**Devraj Pokhrel**  
B.Sc. Biotechnology


