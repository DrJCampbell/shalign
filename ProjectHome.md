This is the source code for the software referred to in Sims et al. 2011 High-throughput RNA interference screening using pooled shRNA libraries and next generation sequencing (Genome Biology 2011, 12:[R104](https://code.google.com/p/shalign/source/detail?r=104) doi:10.1186/gb-2011-12-10-[r104](https://code.google.com/p/shalign/source/detail?r=104))

To use the software, first compile distance.c using gcc and save the program in the same directory as the shalign.pl perl script.

The perl script take options from the command line to define a project number, a list of screening library sequence files and a list of fastq files.

The project number is arbitrary value chosen by the user. The fastq files should each contain hairpin reads from a given pool of hairpins. The files are specified as a comma-separated list. The list of screening library sequence files (comma-separated list) must be in the same order with respect to pools as the fastq files were supplied.

for example:
```
perl ~/scripts/shALIGN/shalign.pl \
--project 047 \
--libraries \
~/scripts/shALIGN/ScreeningPool/CSHL_101-200.txt,\
~/scripts/shALIGN/ScreeningPool/CSHL_301-400.txt,\
~/scripts/shALIGN/ScreeningPool/CSHL_401-500.txt \
--fastqfiles \
~/NGS/FASTQ/shrna_YF/T1_pool2/R1.fq,\
~/NGS/FASTQ/shrna_YF/T1_pool4/R1.fq,\
~/NGS/FASTQ/shrna_YF/T1_pool5/R1.fq
```
