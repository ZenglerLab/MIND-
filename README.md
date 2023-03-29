***

# Microbial guilds and Niche Determination (MiND)

This repository contains scripts associated to the following manuscript:  

***

<h4> <p align ="center">Guild and Niche Determination Enables Targeted Alteration of the Microbiome</p> </h4>

<p align ="center">Oriane Moyne, Mahmoud Al-Bassam, Chloe Lieng, Deepan Thiruppathy, Grant J. Norton, Manish Kumar, Eli Haddad, Livia S. Zaramela, Karsten Zengler</p>

<p align ="center">Departments of Pediatrics and Bioengineering, Center for Microbiome Innovation</p>  <p align ="center">University of California, San Diego, La Jolla, California, USA</p>

***  

## Paper contents

In this study, we present a new approach that integrates transcription and translation measurements to predict competition and substrate preferences within microbial communities, consequently enabling the selective manipulation of the microbiome. By performing metatranscriptomic (metaRNA-Seq) and metatranslatomic (metaRibo-Seq) analysis in complex samples, we classified microbes into functional groups (i.e. guilds) and demonstrated that members of the same guild are competitors. Furthermore, we predicted preferred substrates based on importer proteins, which specifically benefited selected microbes in the community (i.e. their niche) and simultaneously impaired their competitors. 

***

## Repository Contents

This repository contains data and code used to analyze data and produce figures presented in the associated manuscript.  

The repository is divided in subdirectories, which follow the overall outline of the paper. Namely:  

__1. Guild-based Microbiome Classification and Prediction of Competition in a SynCom__  

This section contains scripts and data used to determine __microbial guilds__ and __predict competition__ in a 16-member synthetic community (SynCom) based on translational efficiency (TE = metaRibo-Seq / metaRNA-Seq).  
It also contains results of experimental dropout experiments used to validate guild-based predictions of competition interactions.  

__2. Microbial Niche Determination and Prediction of Substrate Preferences in a SynCom__  

This section contains scripts and data used to perform __Microbial Niche Determination (MiND)__ and __predict substrate preferences__ in a 16-member synthetic community (SynCom) based on TE.  
It also contains results of experimental results of experimental prebiotic experiments used to validate niches-based predictions of substrate preferences.  

## Versions  

These analyses were performed under Linux, Ubuntu 18.04.6 LTS using R version 3.6.3 and Rstudio version 1.4.1717. 

## Dependencies

To run these scripts, user needs to install R and Rstudio on their computer. Follow installation instructions here: https://rstudio-education.github.io/hopr/starting.html).  

Users should also install the following packages prior to running these scripts. From a ```R``` session, run:  

```
install.packages(c("stringr", "ggplot2", "FactoMineR", "factoextra", "reshape", "reshape2", "gplots", "scales", "ggpubr", "cowplot", "svglite"))
```

## License

This repository is covered under GNU GENERAL PUBLIC LICENSE version 3.

***

# Citations  

If you use the code or methods presented in this repository or associated manuscript, please cite:  

Moyne et _al_, 2023. Guild and Niche Determination Enables Targeted Alteration of the Microbiome. _Submitted to Nature_.  



