FWMFG
=====

Freshwater microbial field guide

README 

This is the README file for distribution of the freshwater 16S rRNA gene sequence database curated by the McMahon-Bertilsson research groups.  The ARB databases are useful for those who want to insert new sequences into high-quality trees with established FW taxonomy, or to extract a region of the alignment to classify amplicon tag sequences. The trainingset files are useful for classifying amplicons or metagenomic reads that contain 16S genes.  They have been vetted in both mothur and QIIME.

The following files have been posted to this Gihub repository:

(updates added so that the most recent one is at the top)
__

(updated February 2016)

See here for new and better workflow:
https://github.com/McMahonLab/16STaxAss

FWonly_11Feb2016_1452_ready.fasta
Only FW sequences. Contains 1452 sequences. Added and curated ~300 sequences from Ryan Newton.

FWonly_11Feb2016_1452.taxonomy
Only FW sequences. Contains 1452 sequence IDs. Some typos and inconsistencies have been fixed.

--
(updated 19 July 2012)

FW_trainingset_MMBR_strict_12July12.fasta
Only FW sequences, derived from 28Dec11 version. Contains 1148 sequences. Added a few new reference sequences. Fixed a few errors that made it difficult to blend FW with GG.  

FW_trainingset_MMBR_strict_12July12.taxonomy
Taxonomy file that goes with FW_trainingset_MMBR_strict_12July12.fasta. Note that I had to modify slightly to make it compatible with QIIME (removing extra spaces).


--
(updated 20 January 2012)

SSU_rRNA_FWonly_27Dec11_todistribute.arb - 11587 sequences
Only FW sequences. The corresponding trainingst below was created with the ARB configuration called FW_only_25Dec2011. This excludes the "Minor Phyla", Cyanobacteria, and "AllOtherPhyla" trees because they are not FW-specific enough to justify having them in this special trainingset. Also remove "Soil_I" and "Common Isolates" within the actinos.  Total: 1117 sequences.

FW_trainingset_MMBR_strict_28Dec11.fasta
Only FW sequences, derived from the 9Sept11 version but with only 1117 sequences (see description of the FW_only_25Dec2011 configuration, above). Taxonomies curated to include markups like k__, p__, c__ to match greengenes. This was done to allow merging at coarser levels of resolution.

FW_trainingset_MMBR_strict_28Dec11.taxonomy
Taxonomy file that goes with FW_trainingset_MMBR_strict_28Dec11.fasta. Note that I had to modify slightly to make it compatible with QIIME (removing extra spaces).

I am not uploading a concatenated FW-GG trainingset right now because my group has started doing the assignments serially.  That is, we use the FW-only trainingset first, and then anything that does not get assigned with sufficient confidence gets run through the GG trainingset.  We are doing this in QIIME currently, so I am not sure how to do it in mothur. It would probably require some perl scripting.  I will work on this in the next few months. In the meantime, let me know if you want a merged FW-GG trainingset and I can easily upload one.

To make things even more complicated, greengenes just released a new trainingset.  Byron Crump says there are some bugs (sequences not in the taxonomy and taxonomies not represented in the sequences), so we haven't used it yet. I also prefer to work with the 97%-otu version, which doesn't seem to be availble yet for the new release. I recommend that you watch the GG website closely for updates.  I'll try to also!

--
(updated 28 September 2011)

SSU_rRNA_FWonly_9Sept11_todistribute.arb - 11587 sequences
Only FW sequences. Created by marking the "All FW in trees" configuration in SSU_rRNA_FW_3Aug11_todistribute.arb, and deleting all other sequences. The "FW4mothur2" configuration is used to export sequences and taxonomies for the trainingset.  Updated the "FW4mothur2" configuration to remove one short sequence that had slipped through. Now it selects 1204 sequences.

FW_trainingset_MMBR_strict_9Sept11.fasta - 1204 sequences
Only FW sequences. Created by marking the "FW4mothur2" configuration in SSU_rRNA_FWonly 9Sept11_todistribute.arb. Taxonomies curated to strictly match MMBR hierarchies. Not aligned.

FW_trainingset_MMBR_strict_9Sept11.taxonomy
Taxonomy file that goes with FW_trainingset_MMBR_strict_9Sept11.fasta

