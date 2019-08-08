# How to build a phylogenetic tree

1. make alignment
2. trim alignment  
[trimal](http://trimal.cgenomics.org)  
`trimal -in aligned_seq.fasta -out name.trimal.fasta -gt 0.3 -st 0.001`

3. Fast Tree
4. [RAxML](https://sco.h-its.org/exelixis/web/software/raxml/hands_on.html)  

basic command for ML tree on nucleotide sequences with fast bootstrap  

`raxmlHPC-PTHREADS-SSE3 -T 4 -m GTRCAT -c 25 -e 0.001 -p 31415 -f a -N 100 -x 02938 -n name -s name.aln.fas`

5. [raxml-ng](https://github.com/amkozlov/raxml-ng)

`raxml-ng --all --msa DNA.fa --model GTR+G --tree pars{20} --bs-trees 1000`

Tree with bootstrap:  `DNA.fa.raxml.support`

Actual version 0.9.0 available on conda (--instal raxml-ng).

6. IQtree
7. PhyloBayes
