# Bowtie2

Bowtie is memory-efficient alignment tools that alignes the sequencing reads to reference genomes. Bowtie2 indexes the reference genomes first to save memory small.the index reference genome are used to running the Bowtie2 tool.

# Installation

conda install -c bioconda bowtie2

# Running Bowtie2 tool for metagenomic analysis

> First Index the reference genome;

bowtie2-build Listeria_monocytogenes_genomic_RefSeq.fasta Listeria_monocytogenes

> Running the bowtie2 ;

bowtie2 -x Bacteroides_vulgatus SRR072233.fastq --no-unal -p 12 -S Bacteroides_vulgatus_bowtie.sam

1386198 reads; of these:

1386198 (100.00%) were unpaired; of these:

1309880 (94.49%) aligned 0 times

76318 (5.51%) aligned exactly 1 time

0 (0.00%) aligned >1 times

5.51% overall alignment rate

> By using Samtools; sam file can be coverted to bam file and then sorted and index for next steps which can be variant calling or other analysis.
