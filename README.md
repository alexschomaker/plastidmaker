plastidmaker
============

Plastidmaker is a pipeline wrapper, result analyzer and automated annotator, written in Python v2.7, that, with the help of other programs, builds, analyzes, looks for the best build and annotates plastid genomes (such as mitochondria and cloroplast). It could be used with other targets, such as specific genes, or transcriptomes, even though that is not it's primary goal, nor thoroughly tested.
 
After various attempts to build different mitochondrial genomes in the lab I studied, a general pipeline started to appear: assemble reads with MIRA or SOAPdenovo-Trans, look for a scaffold/contig that matches a closely-related species, check it to see if all expected genomic features are present (since mitochondria is well conserved), check to see if the assembly might have circularized (since it's a circular DNA). If a feature was missing, or it hasn't circularized, try and assemble again with different assembler parameters (mainly k-mer). Rinse and repeat until the best build is found and then annotate it.

Doing these steps automatically, in order to increase efficiency, is basically what plastidmaker was made for.
