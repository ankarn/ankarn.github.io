# Gene  prediction  

de novo gene prediction Augustus  


# Functional annotation  

1. genome
2. organellar genome
3. transcriptome

## blast  

## hmmer  
### 1. Basic usage (???)
### 2. Searching proteins.fasta with hmm profiles
There is a pair of scripts in `/home/halakuc/scripts`:
* `hmmer_them_all.sh`
Usage: hmmer_them_all.sh -p proteins.fasta --profiles profile1.hmm \[profile#.hmm\] -o outdir
* `hmmer_parser.py`
Helper script for the first one.

They produce following output (in outdir):
* proteins_profile#.out - text output of hmmer
* proteins_profile#.tblout - table output of hmmer
* proteins_interesting.fasta - fasta containing all significant hits, header contains protein name and hmmer profile name

## kegg  

## pfam  


