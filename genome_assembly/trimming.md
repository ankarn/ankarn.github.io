# Trimming

1. [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)

`trimmomatic PE <lef_reads.fastq> <right_reads.fastq> <new_name_for_left_paired.fastq> <new_name_for_left_unpaired.fastq><new_name_for_right_paired.fastq> <new_name_for_right_unpaired.fastq> ILLUMINACLIP:<path_to_adaptors>:2:30:9 LEADING:2 TRAILING:2 SLIDINGWINDOW:4:15 MINLEN:25
`
