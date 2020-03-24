#Study of Restorer of Fertility PPR gene cluster in 26 Maize NAM lines

###_Background_
Cytoplasmic male sterility, CMS, is a naturally occurring phenomenon found in many plant species caused by an incompatibility between the mitochondrial and nuclear genomes leading to accumulation of CMS products in the inner mitochondrial membrane, finally resulting in cell death. _Restorer of fertility (Rf)_ genes coded in the nuclear genome are responsible for reducing the accumulation of the CMS products. Frequently, these _Rf_ genes are pentatricopeptide repeat (PPR) encoded proteins, a class of RNA binding proteins involved in post-transcriptional processing in the mitochondria and chloroplast. Restorer of fertility PPR proteins contain tandem repeats of degenerate 35 amino acids motifs. Within the PPR motif, amino acids in positions 5 and 35 interact the RNA strand and are responsible for RNA-binding specificity. Rf PPR proteins are characterized by a high number of PPR motifs, diversifying selection, and are often found in gene clusters (Fujii, et al. 2011).

The maize genome contains an important _Rf_ PPR gene cluster on the long arm of chromosome 2. This cluster contains the _Rf3_ gene, the major dominant restorer for CMS-S, found in the NAM inbred Ky21. In certain inbreds, this cluster also contains an _Rf_ gene for CMS-C cytoplasm (unpublished research). From my initial analysis, the NAM lines contain between 3 and 9 highly similar PPR genes each with 19 PPR motifs. These genes of ~2400 bp in length each differ by ~30 to 40 SNPs. These PPR genes may show higher divergence at amino acids 5 and 35, which determine its PPR code.   

###_Purpose_
The purpose of this analysis is to determine the PPR gene content of this chr2 PPR cluster within the diverse NAM lines. I plan to look at the expansion and diversification of this gene cluster within the NAM lines, in particular the type of PPR genes most likely to be the causal _Rf_ genes. I plan to group the genes by similarity, determine their PPR code, and calculate the rate of divergence at each amino acid position. The end goal is to identify the PPRs unique to KY21 which could be the causal _Rf3_ gene, and also to find the possible CMS-C causal _Rf_ gene.
 
###_Analysis Outline_
1. Identify PPR genes within the chr2 cluster in the NAM lines _I worked on steps 1.1 to 1.5 over the past 2 weeks. It took longer than you would expect, since I am novice level._
	1. Blast flanking markers to find flanking physical interval on chr2 within each NAM line. _The interval size was between 2.9 MB and 3.8 MB for the NAM lines, suggesting occurrences of unequal crossing over and genome rearrangments_
	2. Grep gene names to get only genes within the chr2 interval in GFF
	3. Grep proteins in interval from fasta file
	4. Run HMMer with PPR motifs to identify PPR genes within interval
	5. Grep PPR proteins and PPR transcripts for genes within the interval from fasta files
	
	
2. Analyze PPR gene content of NAM lines
	1. Align mRNA sequence of every PPR gene (using MAFTT?)
	2. Calculate mRNA similarity between every PPR gene to determine which genes are related (don't know which program I'll use yet)
	3. Make a phylogenic tree of genes to show relatedness between PPR gene groups
	4. Determine which NAM lines have the same gene content; which NAM lines have unique PPR genes; etc
	5. Determine the PPR code of each gene, ie, the amino acid at positions 5 & 35 using python script "PPRCODE" from Yan et al. 2019
	6. Find causal _Rf3_ gene for CMS-S and _Rf_ gene for CMS-C

3. Analyze diversifying selection of PPR genes
	1. Maybe calculate Ka/Ks (maybe using PAML?)
	2. Maybe calculate Shannon entropy of each amino acid position 
	3. Determine if amino acid positions 5 and 35 show selection pressure. Do any other positions show selection? 


Fujii, S., C. S. Bond and I. D. Small (2011). "Selection patterns on restorer-like genes reveal a conflict between nuclear and mitochondrial genomes throughout angiosperm evolution." Proc Natl Acad Sci U S A 108(4): 1723-1728.

Yan, J., Y. Yao, S. Hong, Y. Yang, C. Shen, Q. Zhang, D. Zhang, T. Zou and P. Yin (2019). "Delineation of pentatricopeptide repeat codes for target RNA prediction." Nucleic Acids Res 47(7): 3728-3738.