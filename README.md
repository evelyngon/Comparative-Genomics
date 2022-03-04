# Comparative-Genomics
Indentification of critical mutation in comparative genomics analyisis and metabolic networks

The rapid development of high throughput sequencing techniques leads to huge amount of new genomes (most of the time, unfinished draft genomes) to study. The development of automatic tools to analyze those genomes becomes crucial to speed up research and select potential biochemical targets. 

Genome sequencing projects involve several steps downstream of the genome assembly. The first step is the gene prediction and functional annotation of those genes. Several other steps include the Gene Ontology [1] mapping, followed by metabolic networks analysis in order to identify the potential missing pathways or extra branches in some pathways. However, in many cases the simple presence/absence of a gene is not sufficient. Only a few of the current methods target the identification of critical mutations within genes that would affect a pathway (e.g., PRIAM, CCD) [2, 3]. This identification requires further extensive manual analysis of each predicted protein.

In this project, we have been developing a method capable of helping to identify critical residues potentially implicated in a phenotype when comparing two or more very closely related genomes (e.g., two clones of the same genome). We have used position-specific differential HMM (hidden markov models [4]) scoring of the InterPro [5] domain predictors for a direct comparison between orthologous genes. Our method has been detecting slight changes in the scores when mapping HMMs onto closely related proteins and comparing the variations of the score by positions allowing for the identification of potential critical mutations. We have also been using local PSSM (Position Specific Scoring Matrices) around mutated residues to evaluate their conservation among other more distant species.

In addition to this, since many critical residues are highly variable, other methods like positive-selection or purifying selection [6-9] and correlated mutations [10-12] are being used cooperatively with our results leading to a consensus prediction. This consensus prediction method combines those independent tools taking advantage of the strengths of each one of them. 

This method has been applied both to prokaryote and eukaryote genomes and only depend on the availability of good domain predictors. Those predictors do not even need to be defined on well know functional domains, for example even unknown conserved regions could be analyzed to predict potential critical mutations.
In addition, we will also benefit from close contacts with the PROSITE team [13] of the Swiss-Prot group in Geneva [14], to include internally developed “rules” that are extremely useful to automate the annotation of proteins. These “rules” describe additional information within protein domains such as critical residues (active sites, binding sites, modifications sites etc…) [15].

To evaluate the results, we built a specific test set with known critical and random mutations, based on the extensive use of high quality Swiss-Prot annotations (e.g., two or more E.coli proteomes). The method has been applied onto real genomic data through several collaborations.


References
1.	consortium: The Gene Ontology in 2010: extensions and refinements. Nucleic Acids Res 2010, 38(Database issue):D331-335.
2.	Claudel-Renard C, Chevalet C, Faraut T, Kahn D: Enzyme-specific profiles for genome annotation: PRIAM. Nucleic Acids Res 2003, 31(22):6633-6639.
3.	Marchler-Bauer A, Anderson JB, Chitsaz F, Derbyshire MK, DeWeese-Scott C, Fong JH, Geer LY, Geer RC, Gonzales NR, Gwadz M et al: CDD: specific functional annotation with the Conserved Domain Database. Nucleic Acids Res 2009, 37(Database issue):D205-210.
4.	Baldi P, Chauvin Y, Hunkapiller T, McClure MA: Hidden Markov models of biological primary sequence information. Proc Natl Acad Sci U S A 1994, 91(3):1059-1063.
5.	Hunter S, Apweiler R, Attwood TK, Bairoch A, Bateman A, Binns D, Bork P, Das U, Daugherty L, Duquenne L et al: InterPro: the integrative protein signature database. Nucleic Acids Res 2009, 37(Database issue):D211-215.
6.	Capra JA, Singh M: Characterization and prediction of residues determining protein functional specificity. Bioinformatics 2008, 24(13):1473-1480.
7.	Klopman G, Dimayuga M, Talafous J: META. 1. A program for the evaluation of metabolic transformation of chemicals. J Chem Inf Comput Sci 1994, 34(6):1320-1325.
8.	Talafous J, Sayre LM, Mieyal JJ, Klopman G: META. 2. A dictionary model of mammalian xenobiotic metabolism. J Chem Inf Comput Sci 1994, 34(6):1326-1333.
9.	Ye K, Vriend G, AP IJ: Tracing evolutionary pressure. Bioinformatics 2008, 24(7):908-915.
10.	Horner DS, Pirovano W, Pesole G: Correlated substitution analysis and the prediction of amino acid structural contacts. Brief Bioinform 2008, 9(1):46-56.
11.	Miller CS, Eisenberg D: Using inferred residue contacts to distinguish between correct and incorrect protein models. Bioinformatics 2008, 24(14):1575-1582.
12.	Rubinstein R, Fiser A: Predicting disulfide bond connectivity in proteins by correlated mutations analysis. Bioinformatics 2008, 24(4):498-504.
13.	Sigrist CJ, Cerutti L, de Castro E, Langendijk-Genevaux PS, Bulliard V, Bairoch A, Hulo N: PROSITE, a protein domain database for functional characterization and annotation. Nucleic Acids Res 2010, 38(Database issue):D161-166.
14.	Schneider M, Lane L, Boutet E, Lieberherr D, Tognolli M, Bougueleret L, Bairoch A: The UniProtKB/Swiss-Prot knowledgebase and its Plant Proteome Annotation Program. J Proteomics 2009, 72(3):567-573.
15.	Sigrist CJ, De Castro E, Langendijk-Genevaux PS, Le Saux V, Bairoch A, Hulo N: ProRule: a new database containing functional and structural information on PROSITE profiles. Bioinformatics 2005, 21(21):4060-4066.
16.	Kanehisa M, Goto S, Furumichi M, Tanabe M, Hirakawa M: KEGG for representation and analysis of molecular networks involving diseases and drugs. Nucleic Acids Res 2010, 38(Database issue):D355-360.

