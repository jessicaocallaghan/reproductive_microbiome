## Read me file for completing a reanalysis of publically available microbiome datasets.

To reanalyse publically available placental sequencing data. 



**SRA download**

Sequences from the datasets which we wanted to analysis were collated into a list and a for loop was used to download the raw reads with the **sra_read_download** script



# Pipeline analysis

The raw reads were used as an input into the standard QIIME2 pipeline to output a biom table. 

1. Upload raw reads (QIIME2)
2. Check quality (QIIME2)
3. Denoise the reads and assemble into ASVs (QIIME2)
4. Export the reads (dna-sequences.fa) and ASV table (biom). (QIIME2)
5. Analyse reads with decontam.
6. Pull non contaminant reads (real sequences) from the dna-sequences.fa using the ./faSomeRecords using the list of sequences from decontam.
7. Summarize reads and import into R to characterised their taxonomic classification.
8. Use ASV and raw read counts and taxonomic classification to make ggplot2 figures. 











