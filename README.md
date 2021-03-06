# Identification of pathway genes triggered differential expression profile changes


## Project description
Analysis of complex cellular pathways can be an issue. However, despite dozens of possible interconnections between genes in the pathway, it only requires to know the few key genes, that invokes changes in differential expression profile. In recent work we managed to find key genes that orchestrate early changes in differential expression during the Kaposi’s sarcoma-associated herpesvirus (KSHV) invasion. 

## Aims 
 - get acquainted with methods of processing the differential expression data (R based - Phantasus, Limma, KEGGgraph, Pathview)
 - develop a searching graph algorithm for key genes that initialize a differential expression profile change in the cell
 - analyze and prove a biological relevance for obtained results
 
## Methods
We used the real clinical data from cells infected with KSHV - a table of differentially expressed genes, that was previously visualised and selected in the Phantasus software. Then, we intersected these genes with pathways from the KEGG ((Kyoto Encyclopedia of Genes and Genomes) database, to choose pathways, that contain genes of interest. 
Selected pathways were processed using the KEGGgraph R package. We applied so called "breadth-first search", as we search for every "	descendant gene"  of every single gene in the pathway and compared the number of differentially expressed ones amoung them. Gene, that has the biggest omount of those genes (and the lesser number of non-differentially expressed descendants) is considered to be "the key gene", that initiate following changes in that part of the pathway. 

### Data
1) experiment.xlsx - table of differentially expressed genes (threshold: p_value < 0.05)
2) gse_16357_001.xlsx - table of differentially expressed genes (threshold: p_value < 0.01)

### R Packages
 - KEGGgraph (sourse: https://bioconductor.org/packages/release/bioc/html/KEGGgraph.html)
 - gage (sourse: https://bioconductor.org/packages/release/bioc/html/gage.html)
 - KEGGREST (sourse: http://bioconductor.org/packages/release/bioc/html/KEGGREST.html)
### Databases
 - KEGG.db (sourse: http://bioconductor.org/packages/release/data/annotation/html/KEGG.db.html)
### Other tools 
 - Phantasus (sourse: https://artyomovlab.wustl.edu/phantasus/)
 - Pathview (sourse: https://pathview.uncc.edu/)

### Script description
Diff_expression_script.Rmd - script for differential expression data analysis, using graph approach

## Results 
 All genes from KSHV-infected cells data were intersected with KEGG database (KEGG.db) and, as a result, 143 pathways possibly related with KSHV were obtained. 
 We run our script and got a list of genes, significantly presented amoung all pathways. Top 6 most significant genes showed on the plot below.
 
![](https://github.com/DariaGorbach/Dif_expression_profiles_project/blob/master/Result_Rplot.png?raw=true)

## Future aims
 - optimize working function: mind secondary metabolites, cyclic pathways, several possible key genes within one pathway "chain" ( for example, 	disconnected by three or more non-differentially expressed genes)
 - try to apply already working aihorithm on other viral infection cellular profiles                           


## Bibliography
1.	Gallaher, A. M., Das, S., Xiao, Z., Andresson, T., Kieffer-Kwon, P., Happel, C., & Ziegelbauer, J. (2013). Proteomic screening of human targets of viral microRNAs reveals functions associated with immune evasion and angiogenesis. PLoS Pathogens, 9(9), e1003584. 
2.	Liu, X., Happel, C., & Ziegelbauer, J. M. (2017). Kaposi’s Sarcoma-Associated Herpesvirus MicroRNAs Target GADD45B To Protect Infected Cells from Cell Cycle Arrest and Apoptosis. Journal of Virology, 91(3).
3.	Pan, H., Xie, J., Ye, F., & Gao, S.-J. (2006). Modulation of Kaposi’s sarcoma-associated herpesvirus infection and replication by MEK/ERK, JNK, and p38 multiple mitogen-activated protein kinase pathways during primary infection. Journal of Virology, 80(11), 5371–5382. 
4.	Tamura, R. E., de Vasconcellos, J. F., Sarkar, D., Libermann, T. A., Fisher, P. B., & Zerbini, L. F. (2012). GADD45 proteins: central players in tumorigenesis. Current Molecular Medicine, 12(5), 634–651.
5.	Veettil, M. V., Kumar, B., Ansari, M. A., Dutta, D., Iqbal, J., Gjyshi, O., … Chandran, B. (2016). ESCRT-0 Component Hrs Promotes Macropinocytosis of Kaposi’s Sarcoma-Associated Herpesvirus in Human Dermal Microvascular Endothelial Cells. Journal of Virology, 90(8), 3860–3872.
6.	Wang, Z., Sheng, C., Yao, C., Chen, H., Wang, D., & Chen, S. (2019). The EF-Hand Protein CALML6 Suppresses Antiviral Innate Immunity by Impairing IRF3 Dimerization. Cell Reports, 26(5), 1273–1285.e5. 

