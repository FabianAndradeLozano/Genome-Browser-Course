.. _IGV:

*******************
1 IGV (Integrative Genomic Viewer)
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