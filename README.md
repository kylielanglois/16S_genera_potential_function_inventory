# 16S_genera_potential_function_inventory
 for post high-throughput sequencing analysis
 intially created for QIIME1, QIIME2, and mothur pipelines

DNA was recovered from on-site wastewater treatment systems and sequenced using Illumina Mi-Seq. Sequences were run through either the QIIME1, QIIME2 (including R-dada2), or mothur pipeline and assigned taxonomy by Greengenes 13_8 or SILVA_132. 

Abundant genera were assigned a potential function by conducting a literature review and assuming all members of a genus were potentially capable of the metabolism of the type species (unless otherwise noted specifically). Some cases, potential function could be assigned at family level or higher. 

FAPROTAX v.1.1 was accessed from http://www.zoology.ubc.ca/louca/FAPROTAX/lib/php/index.php

Nitrogen, carbon, iron, and sulfur cyling are the focus of this inventory. 

# Please reference this repository if using the 16S function inventory 
Langlois, Kylie (2020). 16S_genera_potential_function_inventory. GitHub. https://github.com/kylielanglois/16S_genera_potential_function_inventory

* 16S_genera_function_inventory_word.txt is a Mac word document with EndNote bibliography
word document last updated: February 18, 2019, 759 genera, 212 EndNote citations
* ### This document is most up-to-date document
* 16S_genera_function_inventory.txt is a tab-delimited file of the inventory  
* 042320 is the most current file
## To download: click "Raw" and you will download a comma separated file that can be opened in Excel in the proper format


*033119, 080219, 042320 includes genera in the FAPROTAX inventory*
*FAPROTAX references at FAPROTAX website*
             
 *081018, 010819, 033119,080219, 042320 updates includes genera not in the 072518 update*  
 *includes information on the presence of functional genes found in genera from 3 studies (see below)*  
 *focus is C, N, S, Fe, and H2 cycling*  

* 16S_function_inventory_051418.enlx is a compressed EndNote library of all references up to that date
 references not included in the EndNote library:  
   
&nbsp;&nbsp;&nbsp;   Anantharaman, K., et al. (2016). "Thousands of microbial genomes shed light on interconnected biogeochemical processes in an aquifer    system." Nature communications 7: 13219.  
&nbsp;&nbsp;&nbsp;   Graf, D. R., et al. (2014). "Intergenomic comparisons highlight modularity of the denitrification pathway and underpin the importance of community structure for N2O emissions." PloS one 9(12): e114118.  
&nbsp;&nbsp;&nbsp;   Jones, C. M., et al. (2008). "Phylogenetic analysis of nitrite, nitric oxide, and nitrous oxide respiratory enzymes reveal a complex evolutionary history for denitrification." Molecular Biology and Evolution 25(9): 1955-1966.  

* 16S_function_inventory_010819.enlx is a compressed EndNote library of all reference up to that date including the 3 listed above


## To use with R
```
fun <- read.csv("042320_16S_genera_function_inventory_faprotax_refs.csv", head=T)
dat <- read.csv("YOURTAXONOMYDATA.csv", head=T)
fun$gen <- toupper(fun$gen)
dat$tax <- toupper(dat$tax) #YOUR TAXONOMY COLUMN, AT GENUS LEVEL
m <- merge(dat, fun, by.x = "tax", by.y = "gen", all.x = T, sort = F)
```
