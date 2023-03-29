# Guild-Based Microbiome Classification and Predictions of Competition in a SynCom  

_Note: The following scripts need to be run in sequence._  
_Note: Before running these scripts, users should modify the path of any data table import or export to match location of corresponding files in their system_ 

*** 

## Overview

This section contains scripts and data used to determine __microbial guilds__ and __predict competition__ in a 16-member synthetic community (SynCom) based on translational efficiency (TE = metaRibo-Seq / metaRNA-Seq).  
It also contains results of experimental dropout experiments used to validate guild-based predictions of competition interactions.  

### Experiment overview  

Multi-omics analysis of a 16-member synthetic community (SynCom) grown in complex medium (see Moyne et _al._, 2023 manuscript for details).  

Multi-omics analysis included:  
- metagenomics (metaG)  
- metatranscriptomics (metaT)  
- metaRibo-Seq (metaRS)  

This directory includes statistical analysis of multiomics sequencing data from the SynCom, notably __Microbial Guilds Classification__ and __prediction of competition__ interactions between SynCom members.  

It also contains statistical analysis of multiomics and metagenomics sequencing data of __experimental dropout__ experiments used to validate guild-based competition predictions.  

### Bioinformatics processing overview  

Data tables used in this directory were obtained through bioinformatic processing of the sequencing data. For more information about sequencing data processing, please refer to Moyne et _al._, 2023.  

***

## Scripts contents overview

### 1.multiomics_customindex_dataprep.Rmd  

__Input File(s):__  
```
- Final_18_strains_with_strainN.saf  
- 18_strains_genenames.txt  
- 18_genomes_KEGG_BlastKOALA.csv  
- FINAL_SynCom_modifs_multiomics_count_table_formatted.tsv  
- Final_18_strains_with_strainN.saf  
```

__Overview:__  
Filtering, normalization and formatting of count tables obtained after bioinformatic processing of multi-omics sequencing data.  
This dataset contains multiomics count table from the SynCom, as well as a first round of single-member dropout experiments carried out in the SynCom.  
This script outputs a table which will be used as the input for the subsequent scripts ('write' command at the end of the script must be enabled).  


### 2.SynCom_Guild_classification_Competition_prediction.Rmd 

__Input File(s):__  
- Output from previous script: ```1.multiomics_customindex_dataprep.Rmd```

__Overview:__  
__Guild-Based Microbiome Classification algorithm__. Guilds classify microbes based the metabolic pathways they prioritize, according to Translational Efficiency (TE = metaRibo-Seq / metaRNA-Seq) measurements.  

Guild classification allowed to calculate a __competition score__ and __predict competition__ between SynCom members.  

This script produces manuscript Figures 1b, 1c, 2c, 2d, as well as several supplementary figures and tables. 


### 3.Dropout_SynCom_Expt1_metaG_taxonomic_abundances.Rmd

__Input File(s):__ 
- Output from previous script: ```1.multiomics_customindex_dataprep.Rmd```

__Overview:__  
Statistical analysis of experimental dropout experiments results (first experiment).  
To test guild-based predicted competitive interactions, we experimentally dropped out individual members from the SynCom and evaluated the effect on relative abundance of the remaining 15 members.  

This script produces manuscript Figure 2e (subset) and Supp. Fig. S6. 


***

### 4.metaG_customindex_abundances_second_dropout_experiment_dataprep.Rmd

__Input File(s):__  
```
- Dropout_expt2_Syncom_metaG_count_table.tsv  
- Final_18_strains_with_strainN.saf  
```

__Overview:__  
Filtering, normalization and formatting of count tables obtained after bioinformatic processing of metagenomics sequencing data.  
This new dataset contains results of a second round of experimental dropout experiments carried out in the SynCom (single- and double-member dropout). 



***

### 5.metaG_customindex_abundances_second_dropout_experiment.Rmd

__Input File(s):__ 
- Output from previous script: ```4.metaG_customindex_abundances_second_dropout_experiment_dataprep.Rmd```

__Overview:__  
Statistical analysis of experimental dropout experiments results (second experiment).  
To test guild-based predicted competitive interactions, we experimentally dropped out one or two individual members from the SynCom and evaluated the effect on relative abundance of the remaining members.  

This script produces manuscript Figure 2e (subset) and Supp. Fig. S7 a, d, e, h. 

