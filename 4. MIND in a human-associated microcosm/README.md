# MIND in a human-associated microcosm

_Note: The following scripts need to be run in sequence._  
_Note: Before running these scripts, users should modify the path of any data table import or export to match location of corresponding files in their system_ 

*** 

## Overview

This section contains scripts and data used to determine __microbial functional profiles__ and __predict competition and substrate preferences__ in a human-associated microcosm based on translational efficiency (TE = metaRibo-Seq / metaRNA-Seq).  
It also contains results of prebiotic experiments used to validate MIND predictions.  

### Experiment overview  

Multi-omics analysis of a __human microbiome from infant fecal sample__ grown in complex medium (see Moyne et _al._ manuscript for details).  

Multi-omics analysis included:  
- metagenomics (metaG)  
- metatranscriptomics (metaT)  
- metaRibo-Seq (metaRS)  


### Bioinformatics processing overview  

Data tables used in this directory were obtained through bioinformatic processing of the sequencing data. For more information about sequencing data processing, please refer to the associated manuscript. 

***

## Scripts contents overview

### 1.MI_Human_fecal_microbiome.Rmd 

__Input File(s):__  
```
- counts_species_uniref.tsv
- ko_kegg_uniref_pathway_manuallycurated.tsv (from the Web of Life database. original downloaded from: https://biocore.github.io/wol/)
- kegg_classification_grouped_by_CAT_PATH_format8.csv
```

__Overview:__  
Comparison of microbes functional profiles allowed to calculate a __competition score__ and __predict competition__ between microbiome members grown in a human-associated microcosm.  


### 2.1.ND_Human_fecal_microbiome_PROKKA.Rmd

__Input File(s):__ 
```
- genome_id_prokka.txt
- metadata.tsv (downloaded from the Web of Life database: https://biocore.github.io/wol/)
- counts_prokka.tsv
```

__Overview:__  
Microbial Niche Determination (ND) based on PROKKA annotation of the detected genomes. Niches define each microbe's preferred substrates based on the import proteins they prioritize, according to Translational Efficiency (TE = metaRibo-Seq / metaRNA-Seq) measurements.


### 2.2.ND_Human_fecal_microbiome_Uniref.Rmd

__Input File(s):__ 
```
- counts_species_uniref.tsv
```

__Overview:__  
Microbial Niche Determination (ND) based on Uniref annotation of the detected genomes. Niches define each microbe's preferred substrates based on the import proteins they prioritize, according to Translational Efficiency (TE = metaRibo-Seq / metaRNA-Seq) measurements.


***

### 3.Human_fecal_microcosm_prebiotics.Rmd

__Input File(s):__  
```
- Objects created in previous scripts 1, 2.1, 2.2.
- MI04_BHI_prebiotics_timepoints_WoL_subset_Woltka_Classify_Species_NEW.tsv
```

__Overview:__  
Statistical analysis of experimental prebiotic experiments carried out in a human-associated microcosm. 
To test MIND predictions, we experimentally supplemented the microcosm culture medium with prebiotics identified by MIND.


This script produces manuscript Figure 6.


