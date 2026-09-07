# variants overlapping TAD boundaries

This document describes how to prioritize variants overlapping TAD boundaries.

## TAD boundaries

We propose the Q4 and Q3 sets, which contain TAD boundaries with high evidence in most tissues:
[TAD_boundaries_UCSC_Q4](./TAD_boundaries_UCSC_Q4.bed) and [TAD_boundaries_UCSC_Q3.bed](./TAD_boundaries_UCSC_Q3.bed)

TAD boundary definitions were downloaded from [UCSC](https://genome.ucsc.edu/cgi-bin/hgTables?hgsid=4107600425_H50Aqhlw86BUtfPnHnZgxMnbmZkJ&db=hg38&hgta_group=user&hgta_track=ct_Q3TADBoundary_1540&hgta_table=0&hgta_regionType=genome&position=chr7%3A155%2C799%2C529-155%2C812%2C871&hgta_outputType=primaryTable&hgta_outFileName=).  

## CTCF sites

TAD boundaries from UCSC are 100 kilobases large and would therefor produce too many CNV hits.  
Thus, we only look at CNVs that overlap both a TAD boundary *and* a constitutive CTCF sites (constitutive in this context means in more than 80% of cell types).  
This folder contains a [BED file of constitutive CTCF sites](./human_constitutive.bed).  
It was downloaded from [https://www.ctcf.info](https://www.ctcf.info/static/data/human/human_constitutive.bed).


## Filtering of CNVs

This is our general recommendation how to filter CNVs for putative regulartory effect due to disruption of a TAD boundary:

- CNV should be rare, i.e. below 0.1% AF in general population.
- CNV call should have high quality - here we cannot give general advice since the quality depends on the CNV caller.
- CNV should overlap a TAD boundary
- CNV should overlap a constitutive CTCF site
- OMIM gene which is known to cause the patient's disease should be contained in the TADs next to the TAD boundary

Optional additional filters:

- CNV is deletion - this easier to interprete than duplications
- OMIM disease inheritance is dominant (or recessive and copy number is 0)

