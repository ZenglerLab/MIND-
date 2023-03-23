<h4> <p align ="center"> Guild-Based Microbiome Classification and Predictions of Competition in a SynCom </p> </h4>

***

### 1.multiomics_customindex_dataprep.Rmd
##### Needed File(s): Final_18_strains_with_strainN.saf, 18_strains_genenames.txt, 18_genomes_KEGG_BlastKOALA.csv, FINAL_SynCom_modifs_multiomics_count_table_formatted.tsv, Final_18_strains_with_strainN.saf

Data cleaning and normalization. Genomes were annotated with the KEGG database using BlastKOALA annotation service (Kanehisa et al. 2016).


***

### 2.SynCom_Guild_classification_Competition_prediction.Rmd
##### Needed File(s): Output from script 1

Translational Efficiency was calculated and Guild-Based Microbiome Classification was performed based on TE. Figures 1b, 1c, 2c, 2d were generated. Supplementary Table S1 and Supplementary Figures S2 and S4 were also generated.


***

### 3.Dropout_SynCom_Expt1_metaG_taxonomic_abundances.Rmd
##### Needed File(s): Output from script 1

Predicting community microbe interactions in soil (competitions and dropouts). Figure 2b and part of Figure 2e and Supplementary Figures S1a and S6 were generated.


***

### 4.metaG_customindex_abundances_second_dropout_experiment_dataprep.Rmd
##### Needed File(s): Dropout_expt2_Syncom_metaG_count_table.tsv, Final_18_strains_with_strainN.saf

Data cleaning and normalization of experimental results of community microbe interactions in soil (competitions and dropouts).


***

### 5.metaG_customindex_abundances_second_dropout_experiment.Rmd
##### Needed File(s): Output from script 4

Experimental community microbal competition and dropout results were analyzed. Figure 2e and Supplementary Figures S7h and S7d were generated.
