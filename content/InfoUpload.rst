InfoUpload
============
`Upload unaligned or aligned reads from scRNA-Seq data.`


.. image:: /images/upload_file.png

Users can choose to upload Fastq files or BAM files:

.. contents:: 
    :local:

Input fastq files
------------------------------------------------------

The file needs to be in fastq.gz format, users can select the directory where the data is located through the Browse button;

.. .. image:: /images/upload_file_browse.png

Perform quality control on data
************************************

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

Then, by clicking the NEXT-> Transcript Alignment button, the user can reach the InfoAssembly interface.


Input bam files
------------------------------------------------------
If upload bam files, the program will automatically assemble and merge transcripts.

The file needs to be in bam format, users can select the directory where the data is located through the Browse button;

Upload the example data by checking the Use example data;

Then the user can run the program by clicking BEGIN.

By clicking the NEXT-> NovelScan button, the user can reach the NovelScan interface.

.. note::   If the user uploads bam files, InfoAssembly will be skipped and NovelScan will proceed directly.