FWGG_trainingset_MMBR_strict_9Sept11.fasta - 36583 sequences
Combined set of FW sequences (FW_trainingset_MMBR_strict_9Sept11.fasta) plus the 97%-OTU Greengenes database (gg_97_otus_4feb2011.fasta) as suggested in Werner et al (2011) ISMEJ, with overlapping sequences deleted. Taxonomies for the FW sequences were curated to strictly match MMBR hierarchies. 

FWGG_trainingset_MMBR_strict_9Sept11.taxonomy
Taxonomy file that goes with FWGG_trainingset_MMBR_strict_9Sept11.fasta

--
(updated 3 Aug 2011)

SSU_rRNA_FW_3Aug11_todistribute.arb  -  28546 sequences
Based on RDP Release 8.0 SSU Prokaryotic data, with FW sequences added

SSU_rRNA_FWonly_3Aug11_todistribute.arb - 11587 sequences
Only FW sequences. Created by marking the "All FW in trees" configuration in SSU_rRNA_FW_3Aug11_todistribute.arb, and deleting all other sequences. The "FW4mothur2" configuration is used to export sequences and taxonomies for the trainingset.

FW_trainingset_MMBR_strict_3Aug11.fasta - 1205 sequences
Only FW sequences. Created by marking the "FW4mothur2" configuration in SSU_rRNA_FW_July11_todistribute.arb. Taxonomies curated to strictly match MMBR hierarchies. Not aligned.

FW_trainingset_MMBR_strict_3Aug11.taxonomy
Taxonomy file that goes with FW_trainingset_MMBR_strict_3Aug11.fasta

FWGG_trainingset_MMBR_strict_3Aug11.fasta - 36634 sequences
Combined set of FW sequences (FW_trainingset_MMBR_strict_3Aug11.fasta) plus the 97%-OTU Greengenes database (gg_97_otus_4feb2011.fasta) as suggested in Werner et al (2011) ISMEJ. Taxonomies for the FW sequences were curated to strictly match MMBR hierarchies. 

FWGG_trainingset_MMBR_strict_3Aug11.taxonomy
Taxonomy file that goes with FWGG_trainingset_MMBR_strict_3Aug11.fasta 

--
Original posting:

SSU_rRNA_FW_July11_todistribute.arb  -  28546 sequences
Based on RDP Release 8.0 SSU Prokaryotic data, with FW sequences added

SSU_rRNA_FWonly_July11_todistribute.arb - 11587 sequences
Only FW sequences. Created by marking the "All FW in trees" configuration in SSU_rRNA_FW_July11_todistribute.arb, and deleting all other sequences. The "FW4mothur2" configuration is used to export sequences and taxonomies for the trainingset.

FW_trainingset_July11.fasta - 1205 sequences
Only FW sequences. Created by marking the "FW4mothur2" configuration in SSU_rRNA_FW_July11_todistribute.arb. Not aligned.

FW_trainingset_July11.taxonomy
Taxonomy file that goes with FW_trainingset_July11.fasta

FWGG_trainingset_July11.fasta - 36634 sequences
Combined set of FW sequences (FW_trainingset_July11.fasta) plus the 97%-OTU Greengenes database (gg_97_otus_4feb2011.fasta) as suggested in Werner et al (2011) ISMEJ.

FWGG_trainingset_July11.taxonomy
Taxonomy file that goes with FWGG_trainingset_July11.fasta




If you find any inconsistencies or mistakes, please email Trina (contact info below).

Credits:
The vast majority of work in preparing this database was done by Dr. Ryan Newton, while a PhD student in the McMahon laboratory at UW-Madison. Drs. Stefan Bertilsson and Alex Eiler contributed a large number of previously unpublished sequences to the database.

###########################################################################

If you use this database and/or the training sets for 16S rRNA sequence classifications, please cite this paper:

R. J. Newton, S. E. Jones, A. Eiler, K. D. McMahon, S. Bertilsson. (2011) "A Guide to the natural history of freshwater lake bacteria". Microbiology and Molecular Biology Reviews 75(1):14-49. 

###########################################################################

Updated by Katherine (Trina) McMahon - 14 September 2014
University of Wisconsin - Madison
Departments of Civil and Environmental Engineering and Bacteriology
tmcmahon@engr.wisc.edu
