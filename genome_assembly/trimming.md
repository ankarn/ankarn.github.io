# Trimming

1. [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)

`trimmomatic PE <lef_reads.fastq> <right_reads.fastq> <left_paired.fastq> <left_unpaired.fastq> <right_paired.fastq> <right_unpaired.fastq> ILLUMINACLIP:<path_to_adaptors>:2:30:9 LEADING:2 TRAILING:2 SLIDINGWINDOW:4:15 MINLEN:25
`
Path to adaptros: `/opt/trinityrnaseq/trinity-plugins/Trimmomatic/adapters/TruSeq3-PE-2.fa`  
Not always (but most likely) the TruSeq3-PE-2.fa file contains your adaptors, you might want to check, which file with adaptors you should use before running trimming. 

### Options  

Trimmomatic's parameters might require a little more explanation. 
`The three numbers that go after ILLUMINACLIP and the path to adapters are the parameters for removal of adapters and you're most likely not going to change them ever, unless, for example, the adapter sequence in your results is not 30 nucleotides long. If it isn't, just change the "30" in the command above to the appropriate value.
`The LEADING/TRAILING parameters stand for the cutoff quality value for first and last (respectively) nucleotides below which they will be removed. As their quality is usually poor, it is advised not to set these parameters to high values (like 20), but rather 2 or 3 in order to remove nucleotides which have absolutely no informative value at all (a score of 1 means more or less "completely random").
`The two SLIDINGWINDOW parameters stand for the length of the scanning window and mean cutoff quality value for the entire window for the tool's quality check procedure, e.g. for SLIDINGWINDOW:4:15 the reads are divided into 4-nucleotide segments and if the mean quality per nucleotide in such a window is below 15, the segment is discarded. Briefly saying, the lower the first value and the higher the second one, the higher amount of sequences will be recognized as poor quality and discarded. When setting these parameters, it's crucially important to keep the balance between strict quality control and loss of a significant portion of data that might result from setting a very high cutoff quality value.
`MINLEN parameter is basically the minimum length of a sequence - anything shorter than the specified value will be discarded. In a decent set of data, this value can be set to up to 80 and the removed sequences will be as little as 0.1% of the total obtained data.

### Comments: MINLEN parameter should be always in the end of the command line.

### Also, it is advised to run fastqc once again after trimming to take a closer look at what really happened. Since different parameters may have a huge impact on the output and there are no universally optimal values, it might be necessary to run this tool multiple times before a satisfactory result is obtained.

### Output

While running you will see at the scree some information, which will look more or less like that  

`TrimmomaticPE: Started with arguments: Equartana_R1.fastq Equartana_R2.fastq Equartana_R1_trinity_paired.fastq Equartana_R1_trinity_npaired.fastq Equartana_R2_trinity_paired.fastq Equartana_R2_trinity_npaired.fastq ILLUMINACLIP:/opt/trinityrnaseq-2.2.0/trinity-plugins/Trimmomatic/adapters/TruSeq3-PE-2.fa:2:30:9 LEADING:2 TRAILING:2 SLIDINGWINDOW:4:15 MINLEN:25
Multiple cores found: Using 16 threads
Using PrefixPair: 'TACACTCTTTCCCTACACGACGCTCTTCCGATCT' and 'GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT'
Using Long Clipping Sequence: 'AGATCGGAAGAGCGTCGTGTAGGGAAAGAGTGTA'
Using Long Clipping Sequence: 'AGATCGGAAGAGCACACGTCTGAACTCCAGTCAC'
Using Long Clipping Sequence: 'GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT'
Using Long Clipping Sequence: 'TACACTCTTTCCCTACACGACGCTCTTCCGATCT'
ILLUMINACLIP: Using 1 prefix pairs, 4 forward/reverse sequences, 0 forward only sequences, 0 reverse only sequences
Quality encoding detected as phred33
Input Read Pairs: 4459091 Both Surviving: 4445833 (99,70%) Forward Only Surviving: 7613 (0,17%) Reverse Only Surviving: 5625 (0,13%) Dropped: 20 (0,00%)
TrimmomaticPE: Completed successfully`

Output will contain four files, two files with the left reads and two with right reads, for each of them there will be one file with reads, which still have pair (new_name_for_left_paired.fastq) and one file with reads, which lost their pair during trimmming (new_name_left_unpaired.fastq)  
