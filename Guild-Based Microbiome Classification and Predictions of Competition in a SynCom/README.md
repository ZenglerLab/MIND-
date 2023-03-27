<h4> <p align ="center"> Guild-Based Microbiome Classification and Predictions of Competition in a SynCom </p> </h4>

_Note: The following scripts need to be run in sequence._  
_Note: Before running these scripts, users should modify the path of any data table import or export to match location of corresponding files in their system_ 

*** 

Data overview: Samples, experiment description

***  

Example code to process sequencing data and obtain input files.


***

### 1.multiomics_customindex_dataprep.Rmd  

This script performs filtering, normalization and formatting of count tables obtained after bioinformatic processing of multi-omics sequencing data.  

__Input File(s):__  
- Final_18_strains_with_strainN.saf  
- 18_strains_genenames.txt  
- 18_genomes_KEGG_BlastKOALA.csv  
- FINAL_SynCom_modifs_multiomics_count_table_formatted.tsv  
- Final_18_strains_with_strainN.saf  

__Overview:__  
Filtering, normalization and formatting of multiomics sequencing data.  
Genomes were annotated with the KEGG database using BlastKOALA (Kanehisa et al. 2016).  
This script outputs a table which will be used as the input for the subsequent scripts ('write' command at the end of the script must be enabled).  

***

### 2.SynCom_Guild_classification_Competition_prediction.Rmd  

__Input File(s):__  
- Output from previous script: 1.multiomics_customindex_dataprep.Rmd

__Overview:__  
Guild-Based Microbiome Classification algorithm. Guilds classify microbes based the metabolic pathways they prioritize, according to Translational Efficiency (TE = metaRibo-Seq / metaRNA-Seq) measurements.  
This script produces manuscript figures 1b, 1c, 2c, 2d, as well as several supplementary figures and tables. 


***

### 3.Dropout_SynCom_Expt1_metaG_taxonomic_abundances.Rmd

__Input File(s):__ 
- Output from previous script: 1.multiomics_customindex_dataprep.Rmd

__Overview:__  

Predicting community microbe interactions in soil (competitions and dropouts). Figure 2b and part of Figure 2e and Supplementary Figures S1a and S6 were generated.




***

### 4.metaG_customindex_abundances_second_dropout_experiment_dataprep.Rmd
##### Input File(s): Dropout_expt2_Syncom_metaG_count_table.tsv, Final_18_strains_with_strainN.saf

Data cleaning and normalization of experimental results of community microbe interactions in soil (competitions and dropouts).




***

### 5.metaG_customindex_abundances_second_dropout_experiment.Rmd
##### Input File(s): Output from script 4

Experimental community microbal competition and dropout results were analyzed. Figure 2e and Supplementary Figures S7h and S7d were generated.


