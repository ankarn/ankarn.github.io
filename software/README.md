# List of the software #

[Databases](databases.md) 

[Phylogenetics](phylogeny.md)

[Genomics](ngs.md)

[Scripts](scripts.md)

1. [blast](https://www.ncbi.nlm.nih.gov/books/NBK279690/)

version 2.2.31+

Basic Local Alignment Search Tool (BLAST) is probably the most popular similarity search tool. Sequence similarity searching is one of the more important bioinformatics activities and often provides the first evidence for the function of a newly sequenced gene or piece of sequence. 

`blastn` `blastp` `blastx` `tblastn` `makeblastdb` `blastdbcmd`  

2. [diamond](https://github.com/bbuchfink/diamond)  

DIAMOND is a sequence aligner for protein and translated DNA searches and functions as a drop-in replacement for the NCBI BLAST software tools. It is suitable for protein-protein search as well as DNA-protein search on short reads and longer sequences including contigs and assemblies, providing a speedup of BLAST ranging up to x20,000.  

`diamond makedb --in nr.faa -d nr` `diamond blastp -d nr -q proteins.fna -o output`

3. [sra-toolkit](https://www.ncbi.nlm.nih.gov/books/NBK158900/)

version 2.3.5-2

The SRA Toolkit will allow you to programmatically access data housed within SRA and convert it from the SRA format to the other formats.


4. [cdhit](http://weizhongli-lab.org/cd-hit/)

version 4.6

CD-HIT is a very widely used program for clustering and comparing protein or nucleotide sequences.

`cdhit` `cdhit-2d` `cdhit-454` `cdhit-est` `cdhit-est-2d` `cd-hit-2d-para` `cd-hit-div` `cd-hit-para`


5. [EMBOSS](http://emboss.sourceforge.net/what/)

version 6.6.0.0

EMBOSS is "The European Molecular Biology Open Software Suite". EMBOSS is a free Open Source software analysis package specially developed for the needs of the molecular biology (e.g. EMBnet) user community. 

6. [hmmer](http://hmmer.org)

version 2.3.2 (hmm2)  
version 3.1b2 (hmm)

HMMER is used for searching sequence databases for sequence homologs, and for making sequence alignments. It implements methods using probabilistic models called profile hidden Markov models (profile HMMs).

`hmmalign` ` hmmbuild ` `hmmcalibrate` `hmmconvert` `hmmemit` `hmmfetch` `hmmindex`  `hmmpfam`   `hmmsearch`

7. [Orthofinder](https://github.com/davidemms/OrthoFinder)  

version 2.0.0  

Accurate inference of orthologous gene groups made easy. "OrthoFinder: solving fundamental biases in whole genome comparisons dramatically improves orthologous gene group inference accuracy"

`orthofinder`

8. [tmux](https://github.com/tmux/tmux/wiki) 

tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal. 

[tmux cheatsheet](https://gist.github.com/MohamedAlaa/2961058)

9. [biopython](http://biopython.org)
 
 Biopython is a set of freely available tools for biological computation written in Python.  
 
[Databases](databases.md)  
