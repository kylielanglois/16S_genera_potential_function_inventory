# 16S_genera_potential_function_inventory
 For post high-throughput sequencing analysis
 intially created for QIIME1, QIIME2, and mothur pipelines

Genera were assigned a potential function by conducting a literature review and assuming all members of a genus were potentially capable of the metabolism of the type species (unless otherwise noted specifically). Some cases, potential function could be assigned at family level or higher. 

Nitrogen, carbon, iron, and sulfur cyling are the focus of this inventory. 

# Please reference this repository if using the 16S function inventory 
Langlois, Kylie (2021). 16S_genera_potential_function_inventory. GitHub. https://github.com/kylielanglois/16S_genera_potential_function_inventory

* 16S_genera_function_inventory.csv is a comma-delimited file of the inventory  
* 2021_0118 is the most current file with 1,855 genera
* 2021_genus_inventory_references.doc is a Word file (Mac format) with references for 2021_0118 inventory
## To download: click "Raw" and you will download a comma separated file that can be opened in Excel in the proper format

*(Louca et al. 2016) references at FAPROTAX website*

FAPROTAX v.1.1 was accessed from http://www.loucalab.com/archive/FAPROTAX/lib/php/index.php?section=Download

*includes information on the presence of functional genes found in genera from 3 studies (see below)*  
   
&nbsp;&nbsp;&nbsp;   Anantharaman, K., et al. (2016). "Thousands of microbial genomes shed light on interconnected biogeochemical processes in an aquifer    system." Nature communications 7: 13219.  
&nbsp;&nbsp;&nbsp;   Graf, D. R., et al. (2014). "Intergenomic comparisons highlight modularity of the denitrification pathway and underpin the importance of community structure for N2O emissions." PloS one 9(12): e114118.  
&nbsp;&nbsp;&nbsp;   Jones, C. M., et al. (2008). "Phylogenetic analysis of nitrite, nitric oxide, and nitrous oxide respiratory enzymes reveal a complex evolutionary history for denitrification." Molecular Biology and Evolution 25(9): 1955-1966.  


## To use with R
```
fun <- read.csv("2020_0703_16S_genera_function_inventory_faprotax_refs.csv", head=T)
dat <- read.csv("YOURTAXONOMYDATA.csv", head=T)
fun$gen <- toupper(fun$gen)
dat$tax <- toupper(dat$tax) #YOUR TAXONOMY COLUMN, AT GENUS LEVEL
m <- merge(dat, fun, by.x = "tax", by.y = "gen", all.x = T, sort = F)
```
