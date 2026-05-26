# 750-Advanced-Genomic-Analysis-Cycle-2-Report---Gene-X
Characterisation of the mutated version of Gene X and its effect on gene expression. 

# Genomic and transcriptomic analysis to characterise the mutated version of 'Gene X' and investigate its effect on gene expression. 

# Analysis was split into 4 main sections:

# Variant Calling
Variant calling analysis (SNV calling) was performed to identify SNP mutations in Gene X by aligning and comparing DNA sequencing reads of Gene X from haploid normal and mutant samples (FASTQ format) to the FASTA genome assembly reference. The FASTA and FASTQ files provided information on SNPs, and as the individuals were haploid, only one allele was present at each position which simplified variant detection. 

# RNA-Seq Analysis
RNA-seq analysis was conducted to identify differentially expressed genes between mutant and normal samples, and investigate how the mutations in Gene X alter this expression. Gene expression count data (.tsv) in which each value represents the number of sequencing reads mapped to a gene in both mutant and normal samples were used for differential expression analysis, conducted with DESeq2 (Love et al., 2014) in R (Version 4.3.3). 

# CUT&RUN 
CUT&RUN data analysis was performed to discover regions where Gene X directly binds to the genome. This method is known as a genome localisation assay that identifies binding peaks, annotated against genomic features by mapping chromatin targets to identify genes located near Gene X binding sites. 

# Combining RNA-Seq and CUT&RUN data 
The DESeq2 data and the CUT&RUN data (bound gene list) was merged in R to determine if and how many differentially expressed genes are directly bound by Gene X (potential direct transcriptional targets) in the mutated samples. This was defined as those that are both bound to Gene X and are significantly differentially expressed (up or downregulated) in the samples with the mutated version of Gene X compared to normal. 
