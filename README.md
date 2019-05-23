# Dif_expression_profiles_project

## Project description
## Aims 
 - get acquainted with methods of processing the differential expression data (R based - Phantasus, Limma, KEGGgraph, Pathview)
 - develop a searching algorithm for key genes that initialize a differential expression profile change in the cell
 - analyze and prove a biological relevance for obtained results
 
## Methods

### Data
1) experiment.xlsx - table of differentially expressed genes (threshold: p_value < 0.05)
2) gse_16357_001.xlsx - table of differentially expressed genes (threshold: p_value < 0.01)

### R Packages
 - KEGGgraph (sourse: https://bioconductor.org/packages/release/bioc/html/KEGGgraph.html)
 - gage (sourse: https://bioconductor.org/packages/release/bioc/html/gage.html)
 - KEGGREST (sourse: http://bioconductor.org/packages/release/bioc/html/KEGGREST.html)
### Databases
 - KEGG.db (sourse: http://bioconductor.org/packages/release/data/annotation/html/KEGG.db.html)


### Script description

## Results 
![](https://github.com/DariaGorbach/Dif_expression_profiles_project/blob/master/Result_Rplot.png?raw=true)

## Bibliography
1.	Gallaher, A. M., Das, S., Xiao, Z., Andresson, T., Kieffer-Kwon, P., Happel, C., & Ziegelbauer, J. (2013). Proteomic screening of human targets of viral microRNAs reveals functions associated with immune evasion and angiogenesis. PLoS Pathogens, 9(9), e1003584. 
2.	Liu, X., Happel, C., & Ziegelbauer, J. M. (2017). Kaposi’s Sarcoma-Associated Herpesvirus MicroRNAs Target GADD45B To Protect Infected Cells from Cell Cycle Arrest and Apoptosis. Journal of Virology, 91(3).
3.	Pan, H., Xie, J., Ye, F., & Gao, S.-J. (2006). Modulation of Kaposi’s sarcoma-associated herpesvirus infection and replication by MEK/ERK, JNK, and p38 multiple mitogen-activated protein kinase pathways during primary infection. Journal of Virology, 80(11), 5371–5382. 
4.	Tamura, R. E., de Vasconcellos, J. F., Sarkar, D., Libermann, T. A., Fisher, P. B., & Zerbini, L. F. (2012). GADD45 proteins: central players in tumorigenesis. Current Molecular Medicine, 12(5), 634–651.
5.	Veettil, M. V., Kumar, B., Ansari, M. A., Dutta, D., Iqbal, J., Gjyshi, O., … Chandran, B. (2016). ESCRT-0 Component Hrs Promotes Macropinocytosis of Kaposi’s Sarcoma-Associated Herpesvirus in Human Dermal Microvascular Endothelial Cells. Journal of Virology, 90(8), 3860–3872.
6.	Wang, Z., Sheng, C., Yao, C., Chen, H., Wang, D., & Chen, S. (2019). The EF-Hand Protein CALML6 Suppresses Antiviral Innate Immunity by Impairing IRF3 Dimerization. Cell Reports, 26(5), 1273–1285.e5. 

