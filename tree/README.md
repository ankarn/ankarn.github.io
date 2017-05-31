# How to build a phylogenetic tree

1. make alignment
2. trim alignment  
[trimal](http://trimal.cgenomics.org)  
`trimal -in aligned_seq.fasta -out name.trimal.fasta -gt 0.3 -st 0.001`

3. Fast Tree
4. [RAxML](https://sco.h-its.org/exelixis/web/software/raxml/hands_on.html)  

basic command for ML tree on nucleotide sequences with fast bootstrap  

`raxmlHPC -f a -m GTRCAT -p 12345 -x 12345 -# 100 -s name.aln.fasta -n name`  

5. IQtree
6. PhyloBayes
