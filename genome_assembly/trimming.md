# Trimming

1. [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)

`trimmomatic PE <lef_reads.fastq> <right_reads.fastq> <left_paired.fastq> <left_unpaired.fastq> <right_paired.fastq> <right_unpaired.fastq> ILLUMINACLIP:<path_to_adaptors>:2:30:9 LEADING:2 TRAILING:2 SLIDINGWINDOW:4:15 MINLEN:25
`
Path to adaptros: `/opt/trinityrnaseq/trinity-plugins/Trimmomatic/adapters/TruSeq3-PE-2.fa`  
Not always (but most likely) the TruSeq3-PE-2.fa file contains your adaptors, you might want to check, which file with adaptors you should use before running trimming. 

### Options  


### Comments: MINLEN parameter should be always in the end of the command line  

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
