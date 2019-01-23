# How to build a phylogenetic tree

1. make alignment
2. trim alignment  
[trimal](http://trimal.cgenomics.org)  
`trimal -in aligned_seq.fasta -out name.trimal.fasta -gt 0.3 -st 0.001`

3. Fast Tree
4. [RAxML](https://sco.h-its.org/exelixis/web/software/raxml/hands_on.html)  

basic command for ML tree on nucleotide sequences with fast bootstrap  

`raxmlHPC-PTHREADS-SSE3 -T 4 -m GTRCAT -c 25 -e 0.001 -p 31415 -f a -N 100 -x 02938 -n name -s name.aln.fas`

5. IQtree
6. PhyloBayes


# How to view a phylogenetic tree

1. [FigTree](http://tree.bio.ed.ac.uk/software/figtree/)
In case it is not running, you can try [experimental version](https://github.com/rambaut/figtree/releases/tag/v1.4.4pre20171111).
