InfoUpload
============
`upload unaligned or aligned reads from scRNA-Seq data`


.. image:: /images/upload_file.png
Users can choose to upload Fastq files or BAM files:

.. contents:: 
    :local:

Input fastq files
------------------------------------------------------

The file needs to be in fastq.gz format, users can select the directory where the data is located through the Browse button;
.. .. image:: /images/upload_file_browse.png

Perform quality control on data
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

After uploading the data, the data will be automatically controlled for quality; if the Adapter sequence is provided, the user can enter the adapter sequence in reads1, reads2; if the adapter sequence not provided, the adapter will be automatically detected for quality control.

Basic Parameters
******************


-  ``-q (--qualified_quality_phred)`` - The quality value that a base is qualified. Default 15 means phred quality >=Q15 is qualified. (int [=15]).
-  ``--thread`` - The worker thread number.

Then the user can run the program by clicking START.
.. .. image:: /images/upload_file_START.png

After the program runs, the user can view the results of the quality control by clicking the Result button.
.. image:: /images/upload_file_Result.png

Quality control results
*************************


.. image:: /images/upload_file_Result_enter.png

The user presses the Enter Key to display the results of the quality control and double-click the file to view the quality of the reads in the upload files.
.. .. image:: /images/upload_file_Result_files.png

InfoAssembly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
`merge reads from multiple cells to perform reads alignment and transcripts assembly`

By clicking the NEXT-> Transcript Alignment button, the user can reach the InfoAssembly interface.

.. image:: /images/upload_file_InfoAssembly.png

The functions of this interface mainly include: comparing data to a reference genome, assembling transcripts, and merging transcripts.

Genome
*************************
Select species (Human or Mouse).

Number of Thread
*************************
The worker thread number.

params
*************************
-  ``--fast`` hisat2 params, --no-repeat-index.
-  ``--sensitive`` hisat2 params, --bowtie2-dp 1 -k 30 --score-min L,0,-0.5.
-  ``--very-sensitive`` hisat2 params, --bowtie2-dp 1 -k 30 --score-min L,0,-0.5.
.. note::   
            * -k: A read may have multiple valid alignments, and not all alignments will be output when output, but only the N alignments specified by the -k parameter. The default value of -k is 5;
            * --score-min: Sets a function governing the minimum alignment score needed for an alignment to be considered “valid” (i.e. good enough to report). This is a function of read length. For instance, specifying L,0,-0.6 sets the minimum-score function f to f(x) = 0 + -0.6 * x, where x is the read length. See also: [setting function options]. The default is L,0,-0.2
            * --bowtie2-dp 1 :use Bowtie2's dynamic programming alignment algorithm (0) - 0: no dynamic programming, 1: conditional dynamic programming, and 2: unconditional dynamic programming (slowest) 

-  ``--min-intronlen`` <int> minimum intron length (default 20).
-  ``--max-intronlen`` <int> maximum intron length (default 500000).
-  ``avoid-pseudogene`` tries to avoid aligning reads to pseudogenes (experimental option).
-  ``--qc-filter`` filter out reads that are bad according to QSEQ filter.
Then the user can run the program by clicking START button.
After the program runs, the user can view the results of the quality control by clicking the Result button.

Assembly results
*************************
.. image:: /images/InfoAssembly_Result_enter.png

The user presses the Enter Key to display the results of the quality control and double-click the file to view.

.. image:: /images/InfoAssembly_Result_files.png

By clicking the NEXT button, the user can reach the NovelScan interface.

Input bam files
------------------------------------------------------
If upload bam files, the program will automatically assemble and merge transcripts.

The file needs to be in bam format, users can select the directory where the data is located through the Browse button;

Upload the example data by checking the Use example data;

Then the user can run the program by clicking BEGIN.

By clicking the NEXT-> NovelScan button, the user can reach the NovelScan interface.

