# PennCNV

PennCNV is a free software tool for Copy Number Variation (CNV) detection from SNP genotyping arrays. Currently it can handle signal intensity data from Illumina and Affymetrix arrays. With appropriate preparation of file format, it can also handle other types of SNP arrays and oligonucleotide arrays.

PennCNV implements a hidden Markov model (HMM) that integrates multiple sources of information to infer CNV calls for individual genotyped samples. It differs form segmentation-based algorithm in that it considered SNP allelic ratio distribution as well as other factors, in addition to signal intensity alone. In addition, PennCNV can optionally utilize family information to generate family-based CNV calls by several different algorithms. Furthermore, PennCNV can generate CNV calls given a specific set of candidate CNV regions, through a validation-calling algorithm.

This website is built for the "original" Perl/C-based PennCNV developed for SNP arrays (see references below). Other tools of the PennCNV family include [PennCNV2](https://github.com/WGLab/PennCNV2/) (C++ based PennCNV for tumor/NGS data) and [PennCNV3](https://github.com/WGLab/HadoopCNV) (Java/Hadoop-based PennCNV for NGS data).

## What's new:

- 20190109: A slightly updated PennCNV is provided in v1.0.5, to improve compatibility with recent version of GCC and Perl. If users still have problems in installation, please follow "last resort" guide and just install a new Perl 5.14.2 to run PennCNV.
- 20170606: Zoltan Kutalik shared an article on how to improve PENNCNV CNV calls [here](https://www.ncbi.nlm.nih.gov/pubmed/27402902). They defined a new quality score (QS) estimating the probability of a CNV called by PennCNV to be confirmed by other software.
- 20161024: Prof. George Kirov shared a recently published paper reporting the use of PennCNV on Affy Axiom arrays [here](http://www.sciencedirect.com/science/article/pii/S0006322316327111). Detailed procedure for CNV calling is given in the supplementary materials.
- 20160805: PennCNV has been dockerized by Roman Hillje at the University of Zurich, Switzerland. The docker image and related documentation are available at https://hub.docker.com/r/romanhaa/penncnv/. 

## Reference:

- Wang K, Li M, Hadley D, Liu R, Glessner J, Grant S, Hakonarson H, Bucan M. [PennCNV: an integrated hidden Markov model designed for high-resolution copy number variation detection in whole-genome SNP genotyping data](http://genome.cshlp.org/cgi/content/short/17/11/1665) _**Genome Research**_ 17:1665-1674, 2007
- Diskin SJ, Li M, Hou C, Yang S, Glessner J, Hakonarson H, Bucan M, Maris JM, Wang K. [Adjustment of genomic waves in signal intensities from whole-genome SNP genotyping platforms](http://nar.oxfordjournals.org/cgi/content/short/36/19/e126) **_Nucleic Acids Research_** 36:e126, 2008
- Wang K, Chen Z, Tadesse MG, Glessner J, Grant SFA, Hakonarson H, Bucan M, Li M. [Modeling genetic inheritance of copy number variations](http://nar.oxfordjournals.org/cgi/content/short/36/21/e138) _**Nucleic Acids Research**_ 36:e138, 2008 

Click the menu to the left to navigate through the PennCNV website.


