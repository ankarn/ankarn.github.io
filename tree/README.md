# How to build a phylogenetic tree

1. make alignment
2. trim alignment  
[trimal](http://trimal.cgenomics.org)  
`trimal -in aligned_seq.fasta -out name.trimal.fasta -gt 0.3 -st 0.001`

3. Fast Tree
4. [RAxML](https://sco.h-its.org/exelixis/web/software/raxml/hands_on.html)  

basic command for ML tree on nucleotide sequences with fast bootstrap  

`raxmlHPC-PTHREADS-SSE3 -m GTRCAT -c 25 -p 12345 -x 6789 -d -f d -N 100 -n name -s aln.trim.fasta`  

5. IQtree
6. PhyloBayes
