# FASTQ-to-BAM
This repository streamlines the conversion of raw DNA sequencing data from FASTQ to BAM format, incorporating scripts that not only facilitate BAM conversion but also generate Sequence Alignment Map (SAM) files.

# "Genomic Alignment Pipeline"

Utilizing Minimap2 and Samtools for efficient data processing and analysis."

## Prerequisites

- [samtools](http://www.htslib.org/download/)
- [minimap2](https://github.com/lh3/minimap2)

## Installation
Align FASTQ to reference genome using minimap2
Convert SAM to BAM using samtools
Replace ref_genome.fa, SRR26624132_1.fastq, and SRR26624132_2.fastq with your actual files.


```bash
brew install samtools
brew install minimap2

minimap2 -t 8 -a -x sr ref_genome.fa SRR26624132_1.fastq SRR26624132_2.fastq -o out_sam.sam

samtools view -bS out_sam.sam > final.bam
```







