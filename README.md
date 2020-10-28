# Clinical_Validation_Of_WES
#Pipeline to validate clinical whole exome using GIAB data set
the Genome In A Bottle (GIAB) Consortium (https://www.nist.gov/programs-projects/genome-bottle) in conjunction with the National Institute of Standards and Technology have
produced a series of high coverage reference genome in which SNP and INDEL locations are considered to be well characterized (True VCF file v3.3.2). USCS Human Reference genome
(GRCh37/hg19) downloaded and processed by this pipeline using BWA-MEM (Version 0.7.17-r1188) for Alignments, Samtools (Version 1.10)/Picards-tools (2.23.8) for post-alignments
processing and GATK (4.1.8.1) HapolcallerType for Variants calling (Query VCF file).
quality control metrics regarding the following parameter:
A.	True Positive (TP): Variants found in both Query and True VCF files.
B.	False Positive (FP): Variants found in Query VCF file buy Not in True VCF file.
C.	False Negative (FN): Variants found in True VCF buy Not in file Query VCF file. 
D.	True Negative (TN): Variants Not found in both True and Query VCF files

RTG vcfeval command, which performs a sophisticated comparison of VCF files. RTG vcfeval performs variant comparison at the haplotype level; that is, it determines whether the
genotypes asserted in the VCFs under comparison result in the same genomic sequence when applied to the reference genome. The RTG vcfeval output VCF files containing false
positives, false negatives, and true positives.
##Analytical sensitivity or Limit of detection:
False positive variants may arise through sequencing and bioinformatics selection/filtering artefacts.
The number of True Negative can’t exactly calculate but can be estimated to great accuracy. The estimation above 0.1% at most as per 
Heng Li. (https://groups.google.com/a/realtimegenomics.com/g/rtg-users/c/3JU3j2wDHcI/m/r_jGaW3ZAAAJ).
