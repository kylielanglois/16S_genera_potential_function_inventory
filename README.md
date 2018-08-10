# 16S_genera_potential_function_inventory
 for post high-throughput sequencing analysis
 intially created for QIIME1, QIIME2, and mothur pipelines

DNA was recovered from on-site wastewater treatment systems and sequenced using Illumina Mi-Seq. Sequences were run through either the QIIME1, QIIME2 (including R-dada2), or mothur pipeline and assigned taxonomy by Greengenes 13_8 or SILVA_132. 

Abundant genera were assigned a potential function by conducting a literature review and assuming all members of a genus were potentially capable of the metabolism of the type species (unless otherwise noted specifically). Some cases, potential function could be assigned at family level or higher. 

Nitrogen, carbon, iron, and sulfur cyling are the focus of this inventory. 

# Please reference this repository if using the 16S function inventory 

* 16S_genera_function_inventory_word.txt is a Mac word document with EndNote bibliography
word document last updated: July 25, 2018, 349 genera, 202 references

* 16S_genera_function_inventory_R.txt is a tab-delimited file of the inventory  
  
 &nbsp;&nbsp;&nbsp;    If using the R.txt file, all genera have the prefix "g__" to remove: 
           x$pot_function<-gsub("g__", "", x$pot_function) 
             
 *081018 update includes genera not in the 072518 update*  
 *includes information on the presence of functional genes found in genera from 3 studies (see below)*  
 *focus is C, N, S, Fe, and H2 cycling*  

* 16S_function_inventory_051418.enlx is a compressed EndNote library of all references 
 references not included in the EndNote library:  
   
&nbsp;&nbsp;&nbsp;   Anantharaman, K., et al. (2016). "Thousands of microbial genomes shed light on interconnected biogeochemical processes in an aquifer    system." Nature communications 7: 13219.  
&nbsp;&nbsp;&nbsp;   Graf, D. R., et al. (2014). "Intergenomic comparisons highlight modularity of the denitrification pathway and underpin the importance of community structure for N2O emissions." PloS one 9(12): e114118.  
&nbsp;&nbsp;&nbsp;   Jones, C. M., et al. (2008). "Phylogenetic analysis of nitrite, nitric oxide, and nitrous oxide respiratory enzymes reveal a complex evolutionary history for denitrification." Molecular Biology and Evolution 25(9): 1955-1966.  


