RNA-Export
==========

Extract from our Oracle database the RNA data

## Description
RNA data will be extracted from the Oracle database and dump into a flat file that will be further:

* Submitted to [RNA central](http://rnacentral.org/)
* Import into the new dicty Postgresql database

Estimated finishing date 3/20/2014


## Feedback from EBI
RNAcentral is based on ncRNAs entries in ENA. Dicty sequences might have been already submitted to INSDC databases.

Searching in the non-coding ENA domain "Dictyostelium discoideum", it retrieves 3971 results. I digged in and this is what I found:

From these, 

* 486 from "Dictyostelium discoideum AX4 r28" (these are probably our annotations)
* 3,485 from "Dictyostelium discoideum" (we don't know where these come from exactly)

The dictybase BLAST tool offers different optional databases to search against. 
One of them is "D. discoideum Non-coding sequences DNA", which should contains all the non-coding RNA. This database contains 1159 sequences.

Through SQL queries, we know that:

* 508 are non coding RNA
* 651 are pseudogenes 

This means that 508-486 = 22 entries have been lost in dumping data to EBI







