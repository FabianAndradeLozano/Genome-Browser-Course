.. _Introduction to genome browsers:

*******************
1 Introduction to Genome Browsers
*******************

Types of Genome Browsers
================================

As sequencing technologies improve and the number of sequenced genomes increases, a need for exploring, comparing, and examining this data emerges. 
A solution to this need led to the development of genome browsers. A genome browser is a program that stores the sequence and annotations of a species, 
allowing researchers from various fields to access, search, retrieve, and analyze this data in a graphical way. 

A genome browser is an interactive tool that enables researchers to visualize and navigate genomic sequences and their annotations. 
It provides a graphical interface to explore genes, regulatory elements, variations, and comparative genomics data within a genome. 

Genome browsers are structured around two main components: sequence and tracks. The sequence displays the actual DNA bases within specific regions, 
defined by chromosome number (if applicable) and start/end positions. Tracks, on the other hand, represent various types of annotations, such as transcript evidence, expression profiles, 
and regulatory data, sourced from different databases. By overlaying multiple tracks from the same genomic region, researchers can interpret the genomic landscape, assign functions to specific areas, 
and conduct comparative analyses across species.

Genome browsers are divided into web-based browsers and standalone applications. In this course, we will focus on the first type.

Web-based
-----------
Accesible online, regularly updated:

	**UCSC Genome Browser**

	**Ensembl**

	**NCBI Genome Data Viewer**

Also, Several genome browsers have been designed for specific organisms, providing specialized resources. Most of these correspond to model experimental species. 
Some examples are:

	- `**FlyBase**: For *Drosophila melanogaster* (fruit fly). <https://flybase.org/>`_
	- `**WormBase**: For *Caenorhabditis elegans* (nematode worm). <https://wormbase.org/#012-34-5>`_
	- `**TAIR**: For *Arabidopsis thaliana* (thale cress). <https://www.arabidopsis.org/>`_ 
	- `**MaizeGDB**: For *Zea mays* (maize). <https://www.maizegdb.org/>`_
	- `**Gramene**: Focused on plant genomes like rice, wheat, and barley. <https://www.gramene.org/>`_
	- `**Saccharomyces Genome Database (SGD)**: For *Saccharomyces cerevisiae* (baker's yeast). <https://www.yeastgenome.org/>`_
	- `**Rat Genome Database (RGD)**: For *Rattus norvegicus* (rat). <https://rgd.mcw.edu/>`_ 
	- `**ZFIN**: For *Danio rerio* (zebrafish). <https://zfin.org/>`_
	- `**Mouse Genome Informatics (MGI) Browser**: For *Mus musculus* (mouse). <https://www.informatics.jax.org/>`_
	- `**Echinobase**: For echinoderms like sea urchins. <https://echinobase.org/echinobase/>`_
	- `**Cattle Genome Database**: For *Bos taurus* (cattle). <https://bovinegenome.elsiklab.missouri.edu/>`_

Software-based
--------------
Applications installed on local machines, recommended when working with large datasets or new genome assemblies. 

	`**Integrative Genomic Viewer (IGV)** <https://igv.org/doc/desktop/>`_

	`**Artemis** <https://sanger-pathogens.github.io/Artemis/Artemis/>`_ 


Genome assembly codification
=============================

We can find different genomes assemblies codification names for the same specie and version depeding on their sourcer (UCSC, ENSEMBL or NCBI). 

.. note::
	For chromosome naming:

	- UCSC uses "chr" prefix (e.g., chr1, chr2, chrX)
	- ENSEMBL/NCBI uses numbers or letters without prefix (e.g., 1, 2, X)
	
	When working with this genomes is important to be consistent when choosing the reference genome, annotation, aligning , etc.
	This difference in chromosome naming can affect how genomic coordinates are interpreted and may require conversion when switching between resources or tools that use different conventions.	

ENSEMBL Codification
------------------

Ensembl uses a naming convention that includes the species and the version of the genome. The current genome assembly is referred to as GRCh38.p14, while the previous genome is referred to as GRCh37. For the first name the codification is:

- GRC stands for `Genome Reference Consortium <https://www.ncbi.nlm.nih.gov/grc>`_
- h stands for human
- 38 indicates the 38th version
- p.14 denotes the 14th patch (small updates that do not affect the assembly coordinates but correct specific regions or add annotations). This feature provides a more detailed versioning system.

UCSC Codification
------------------

UCSC uses a simplified naming system. For the current human genome assembly, it refers to it as hg38 (Homo sapiens genome build 38), and for the previous version as hg19.

This naming difference stems from the fact that Ensembl tends to mirror official genome releases like those from the GRC,
while UCSC focuses on providing stable assembly versions. Patches or updates in UCSC are referred to as separate tracks.
This means that users working with hg38 may not be automatically aware of any minor updates unless they manually explore the tracks.