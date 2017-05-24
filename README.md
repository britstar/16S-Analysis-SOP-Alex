# 16S-Analysis-SOP-Alex
The SOP, created by Alex, for 16S Analysis in the Huffnagle Lab

**Renaming the Specimens**

Once the sequencing data has been processed, you should have three files for use in analysis:
1. .shared 
2. .cons.taxonomy
3. .rep.fasta

The shared file is a data frame with a similar format to a spreadsheet, where each row corresponds to each OTU in each sample. The cons.taxonomy file lists each OTU, as well as the taxonomic classification that it was provided during processing in mothur, descending from Phylum to Genus classification, with unknown designation where the classificaiton was not clear. The rep.fasta file provides, for each OTU, a representative sequence of the 16S rRNA gene that was identified during either 454 or MiSeq sequencing. 

The first step, before any analysis is performed, is to rename the specimens using a standardized, easy to visualize format. This is up to personal preference and depends on the experiment, but the format that I used for the Mouse H1N1 experiment was AAAAA_BB_CC_DDDD, where the A's correspond to specimen type (e.g. CECUM, LUNG), the B's correspond to mouse number or control type (e.g. 01, 23, AE, WR), C's represent cage number, or is filled with XX for controls, and the D's show exposure type (e.g.H1N1, SALN, XXXX for controls). An example of a full name would be TNGUE_06_02_H1N1, which is for the tongue sample of mouse 6, who was housed in cage 2 and treated with H1N1 virus. 

The easiest way to do this is to open the .shared file in Excel and copy the second column, corresponding to the default sample names, into a new spreadsheet. Then, in the following columns fill in the information that will be used in your naming scheme, wiht each part that is separated by an underscore in its own column. Then combine the columns by separating them with the &symbol and an underscore in quotes " ", forming a final column that matches column one except each sample is now named using your guidelines. Paste this final column into the row name column of your .shared file, and you now have a file that will show your naming scheme when prompted for row names in R. For an example of the spreadsheet, see the screenshot below: 

