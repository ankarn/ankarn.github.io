## Genome assembly ##

### *de novo* assembly - Illumina reads
1. SOAPdenovo  
[SOAPdenovo](https://github.com/aquaskyline/SOAPdenovo2)

2. [SPAdes](http://spades.bioinf.spbau.ru/release3.10.1/manual.html#sec2.1)

version 3.10.1

SPAdes – St. Petersburg genome assembler – is an assembly toolkit containing various assembly pipelines. 

You can start with that command line, -o output, -t numer of threads 

`spades -k 21,33,55,77,99,127 --only-assembler -o -1 -2 -t 4 `  

3. Ray  
[Ray](http://denovoassembler.sourceforge.net/manual.html)

### *de novo* assembly - PacBio reads

1. [minimap/miniasm](https://github.com/lh3/miniasm) 

Dirty and fast preliminary assembly.  
Miniasm is a very fast OLC-based de novo assembler for noisy long reads.

2. [CANU](http://canu.readthedocs.io/en/stable/)  

Canu 1.6

Canu is a fork of the Celera Assembler designed for high-noise single-molecule sequencing (such as the PacBio RSII or Oxford Nanopore MinION).

### *de novo* hybrid assembly - Illumina + PacBio reads

1. SPAdes
2. MaSuRCA
3. [DBG2OLC](https://github.com/yechengxi/DBG2OLC)  
 
DBG2OLC:Efficient Assembly of Large Genomes Using Long Erroneous Reads of the Third Generation Sequencing Technologies  

`DBG2OLC` `AssemblyStatistics` `SelectLongestReads` `Sparc` `SparseAssembler`

### organellar assemblers

1. [NOVOPlasty](https://github.com/ndierckx/NOVOPlasty)

`perl /opt/NOVOPlasty/NOVOPlasty2.5.9.pl -c config.txt`

### configuration file preparation

**Project name**         = Choose a name for your project, it will be used for the output files  
**Insert size**          = Total insert size of your paired end reads, it doesn't have to be accurate but should be close enough  
**Insert size aut**      = yes/no [default: yes; choose yes if you ae not sure what is the insert size]   
**Read Length**          = The read length of your reads [figure it out, for example based on qc report]  
**Type**              = chloro/mito/mito_plant  
**Genome Range**         = The expected genome size range of the genome  [Default 700000-2000000; check closely elated organisms to adjust that number]  
**K-mer**                = This is the length of the overlap between matching reads [I never change that if I have reads longer than 100 bp]    
                       If reads are shorter then 90 bp or you have low coverage data, this value should be decreased down to 23.
                       For reads longer then 101 bp, this value can be increased, but this is not necessary. [default: 39]  
**Insert Range**         = This variation on the insert size, could lower it when the coverage is very high or raise it when the
                       coverage is too low [Default: 1.6; use default in the first run].  
**Insert Range strict**  = Strict variation to resolve repetitive regions [Default: 1.2; use default in the first run]  
**Single/Paired**        = PE [For the moment only paired end reads are supported]  
**Max memory**          = You can choose a max memory usage if you work on deskktop, leave it blank for the server  
**Coverage Cut off**     = You can speed up the assembly by lowering the coverage cut off, standard it will use up to 1000 coverage  
**Extended log**        = Prints out a very extensive log, could be useful to send me when there is a problem  (0/1)  
**Save assembled reads** = All the reads used for the assembly will be stored in seperate files (yes/no)  
**Combined reads**       = The path to the file that contains the combined reads (forward and reverse in 1 file) [very rare case; otherwise leave it blank] 
**Forward reads**        = The path to the file that contains the forward reads (not necessary when there is a merged file)  
**Reverse reads**       = The path to the file that contains the reverse reads (not necessary when there is a merged file)  
**Seed Input**          = The path to the file that contains the seed sequence. [you have to find and download the proper seed file; that could be conserved organellar gene or the genome of closely related species]  
**Chloroplast sequence** = The path to the file that contains the chloroplast sequence (Only for mito_plant mode).  


