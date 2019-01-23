# Estimation of the genome assembly quality

1. [QUAST](http://bioinf.spbau.ru/quast)  
Useful tool for comparison of basic metrics of assemblies, as mentioned in the previous chapter. The command should be like this:  

`quast.py assembly_file.fasta`  

Note: you can (and you should) run QUAST on multiple assemblies at once, but for some reason it will run only if all input files are in the same folder or you specify exact files (so `quast.py *.fasta` and `quast.py dir1/file1.fasta dir2/file2.fasta [...]` are fine, but `quast.py */*.fasta` is not).

Output  

This is how the report should look like:

![Screenshot](ankarn.github.io/quastreport.jpg)

What's quite convenient is that every parameter in every assembly is highlighted with a color corresponding to its quality - you will not need to estimate if a value is good or bad by yourself. As it was mentioned before, the K127 assembly is most likely the best one in terms of all or at least a majority of parameters.

N50 - under construction  

2. [Bandage](https://rrwick.github.io/Bandage/)

Bandage is a localy run program with functional and user friendly GUI, which runs on Windows, OS and Linux. It allows to view and edit assembly graphs produced by SPAdes or other DBG assemblers. The guide will asume you are using SPAdes, filenames may vary in other assemeblers.
It requirers assembly_graph.fastg, located in SPAdes output directory on your desktop. After you load the file, there are 4 main ways to view de Brujin graphs:
- whole graph (not recommended with eukaryotes)
- around certain nodes (edges)
- around BLAST hits (requires accessible from command line blast+ package)
- only nodes in coverage range
It is important to note, that "nodes" in the graph are not nodes in contigs.fasta. They are EDGES, which can be foun in assembly_graph.fastg. Edges corresponding to nodes can be found in contigs.paths.


3. mapping reads 

[bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)   

Bowtie2 is a tool for mapping of sequences onto the assembled genome, which is done by a two-step procedure: making a set of BT2 index files and making a SAM mapping file.  
For the first step, the command should be like this:

`bowtie2-build <genome_assembly.fasta> <index_name>`   

Note: this command will produce more than one file - the output files will be named index_name.1.bt2, index_name.2.bt2 and so on. This is very important for the next step, where the outputs are required as an input, but they should be addressed in a rather non-intuitive way - they go after "-x", but despite them being multiple files with partially identical names, you CAN'T put the asterisk in their name as it's usually done in the command line. In brief, use only the index_name, but not index_name* or index_name*.bt2.  
This is the command for the second step:

`bowtie2 -x <index_name> -1 <folder/reads_1.fastq> -2 <folder/reads_2.fastq> -S <mapping.sam>`   

The files that are addressed after -1 and -2 are your original data obtained from the sequencing, which are the UNASSEMBLED reads. For the reads merged with PEAR, the command should be slightly different:   
 
`bowtie2 -x <index_name> -U <folder/reads.fq> -S <mapping.sam>`   

Unlike the .bt2 index files, the output in SAM format is human-readable, so you can do a quick quality check here. The file should consist of two parts: headers, which are lines starting with @, and alignments, which are nucleotide sequences, sequence IDs, scores and a few more numbers - something that looks like a little more elaborate version of FASTQ. If there's something clearly wrong with the SAM - e.g. there are only headers in the file - you should check if the input files you used are consistent with each other, or in simple words, if the assembly used for indexing (1st part) is the assembly you generated from the reads used for mapping (2nd part). Files can get mixed up sometimes.  

[STAR](https://github.com/alexdobin/STAR); under construction   

utworzyć folder, w którym będzie indeks   
`mkdir <nazwa>`    

generowanie indeksu   
`/home/ankarn/bin/STAR-2.5.3a/bin/Linux_x86_64/STAR --runThreadN n --runMode genomeGenerate --genomeDir <ścieżka do folderu z indeksem> --limitGenomeGenerateRAM 166028754304 --genomeFastaFiles <ścieżka do assembly genomu>`   

mapowanie   
`/home/ankarn/bin/STAR-2.5.3a/bin/Linux_x86_64/STAR --runThreadN n --genomeDir <ścieżka indeks> --readFilesIn <ścieżka_lewy_odczyt> <ścieżka prawy odczyt> --outFileNamePrefix <ścieżka i prefix do output> --outSAMtype BAM SortedByCoordinate`
