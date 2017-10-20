# Merging reads

That is an optional step, very useful with PE reads over 250bp for transcriptome assemblies; otherwise, this part can be skipped as 100 or 150-nucleotide-long reads simply would not merge.

[PEAR](http://sco.h-its.org/exelixis/web/software/pear/)  

`pear -f left.fastq -r right.fastq -o output`

Usage: use at non-trimmed reads with removed adaptors
