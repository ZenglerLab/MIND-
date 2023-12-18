***

# Microbial Interaction and Niche Determination (MIND) Enable Targeted Alteration of the Microbiome


***

<p align ="center">Oriane Moyne, Mahmoud Al-Bassam, Chloe Lieng, Deepan Thiruppathy, Grant J. Norton, Manish Kumar, Eli Haddad, Yuhan Weng, Livia S. Zaramela, Karsten Zengler</p>

<p align ="center">Departments of Pediatrics and Bioengineering, Center for Microbiome Innovation</p>  <p align ="center">University of California, San Diego, La Jolla, California, USA</p>

***  

## Paper contents

In this study, we present a new approach that integrates transcription and translation measurements to __predict competition and substrate preferences__ within microbial communities, consequently __enabling selective manipulation of the microbiome__.  

By performing metatranscriptomic (metaRNA-Seq) and metatranslatomic (metaRibo-Seq) analysis in complex samples, we characterized microbes into __functional profiles__ and demonstrated that __members of with similar functional profiles are competitors__.  

Then, we predicted __preferred substrates__ based on metaRNA-Seq and metaRibo-Seq signal on importer proteins, which specifically benefited selected microbes in the community (i.e. their __niche__) and simultaneously impaired their competitors. 

***

## Repository Contents

This repository contains data and code used to analyze data and produce figures presented in the associated manuscript.  

The repository is divided in subdirectories, which follow the overall outline of the paper. Namely:  

__1. Microbial Interactions (MI) in a SynCom__  

This section contains scripts and data used to determine __microbial functional profiles__ and __predict competition__ in a 16-member synthetic community (SynCom) based on translational efficiency (TE = metaRibo-Seq / metaRNA-Seq).  
It also contains results of dropout experiments used to validate MI-based predictions of competition interactions.  

__2. Niche Determination (ND) in a SynCom__  

This section contains scripts and data used to perform __Niche Determination (ND)__ and __predict substrate preferences__ in a 16-member synthetic community (SynCom) based on TE.  
It also contains results of prebiotic experiments used to validate niches-based predictions of substrate preferences.  

__3. MIND in a soil microcosm__

This section contains scripts and data used to perform __MIND predictions__ based on TE in a soil microcosm grown in complex medium.  
It also contains results of prebiotic and probiotic experiments used to validate MIND predictions of substrate preferences and competition.  

## Versions  

These analyses were performed under Linux, Ubuntu 18.04.6 LTS using R version 3.6.3 and Rstudio version 1.4.1717. 

## Dependencies

To run these scripts, user needs to install R and Rstudio on their computer. Follow installation instructions here: https://rstudio-education.github.io/hopr/starting.html).  

Users should also install the following packages prior to running these scripts. From a ```R``` session, run:  

```
install.packages(c("stringr", "ggplot2", "FactoMineR", "factoextra", "reshape", "reshape2", "gplots", "scales", "ggpubr", "cowplot", "svglite", "dendextend", "RColorBrewer"))
```

## License

This repository is covered under GNU GENERAL PUBLIC LICENSE version 3.

***




