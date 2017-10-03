# List of the software #

[Databases](databases.md) 

[Phylogenetics](phylogeny.md)

[genomics](ngs.md)

1. [blast](https://www.ncbi.nlm.nih.gov/books/NBK279690/)

version 2.2.31+

Basic Local Alignment Search Tool (BLAST) is probably the most popular similarity search tool. Sequence similarity searching is one of the more important bioinformatics activities and often provides the first evidence for the function of a newly sequenced gene or piece of sequence. 

`blastn` `blastp` `blastx` `tblastn` `makeblastdb` `blastdbcmd`

2. [sra-toolkit](https://www.ncbi.nlm.nih.gov/books/NBK158900/)

version 2.3.5-2

The SRA Toolkit will allow you to programmatically access data housed within SRA and convert it from the SRA format to the other formats.


3. [cdhit](http://weizhongli-lab.org/cd-hit/)

version 4.6

CD-HIT is a very widely used program for clustering and comparing protein or nucleotide sequences.

`cdhit` `cdhit-2d` `cdhit-454` `cdhit-est` `cdhit-est-2d` `cd-hit-2d-para` `cd-hit-div` `cd-hit-para`


4. [EMBOSS](http://emboss.sourceforge.net/what/)

version 6.6.0.0

EMBOSS is "The European Molecular Biology Open Software Suite". EMBOSS is a free Open Source software analysis package specially developed for the needs of the molecular biology (e.g. EMBnet) user community. 

5. [hmmer](http://hmmer.org)

version 2.3.2 (hmm2)  
version 3.1b2 (hmm)

HMMER is used for searching sequence databases for sequence homologs, and for making sequence alignments. It implements methods using probabilistic models called profile hidden Markov models (profile HMMs).

`hmmalign` ` hmmbuild ` `hmmcalibrate` `hmmconvert` `hmmemit` `hmmfetch` `hmmindex`  `hmmpfam`   `hmmsearch`

### NGS software

1. [bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)

version 2.2.6

Bowtie 2 is an ultrafast and memory-efficient tool for aligning sequencing reads to long reference sequences.

2. [tophat](https://ccb.jhu.edu/software/tophat/index.shtml)

version 2.1.0

TopHat is a fast splice junction mapper for RNA-Seq reads. Please note that TopHat has entered a low maintenance, low support stage as it is now largely superseded by HISAT2 (32).

3. [bamtools](https://github.com/pezmaster31/bamtools/wiki)

version 2.4.0

Bamtools is a command-line toolkit for reading, writing, and manipulating BAM (genome alignment) files. 

4. [samtools](http://samtools.sourceforge.net)

Version: 0.1.19-96b5f2294a

SAM Tools provide various utilities for manipulating alignments in the SAM format, including sorting, merging, indexing and generating alignments in a per-position format.

[samtools cheatsheet](https://davetang.org/wiki/tiki-index.php?page=SAMTools)

5. [bedtools](http://bedtools.readthedocs.io/en/latest/)

version 2.25.0

6. [bwa](http://bio-bwa.sourceforge.net)

version 0.7.12-r1039

BWA is a software package for mapping low-divergent sequences against a large reference genome, such as the human genome.

7. [fastx-toolkit](http://hannonlab.cshl.edu/fastx_toolkit/)

version 0.0.14

The FASTX-Toolkit is a collection of command line tools for Short-Reads FASTA/FASTQ files preprocessing.

8. [gmap](http://research-pub.gene.com/gmap/src/README)

version 2015-12-31

GMAP: a genomic mapping and alignment program for mRNA and EST sequences

[aligner tutorial](https://github.com/PacificBiosciences/cDNA_primer/wiki/Aligner-tutorial:-GMAP,-STAR,-BLAT,-and-BLASR#refgmap)

9. [trinity](https://github.com/trinityrnaseq/trinityrnaseq/wiki)

version 2.4.0

Trinity assembles transcript sequences from Illumina RNA-Seq data.

`trinity`

10. [SPAdes](http://spades.bioinf.spbau.ru/release3.10.1/manual.html#sec2.1)

version 3.10.1

SPAdes – St. Petersburg genome assembler – is an assembly toolkit containing various assembly pipelines. 

11. [QUAST](http://quast.sourceforge.net/quast.html)

version 4.5

QUAST evaluates genome assemblies

`quast`

12. [STAR](https://github.com/alexdobin/STAR)

version 2.5.0a

STAR: ultrafast universal RNA-seq aligner

`STAR`

13. [NOVOPlasty](https://github.com/ndierckx/NOVOPlasty)

version 2.6.2

NOVOPlasty is a de novo assembler for short circular genomes.

`novoplasty`

14. [trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)

Trimmomatic: A flexible read trimming tool for Illumina NGS 

`trimmomatic`

15. [fastqc](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)

version 0.11.4

A quality control tool for high throughput sequence data.

`fastqc -h`

16. [hisat2](https://ccb.jhu.edu/software/hisat2/index.shtml)  

version 2.1.0

HISAT2 is a fast and sensitive alignment program for mapping next-generation sequencing reads (both DNA and RNA) to a population of genomes (as well as to a single reference genome). 

`hisat2` `hisat2-align-s` `hisat2-align-l` `hisat2-build` `hisat2-build-s` `hisat2-build-l` `hisat2-inspect` `hisat2-inspect-s` `hisat2-inspect-l`

 17. [seqtk](https://github.com/lh3/seqtk)
 
 version 1.0-r31
 
 Seqtk is a fast and lightweight tool for processing sequences in the FASTA or FASTQ format.
 
 `seqtk`  
 
 18. [DBG2OLC](https://github.com/yechengxi/DBG2OLC)  
 
DBG2OLC:Efficient Assembly of Large Genomes Using Long Erroneous Reads of the Third Generation Sequencing Technologies  

`DBG2OLC` `AssemblyStatistics` `SelectLongestReads` `Sparc` `SparseAssembler`  

19. [CANU](http://canu.readthedocs.io/en/stable/)  

Canu 1.6

Canu is a fork of the Celera Assembler designed for high-noise single-molecule sequencing (such as the PacBio RSII or Oxford Nanopore MinION).

`canu`

20. [minimap/miniasm](https://github.com/lh3/miniasm)  

minimap version 0.2-r124-dirty

miniasm version 0.2-r168-dirty

Miniasm is a very fast OLC-based de novo assembler for noisy long reads.  

`minimap` `miniasm`  

21. [Pilon](https://github.com/broadinstitute/pilon/wiki)  

version 1.22

Pilon is a software tool which can be used to (1) automatically improve draft assemblies and (2) find variation among strains, including large event detection.  

`pilon`  

22. [BUSCO](https://gitlab.com/ezlab/busco)  

Assessing genome assembly and annotation completeness with Benchmarking Universal Single-Copy Orthologs (BUSCO)

*under construction*  

23. [blobtools](https://blobtools.readme.io/docs)  

A modular command-line solution for visualisation, quality control and taxonomic partitioning of genome datasets  

*under construcion*

24. [sspace](https://github.com/nsoranzo/sspace_basic)  

SSPACE is a script able to extend and scaffold pre-assembled contigs using one or more mate pairs or paired-end libraries, or even a combination.  

`perl /opt/sspace_basic/SSPACE_Basic.pl`  

25. [PLATANUS](http://platanus.bio.titech.ac.jp/)  

PLATform for Assembling NUcleotide Sequences

Read more: Kajitani R, Toshimoto K, Noguchi H, Toyoda A, Ogura Y, Okuno M, Yabana M, Harada M, Nagayasu E, Maruyama H, Kohara Y, Fujiyama A, Hayashi T, Itoh T, “Efficient de novo assembly of highly heterozygous genomes from whole-genome shotgun short reads”. Genome Res. 2014 Aug;24(8):1384-95. doi: 10.1101/gr.170720.113. 

*under construction*

26. [CGAL](https://pachterlab.github.io/cgal/)   

CGAL is a tool for computing genome assembly likelihoods. It computes the likelihood of reads with respect to the assembly and a statistical model which can be used as a metric for evaluating assemblies.  

*unser construction*  

27. [Orthofinder](https://github.com/davidemms/OrthoFinder)  

version 2.0.0  

Accurate inference of orthologous gene groups made easy. "OrthoFinder: solving fundamental biases in whole genome comparisons dramatically improves orthologous gene group inference accuracy"

`orthofinder`

### other

1. [tmux](https://github.com/tmux/tmux/wiki) 

tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal. 

[tmux cheatsheet](https://gist.github.com/MohamedAlaa/2961058)

2. [biopython](http://biopython.org)
 
 Biopython is a set of freely available tools for biological computation written in Python.  
 
[Databases](databases.md)  
