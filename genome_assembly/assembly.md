### Genome assembly


1. SOAPdenovo  
[SOAPdenovo](https://github.com/aquaskyline/SOAPdenovo2)

2. SPADes

You can start with that command line, -o output, -t numer of threads  
`spades -k 21,33,55,77,99,127 --only-assembler -o -1 -2 -t 4 `  

3. Ray  
[Ray](http://denovoassembler.sourceforge.net/manual.html)

4. MIRA  

5. The organelle assembler  

[NOVOPlasty](https://github.com/ndierckx/NOVOPlasty)

configuration file

Project name         = Choose a name for your project, it will be used for the output files
Insert size          = Total insert size of your paired end reads, it doesn't have to be accurate but should be close enough
Insert size aut      = yes/no [default: yes]
Read Length          = The read length of your reads
Type                 = chloro/mito/mito_plant
Genome Range         = The expected genome size range of the genome
K-mer                = This is the length of the overlap between matching reads.
                       If reads are shorter then 90 bp or you have low coverage data, this value should be decreased down to 23.
                       For reads longer then 101 bp, this value can be increased, but this is not necessary. [default: 39]
Insert Range         = This variation on the insert size, could lower it when the coverage is very high or raise it when the
                       coverage is too low (Default: 1.6).
Insert Range strict  = Strict variation to resolve repetitive regions (Default: 1.2)
Single/Paired        = PE [For the moment only paired end reads are supported]
Max memory           = You can choose a max memory usage, suitable to automatically subsample the data or when you have limited
                       memory capacity. If you have sufficient memory, leave it blank, else write your available memory in GB
                       (if you have for example a 8 GB RAM laptop, put down 7 or 7.5 (don't add the unit in the config file))
Coverage Cut off     = You can speed up the assembly by lowering the coverage cut off, standard it will use up to 1000 coverage
Extended log         = Prints out a very extensive log, could be useful to send me when there is a problem  (0/1)
Save assembled reads = All the reads used for the assembly will be stored in seperate files (yes/no)
Combined reads       = The path to the file that contains the combined reads (forward and reverse in 1 file)
Forward reads        = The path to the file that contains the forward reads (not necessary when there is a merged file)
Reverse reads        = The path to the file that contains the reverse reads (not necessary when there is a merged file)
Seed Input           = The path to the file that contains the seed sequence.
Chloroplast sequence = The path to the file that contains the chloroplast sequence (Only for mito_plant mode).


6. Plastid assembler (not tested by Ania)   
[Fast-Plast](https://github.com/mrmckain/Fast-Plast)
