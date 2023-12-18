# MIND in a soil microcosm

_Note: The following scripts need to be run in sequence._  
_Note: Before running these scripts, users should modify the path of any data table import or export to match location of corresponding files in their system_ 

*** 

## Overview

This section contains scripts and data used to determine __microbial functional profiles__ and __predict competition and substrate preferences__ in a 16-member synthetic community (SynCom) grown in a soil microcosm based on translational efficiency (TE = metaRibo-Seq / metaRNA-Seq).  
It also contains results of prebiotic and probiotic experiments used to validate MIND predictions.  

### Experiment overview  

Multi-omics analysis of a __16-member SynCom grown together with soil__ in complex medium (see Moyne et _al._ manuscript for details).  

Multi-omics analysis included:  
- metagenomics (metaG)  
- metatranscriptomics (metaT)  
- metaRibo-Seq (metaRS)  


### Bioinformatics processing overview  

Data tables used in this directory were obtained through bioinformatic processing of the sequencing data. For more information about sequencing data processing, please refer to the associated manuscript. 

***

## Scripts contents overview

### 1.multiomics_customindex_dataprep.Rmd  

__Input File(s):__  
```
- 18_strains_genenames.txt  
- 18_genomes_KEGG_BlastKOALA.csv  
- MIND_Soil_SynCom_customindex_Expt2_count_table.tsv  
- Final_18_strains_with_strainN.saf  
```

__Overview:__  
Filtering, normalization and formatting of count tables obtained after bioinformatic processing of multi-omics sequencing data.  
This script outputs a table which will be used as the input for the subsequent scripts ('write' command at the end of the script must be enabled).  


### 2.MI_SynCom_in_soil_microcosm.Rmd 

__Input File(s):__  
- Output from previous script: ```1.multiomics_customindex_dataprep.Rmd```

__Overview:__  
Comparison of microbes functional profiles allowed to calculate a __competition score__ and __predict competition__ between SynCom members hwne grown in a soil microcosm.  

This script produces manuscript Figure 5b and Suppl. Figure S5a. 


### 3.ND_SynCom_in_soil_microcosm.Rmd

__Input File(s):__ 
- Output from previous script: ```1.multiomics_customindex_dataprep.Rmd```

__Overview:__  
Microbial Niche Determination (ND) algorithm. Niches define each microbe's preferred substrates based on the import proteins they prioritize, according to Translational Efficiency (TE = metaRibo-Seq / metaRNA-Seq) measurements.

This script produces manuscript Suppl. Figure S5b. 


***

### 4.Soil_microcosm_prebiotic_probiotic.Rmd

__Input File(s):__  
```
- Soil_pre_pro_biotics_wolsubset_ogu.tsv  
- lineage.txt (part of the Web of Life database, download from: https://biocore.github.io/wol/)  
```

__Overview:__  
Statistical analysis of experimental prebiotic and probiotic experiments carried out in a soil microcosm. 
To test MIND predictions, we experimentally supplemented the soil microcosm culture medium with a prebiotic, a probiotic, a probiotic consortium, or combinations thereof. See details in Moyne et _al._ manuscript.


This script notably produces manuscript Figures 5c and Suppl. Fig. S6. 


