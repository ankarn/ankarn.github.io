# List of the software #

### General 

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

### phylogenetics

1. [mafft](http://mafft.cbrc.jp/alignment/software/)

version 7.271

MAFFT is a multiple sequence alignment program for unix-like operating systems.  
`mafft in > out`

2. [raxmlHPC](http://www.exelixis-lab.org)

version 8.2.4

Standard tool for Maximum-likelihood based phylogenetic inference.

3. [iqtree](http://www.iqtree.org/doc/)

version 1.3.11.1 built Feb  1 2016 (quite old)

Efficient phylogenomic software by maximum likelihood

4. [fasttreeMP](http://www.microbesonline.org/fasttree/)

version version 2.1.8

FastTree infers approximately-maximum-likelihood phylogenetic trees from alignments of nucleotide or protein sequences

5. [prottest](https://github.com/ddarriba/prottest3)

version 2.1

ProtTest is a bioinformatic tool for the selection of best-fit models of aminoacid replacement for the data at hand.

6. [readal](http://trimal.cgenomics.org/use_of_the_readal_v1.2)

version 1.2rev59

readAl reads protein or nucleotide alignments in several Multiple Sequence Alignment formats, including Phylip, Fasta, Clustal, NBRF/Pir, Mega and Nexus. The program detects automatically the input format and converts the alignment to other available formats.

7. [trimal](http://trimal.cgenomics.org)

version 1.2rev59

trimAl is a tool for the automated removal of spurious sequences or poorly aligned regions from a multiple sequence alignment

`trimal`

8. [PartitionFinder](http://www.robertlanfear.com/partitionfinder/tutorial/)

PartitionFinder is software to select best-fit partitioning schemes and models of molecular evolution for phylogenetic analyses.

9. [MrBayes](http://mrbayes.sourceforge.net)

version 3.2.6

MrBayes is a program for Bayesian inference and model choice across a wide range of phylogenetic and evolutionary models. MrBayes uses Markov chain Monte Carlo (MCMC) methods to estimate the posterior distribution of model parameters.

`please contact Łukasz B. before you will start using MrBayes`

10. [bmge](http://gensoft.pasteur.fr/docs/BMGE/1.0/BMGE_doc.pdf)

version 1.12

Selects regions in a multiple sequence alignment that are suited for phylogenetic inference. BMGE is able to perform biologically relevant trimming on a multiple alignment of DNA, codon or amino acid sequences.

`bmge -?`  

11. 7. [concaterpillar.py](http://rogerlab.biochemistryandmolecularbiology.dal.ca/Software/Software.htm#Concaterpillar)  


Assessment of congruence for protein alignment concatenation.

### other

1. [tmux](https://github.com/tmux/tmux/wiki) 

tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal. 

[tmux cheatsheet](https://gist.github.com/MohamedAlaa/2961058)

2. [biopython](http://biopython.org)
 
 Biopython is a set of freely available tools for biological computation written in Python.
