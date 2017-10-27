# [Blobtools](https://blobtools.readme.io/docs)

Tools for making blobplots or Taxon-Annotated-GC-Coverage plots (TAGC plots) to visualise the contents of genome assembly data sets as a QC step.  
Blobtools is a bit more tricky than all the previously used tools, as it requires multiple input files in formats not mentioned before. The first thing you'll need is BLAST results in a tab-separated-values file with very specific data in each column, which you can produce using this command:  
  `blastn -query assembly_file.fasta -db mnt/databases/NCBI/nt -outfmt "6 qseqid staxids bitscore std" -max_target_seqs 1 -max_hsps 1 -num_threads 4 -evalue 1e-25 -out results_file.txt`  
  Next, you need a sorted BAM mapping file which you can obtain by converting (and sorting) the SAM generated previously:
  `samtools view -Sb mapping.sam > mapping.bam`  
`samtools sort mapping.bam mapping_sorted.bam`  
  Now, to run the first step of blobtools (creating a database file), you need this command:  
  `/opt/blobtools/blobtools create -i assembly.fasta -b mapping_sorted.bam -t blastresults.txt -o filename`  
  As you could probably guess by now, the "-i", "-b" and "-t" parameters indicate the three input files. What's extremely important is that for some reason, blobtools doesn't recognize any sort of path other than to itself, meaning that you have to put all the input files in the same folder and be in that folder in order to run this command.  
The next step is creating a table with results:  
  `/opt/blobtools/blobtools view -i filename.blobDB.json`  
  For a visualization of the results and a basic statistic of taxa that the sequences are associated with, use:  
  `/opt/blobtools/blobtools blobplot -i filename.blobDB.json`  
  (We're going to elaborate a little more on these results soon)  
  Now, since blobtools is a tool for detection (and quantification) of contamination in the data, it would be rather convenient to also mention how to remove the contaminating sequences. For example, let's assume that blobtools associated some of the sequences with Firmicutes. To remove these sequences from your assembly, you can use a set of commands:  
  `grep -v "Firmicutes" blobtools_view_output.blobDB.table.txt > blobtools_table_without_firmicutes.txt`  
  `cut -f 1,1 blobtools_table_without_firmicutes.txt > node_names.txt`  
  `/opt/scripts/fasta_tool --select node_names.txt assembly.fasta > assembly_clean.fasta`  
  What's left in the `assembly_clean.fasta` file is your assembly without the Firmicutes-associated sequences. At this point, it might be useful to compare this new assembly file with the old one (e.g. by QUAST) to see what changed after removal of the contaminations - for example, to see if there's anything remotely relevant left in your assembly.   

# KAT

The K-mer Analysis Toolkit (KAT) contains a number of tools that analyse and compare K-mer spectra  
[KAT](https://github.com/TGAC/KAT)

# MCSC

pipeline for decontamination of biological sequences  

[MCSC_DEcontamination](https://github.com/Lafond-LapalmeJ/MCSC_Decontamination)

