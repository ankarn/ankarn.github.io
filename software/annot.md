# Annotation tools #

1. [Signalp](http://www.cbs.dtu.dk/services/SignalP/)  

`signalp -m fasta-file [options]`

`/usr/local/bin/signalp`

SignalP 4.1 predicts the presence and location of signal peptide cleavage sites in amino acid sequences from different organisms: Gram-positive prokaryotes, Gram-negative prokaryotes, and eukaryotes. The method incorporates a prediction of cleavage sites and a signal peptide/non-signal peptide prediction based on a combination of several artificial neural networks.


2. [Targetp](http://www.cbs.dtu.dk/services/TargetP/)

`/home/halakuc/bin/targetp -P/-N (plant/non-plant) input [> output]`

`/home/halakuc/bin/targetp`

TargetP 1.1 predicts the subcellular location of eukaryotic proteins. The location assignment is based on the predicted presence of any of the N-terminal presequences: chloroplast transit peptide (cTP), mitochondrial targeting peptide (mTP) or secretory pathway signal peptide (SP).

For the sequences predicted to contain an N-terminal presequence a potential cleavage site can also be predicted.

NOTE 1:   TargetP uses ChloroP and SignalP to predict cleavage sites for cTP and SP, respectively. 


3. [ChloroP](http://www.cbs.dtu.dk/services/ChloroP/)

`/home/halakuc/bin/chlorop`

The ChloroP server predicts the presence of chloroplast transit peptides (cTP) in protein sequences and the location of potential cTP cleavage sites.


4. [tmhmm](http://www.cbs.dtu.dk/services/TMHMM/)

`/home/halakuc/software/tmhmm-2.0c/bin/tmhmm`

This program is for prediction of transmembrane helices in proteins.

