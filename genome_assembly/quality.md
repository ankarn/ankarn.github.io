# Estimation of the genome assembly

1. [QUAST](http://bioinf.spbau.ru/quast)  
Useful tool for comparison of basic metrics of assemblies  

`quast.py assembly_file`  

Output  

N50  

2. bandage

3. mapping reads 

[bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)   

generowanie indeksu   
`bowtie2-build <genom.fasta> <nazwa indeksu>`   

`bowtie2 -x <nazwa indeksu> -1 <ścieżka dostępu/reads_1.fq> -2 <ścieżka dostępu/reads_2.fq> -S <nazwa.sam>`   
 
dla odczytów połączonych (np. po obróbce w programie PEAR) komenda:   
 
`bowtie2 -x <nazwa indeksu> -U <ścieżka dostępu/reads.fq> -S <nazwa.sam>`   

[STAR](https://github.com/alexdobin/STAR)   

utworzyć folde, w którym będzie indeks
`mkdir <nazwa>`

generowanie indeksu   
`/home/ankarn/bin/STAR-2.5.3a/bin/Linux_x86_64/STAR --runThreadN n --runMode genomeGenerate --genomeDir <ścieżka do folderu z indeksem> --limitGenomeGenerateRAM 166028754304 --genomeFastaFiles <ścieżka do assembly genomu>`   

mapowanie   
`/home/ankarn/bin/STAR-2.5.3a/bin/Linux_x86_64/STAR --runThreadN 16 --genomeDir <ścieżka indeks> --readFilesIn <ścieżka_lewy_odczyt> <ścieżka prawy odczyt> --outFileNamePrefix <ścieżka i prefix do output> --outSAMtype BAM SortedByCoordinate`
