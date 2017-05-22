# Organellar genome assembly

1. NOVOPlasty v.2.5.9  
[NOVOPlasty](https://github.com/ndierckx/NOVOPlasty)

Useful for plastid, mitochondrial and plants mitochondrial genomes. Requires seed. 

`perl /home/ankarn/bin/NOVOPlasty/NOVOPlasty2.5.9.pl -c config.txt`

configuration file preparation

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
**Seed Input**          = The path to the file that contains the seed sequence. [you have to find and download the proper seed file; that could be conserved organellar gene from the same or very similar genome or the genome of related species; NOVOPlasty will inform you if the seed is not valid]  
**Chloroplast sequence** = The path to the file that contains the chloroplast sequence (Only for mito_plant mode).  


2. Fast-Plast (Ania is testing)  
[Fast-Plast](https://github.com/mrmckain/Fast-Plast)

Input files might be not quality trimmed and with adaptors, everything will be prepared during the run. There are ready to use bowtie indexes for various groups of plants and algae but there is also option of custom index.  

*There is a problem when the genome dosen't contain IR.*  

--bowtie_index Mamiellales, Euglenales [check manual for all possible options]  
--adapter [NEB|Nextera|TruSeq]  
--coverage_analysis [recommended]  
--clean light   

` perl /home/ankarn/bin/Fast-Plast/fast-plast.pl -1 left.fastq -2 right.fastq -n test --threads 6 --bowtie_index	Euglenales --adapters TruSeq --coverage_analysis --clean light`
