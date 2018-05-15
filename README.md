# 16S_genera_potential_function_inventory
 for post high-throughput sequencing analysis
 intially created for QIIME1, QIIME2, and mothur pipelines

DNA was recovered from on-site wastewater treatment systems and sequenced using Illumina Mi-Seq. Sequences were run through either the QIIME1, QIIME2 (including R-dada2), or mothur pipeline and assigned taxonomy by Greengenes 13_8 or SILVA_132. 

Abundant genera were assigned a potential function by conducting a literature review and assuming all members of a genus were potentially capable of the metabolism of the type species (unless otherwise noted specifically). Some cases, potential function could be assigned at family level or higher. 

Nitrogen, carbon, iron, and sulfur cyling are the focus of this inventory. 

# Please reference this repository if using the 16S function inventory 

16S_genera_function_inventory_word.txt is a Mac word document with EndNote bibliography
16S_genera_function_inventory_R.txt is a tab-delimited file of the inventory
     If using the R.txt file, all genera have the prefix "g__" to remove: 
           x$pot_function<-gsub("g__", "", x$pot_function)

last updated: May 14, 2018, 330 genera, 197 references
