# Genomics #

## quality control ##  

1. [fastqc](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)

version 0.11.4

A quality control tool for high throughput sequence data.

`fastqc -h`

12. [trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)

Trimmomatic: A flexible read trimming tool for Illumina NGS 

`trimmomatic`

3. [blobtools](https://blobtools.readme.io/docs)  

A modular command-line solution for visualisation, quality control and taxonomic partitioning of genome datasets  

*under construcion*  

4. [BUSCO](https://gitlab.com/ezlab/busco)  

Assessing genome assembly and annotation completeness with Benchmarking Universal Single-Copy Orthologs (BUSCO)

*under construction*  

## genome and transcriptome assembly ##

1. [kmergenie](http://kmergenie.bx.psu.edu)

version 1.7044

KmerGenie estimates the best k-mer length for genome de novo assembly. 

2. [SPAdes](http://spades.bioinf.spbau.ru/release3.10.1/manual.html#sec2.1)

version 3.10.1

SPAdes – St. Petersburg genome assembler – is an assembly toolkit containing various assembly pipelines. 

3. [trinity](https://github.com/trinityrnaseq/trinityrnaseq/wiki)

version 2.4.0

Trinity assembles transcript sequences from Illumina RNA-Seq data.

`trinity`  

4. [NOVOPlasty](https://github.com/ndierckx/NOVOPlasty)

version 2.6.2

NOVOPlasty is a de novo assembler for short circular genomes.

`novoplasty`

5. [DBG2OLC](https://github.com/yechengxi/DBG2OLC)  
 
DBG2OLC:Efficient Assembly of Large Genomes Using Long Erroneous Reads of the Third Generation Sequencing Technologies  

`DBG2OLC` `AssemblyStatistics` `SelectLongestReads` `Sparc` `SparseAssembler`  

dependencies  

[blasr](https://github.com/PacificBiosciences/blasr)  

BLASR: The PacBio® long read aligner 

[pbdgacon](https://github.com/PacificBiosciences/pbdagcon)  

A sequence consensus algorithm implementation based on using directed acyclic graphs to encode multiple sequence alignment  

6. [CANU](http://canu.readthedocs.io/en/stable/)  

Canu 1.6

Canu is a fork of the Celera Assembler designed for high-noise single-molecule sequencing (such as the PacBio RSII or Oxford Nanopore MinION).

`canu`

7. [minimap/miniasm](https://github.com/lh3/miniasm)  

minimap version 0.2-r124-dirty

miniasm version 0.2-r168-dirty

Miniasm is a very fast OLC-based de novo assembler for noisy long reads.  

`minimap` `miniasm`  

8. [PLATANUS](http://platanus.bio.titech.ac.jp/)  

PLATform for Assembling NUcleotide Sequences

Read more: Kajitani R, Toshimoto K, Noguchi H, Toyoda A, Ogura Y, Okuno M, Yabana M, Harada M, Nagayasu E, Maruyama H, Kohara Y, Fujiyama A, Hayashi T, Itoh T, “Efficient de novo assembly of highly heterozygous genomes from whole-genome shotgun short reads”. Genome Res. 2014 Aug;24(8):1384-95. doi: 10.1101/gr.170720.113. 

*under construction*  

9. [sspace](https://github.com/nsoranzo/sspace_basic)  

SSPACE is a script able to extend and scaffold pre-assembled contigs using one or more mate pairs or paired-end libraries, or even a combination.  

`perl /opt/sspace_basic/SSPACE_Basic.pl`  

10. [Pilon](https://github.com/broadinstitute/pilon/wiki)  

version 1.22

Pilon is a software tool which can be used to (1) automatically improve draft assemblies and (2) find variation among strains, including large event detection.  

`java -jar /opt/pilon-1.22.jar`  

11. [QUAST](http://quast.sourceforge.net/quast.html)

version 4.5

QUAST evaluates genome assemblies

`quast`  

12. [CGAL](https://pachterlab.github.io/cgal/)   

CGAL is a tool for computing genome assembly likelihoods. It computes the likelihood of reads with respect to the assembly and a statistical model which can be used as a metric for evaluating assemblies.  

*unser construction*  

13. [SOAPdenovo](https://github.com/aquaskyline/SOAPdenovo2)  

Version 2.04

Next generation sequencing reads de novo assembler.  

14. [MIRA](http://mira-assembler.sourceforge.net/docs/DefinitiveGuideToMIRA.html)  

version 4.0.0 (the newest version 4.0.2 is not working properly)

MIRA is a multi-pass DNA sequence data assembler/mapper for whole genome and EST/RNASeq projects.

*cicuta only*  

15. [edena](http://www.genomic.ch/edena.php) 

vesrion 3  

de novo short reads assembler  

*cicuta only*  

16. [velvet](https://www.ebi.ac.uk/~zerbino/velvet/)  

version 1.2.10  

Velvet is a de novo genomic assembler specially designed for short read sequencing technologies, such as Solexa or 454.

*cicuta only*  

17. [GRAbB](https://github.com/b-brankovics/grabb#installation)  

GRAbB (Genome Region Assembly by Baiting) is program designed to assemble selected regions of the genome or transcriptome using reference sequences and NGS data.  

`grabb`

*cicuta only*  

18. [REAPR](http://www.sanger.ac.uk/science/tools/reapr) 

version: 1.0.18  

REAPR is a tool that evaluates the accuracy of a genome assembly using mapped paired end reads, without the use of a reference genome for comparison. It can be used in any stage of an assembly pipeline to automatically break incorrect scaffolds and flag other errors in an assembly for manual inspection. It reports mis-assemblies and other warnings, and produces a new broken assembly based on the error calls. 

`reapr`

*cicuta only*

## mapping ##

1. [bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)

version 2.2.6

Bowtie 2 is an ultrafast and memory-efficient tool for aligning sequencing reads to long reference sequences.

2. [tophat](https://ccb.jhu.edu/software/tophat/index.shtml)

version 2.1.0

TopHat is a fast splice junction mapper for RNA-Seq reads. Please note that TopHat has entered a low maintenance, low support stage as it is now largely superseded by HISAT2 (32).

3. [bwa](http://bio-bwa.sourceforge.net)

version 0.7.12-r1039

BWA is a software package for mapping low-divergent sequences against a large reference genome, such as the human genome.  

4. [gmap](http://research-pub.gene.com/gmap/src/README)

version 2015-12-31

GMAP: a genomic mapping and alignment program for mRNA and EST sequences

[aligner tutorial](https://github.com/PacificBiosciences/cDNA_primer/wiki/Aligner-tutorial:-GMAP,-STAR,-BLAT,-and-BLASR#refgmap)  

5. [STAR](https://github.com/alexdobin/STAR)

version 2.5.0a

STAR: ultrafast universal RNA-seq aligner

`STAR`  

6. [hisat2](https://ccb.jhu.edu/software/hisat2/index.shtml)  

version 2.1.0

HISAT2 is a fast and sensitive alignment program for mapping next-generation sequencing reads (both DNA and RNA) to a population of genomes (as well as to a single reference genome). 

`hisat2` `hisat2-align-s` `hisat2-align-l` `hisat2-build` `hisat2-build-s` `hisat2-build-l` `hisat2-inspect` `hisat2-inspect-s` `hisat2-inspect-l`


## File processing ##

1. [fastx-toolkit](http://hannonlab.cshl.edu/fastx_toolkit/)

version 0.0.14

The FASTX-Toolkit is a collection of command line tools for Short-Reads FASTA/FASTQ files preprocessing.

2. [seqtk](https://github.com/lh3/seqtk)
 
 version 1.0-r31
 
 Seqtk is a fast and lightweight tool for processing sequences in the FASTA or FASTQ format.
 
 `seqtk`  

3. [bamtools](https://github.com/pezmaster31/bamtools/wiki)

version 2.4.0

Bamtools is a command-line toolkit for reading, writing, and manipulating BAM (genome alignment) files. 

4. [samtools](http://samtools.sourceforge.net)

Version: 1.6

SAM Tools provide various utilities for manipulating alignments in the SAM format, including sorting, merging, indexing and generating alignments in a per-position format.

[samtools cheatsheet](https://davetang.org/wiki/tiki-index.php?page=SAMTools)

5. [bedtools](http://bedtools.readthedocs.io/en/latest/)

version 2.25.0  

6. [prinseq](http://prinseq.sourceforge.net/Data_preprocessing.pdf)  

PRINSEQ-lite 0.20.4  

PRINSEQ will help you to preprocess your genomic or metagenomic sequence data in FASTA or FASTQ format  

7. [BBMap](https://github.com/BioInfoTools/BBMap)  

BBMap short read aligner, and other bioinformatic tools.  

`/opt/BBMap/`  

8. [bcftools](https://samtools.github.io/bcftools/bcftools.html)  

BCFtools is a set of utilities that manipulate variant calls in the Variant Call Format (VCF) and its binary counterpart BCF.  

## Annotation ##  

*cicuta only*

1. [RepeatModeler](http://www.repeatmasker.org/RepeatModeler/) 

version open-1.0.11  

RepeatModeler is a de-novo repeat family identification and modeling package. At the heart of RepeatModeler are two de-novo repeat finding programs ( RECON and RepeatScout ) which employ complementary computational methods for identifying repeat element boundaries and family relationships from sequence data.  

`RepeatModeler`

2. [RepeatMasker](http://www.repeatmasker.org)  

version open-4.0.7  

RepeatMasker is a program that screens DNA sequences for interspersed repeats and low complexity DNA sequences. The output of the program is a detailed annotation of the repeats that are present in the query sequence as well as a modified version of the query sequence in which all the annotated repeats have been masked (default: replaced by Ns).  

`RepeatMasker`  

3. [CIRI](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-014-0571-3)  

Version:  2.0.6  

CIRI: an efficient and unbiased algorithm for de novo circular RNA identification  

`perl /opt/CIRI_v2.0.6/CIRI2.pl`  





