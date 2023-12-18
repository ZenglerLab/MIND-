# Niche Determination (ND) in a SynCom

_Note: The following scripts need to be run in sequence._  

_Note: Script_ ```1.MiND_Prediction_Substrate_Preferences.Rmd``` _also requires the output of script_ ```1.multiomics_customindex_dataprep.Rmd``` _from subdirectory __1. Guild-Based Microbiome Classification and Predictions of Competition in a SynCom__ of this repository. See details below._
  
_Note: Before running these scripts, users should modify the path of any data table import or export to match location of corresponding files in their system_ 

***

## Overview

This section contains scripts and data used to perform __microbial Niche Determination (ND)__ and __predict substrate preferences__ in a 16-member synthetic community (SynCom) based on translational efficiency (TE = metaRibo-Seq / metaRNA-Seq).   
It also contains results of experimental results of experimental prebiotic experiments used to validate niches-based predictions of substrate preferences. 

### Experiment overview  

Multi-omics analysis of a 16-member synthetic community (SynCom) grown in complex medium (see Moyne et _al._, 2023 manuscript for details).  

Multi-omics analysis included:  
- metagenomics (metaG)  
- metatranscriptomics (metaT)  
- metaRibo-Seq (metaRS)  

### Bioinformatics processing overview  

Data tables used in this directory were obtained through bioinformatic processing of the sequencing data. For more information about sequencing data processing, please refer to the associated manuscript. 


***

## Scripts contents overview

### 1.MiND_Prediction_Substrate_Preferences.Rmd

__Input File(s):__  

- ```Final_18_strains_with_strainN.saf```  
- Output from previous script from directory __1. Microbial Interactions (MI) in a SynCom__: ```1.multiomics_customindex_dataprep.Rmd```

__Overview:__  
__Microbial Niche Determination (ND) algorithm__. Niches define each microbe's preferred substrates based on the import proteins they prioritize, according to Translational Efficiency (TE = metaRibo-Seq / metaRNA-Seq) measurements.

This script notably produces manuscript Figure 4b-d, as well as Supp. Fig. S3. 

### 2.Prebiotics_Experiment_metaG_dataprep.Rmd

__Input File(s):__  
```
- Prebiotics_SynCom_metaG_count_table.tsv
- Final_18_strains_with_strainN.saf 
```

__Overview:__  
Filtering, normalization and formatting of count tables obtained after bioinformatic processing of metagenomics sequencing data.  
This dataset contains the __results of a prebiotics experiment carried out in the SynCom__, with __prebiotic interventions designed based on ND__ (see previous script: ```1.MiND_Prediction_Substrate_Preferences.Rmd```.     
This script outputs a table which will be used as the input for the subsequent script ('write' command at the end of the script must be enabled).  


### 3.Prebiotics_Experiment_metaG_taxonomy_analysis.Rmd

__Input File(s):__ 
- Output from previous script: ```2.Prebiotics_Experiment_metaG_dataprep.Rmd```

__Overview:__  
Statistical analysis of prebiotic experiments results.  
To test niche-based predictions of substrate preferences, we experimentally supplemented the SynCom culture medium with substrates identified as niche for SynCom members evaluated the effect on metagenomics relative abundance of all members.  

This script produces manuscript Figure 4e-j and Supp. Fig. S4. 




