.. _IGV:

*******************
4 IGV (Integrative Genomic Viewer)
*******************

IGV is a local Genome Browser software  that allows users to visualize large-scale genomic data. It is very useful for visualizing aligment data such as BAM files or VCF files, and validate genetic variants.


Installation
================

IGV is available for Windows, MacOS, and Linux. You can download the latest version from the official IGV website: `IGV Downloads <https://igv.org/doc/desktop/#DownloadPage/>`_.

Navigation and general concepts
================================

Once installation is completed, to start analysisng your data IGV requires a reference genome. 
By default human genome GRCH38/HG38 is loaded, but you can select another version or speciee genome from the  genome dropdown menu.

If your reference genome is not included, you can load  in FASTA or 2bit format  with the option "Load Genome from File" in the "Genomes" menu.

.. important::
    FASTA files must be indexed with a .fai file using the `Samtools suite <https://www.htslib.org/doc/samtools-index.html>`_.

Check this video for a quick introduction to IGV: `IGV Sequencing Data Basics <https://www.youtube.com/watch?v=E_G8z_2gTYM>`_.


Loading and visualizing data
================================

In this example we will use  a public BAM file  from the ENCODE project  taht contains Bulk RNA-Seq data from colon tissue aligned to the reference Genome GRCh38 (https://www.encodeproject.org/files/ENCFF205TFF/)
For memory efficiency, the file was filtered to only include the reads of the chromosome 12. 

Open IGV and load the reference genome GRCh38 (if not already loaded).

In File > Load from File, select the filtered BAM file for chromosome 12 that you will find in test_data/ENCFF297UZI_chr12.bam 

Remember to download the index file (.bai) for the BAM file and place it in the same directory as the BAM file. Otherwise, IGV will not be able to load the BAM file.

Select the chromosome 12 from the dropdown menu to visualize the data.

In this tutorial we will focus on the KRAS genes, which is located at position chr12:25,189,456-25,251,928
Paste this coordinates in the "Go to" box at the top of the IGV window and press Enter.

From top to down you will see the following tracks:
1. Chromosome ideogram: a graphical representation of the chromosome structure and current position in red rectangle.
2. Length in bp of the showed region and lines inidicating  the different positions in bp. 
3. Coverage graph: a bar graph showing the number of reads that cover each position in the genome.
4. Splice junctions: tracks that shows the breaks in read coverage due to splicing. Blue for + strand and red for - strand. 
5. Alignments: a graphical representation of the reads aligned to the reference genome. 
6. Refseq: a track showing the reference sequence for the region of interest.

As you might have noticed, the coverage graph show a high number of reads coverage the regions that corrrespond to the exons. This is because this experimennt was a Bulk RNA-Seq experiment, which means that it was designed to capture the expressed regions of the genome.
Reads that belong to different transcripts are splitted and a blue line joined in an intronic region. 

Let's zoom in to the region chr12:25,208,119-25,208,240, you will see in the reads boxes come nucleotides highlited in different colors and intensities.
This highlited nucleotides represent the bases that are different from the reference genome, and the intensitie the score of  the base quality (more intense means higher quality).
You can click on a read to see more information about it, such as the mapping quality, strand, and base quality scores.

You can observe also some regions of reads with an I symbol, which indicates that there is an insertion in the read compared to the reference genome.
If more than one nucleotide is inserted, you will see a  "InumberI" symbol indicating the number of inserted nucleotides.

Deletions are are represented as a dash (-) in the read, if more than one nucleotide is deleted, you will see a number sorrounded by dashes. 

.. seealso::
    `IGV RNA-seq data basics tutorial: <https://www.youtube.com/watch?v=awGN-rpLYas>`_