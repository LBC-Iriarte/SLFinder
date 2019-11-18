# SLFinder
SL Finder is a four step pipeline of bioinformatic analyses meant to identify putative Spliced Leader (pSL) sequences from Transcriptome data assembled de novo, without making use of known SL sequences and requiring minimal manual manipulaion of the data by the user:

#### SLFinder-step0
Filters a Trinity assemblies and retrieves the firsts and last XX bases of the longer isoform of each assembled gene. According to Trinity contig naming convention.

#### SLFinder-step1
Creates and evaluates “Hook” sequences that more likely represent SLs and retrieves contig regions, either in the 3’ or 5’ region for further analyses.

#### SLFinder-step2
Aligns the sequences identified for each hook and automatically trims them remove noise as much as possible (Depending of your data this step might require your direct intervention)

#### SLFinder-step3
Blast the pSL sequences against a reference transcriptome looking to verify their sequence and identify their coding location and copy number and identify the transcripts with validated pSL variants. If provided, it uses an external reference to annotate the genomic region with each SLps and discard those with matches.

Detailed instructions of how to run to control the SL search can be find on the SLFinder_manual.pdf

## Necesary programs:
The pipeline requires a BASH enviroment to run (i.e. UBUNTU) and the following programs installed and in the PATH:

Ncbi-blast: https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download
Cd-Hit: https://github.com/weizhongli/cdhit
Jellyfish: https://github.com/gmarcais/Jellyfish
MAFFT: https://mafft.cbrc.jp/alignment/software/source.html
Salmon: https://github.com/COMBINE-lab/salmon
Seqkit: https://github.com/shenwei356/seqkit
Trinity: https://github.com/trinityrnaseq/trinityrnaseq/wiki
Trimal: http://trimal.cgenomics.org/trimal
Weblogos: http://weblogo.berkeley.edu/

## Instalation
SLFinder's scripts does not require compiling, only be granded execution permisions with the following command:

chmod +x SLFinder-step*

## Citation:
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
