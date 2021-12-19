Installation
=============

Remember -- InfoScan are available for **Linux os** as well as for
**Mac os**!

.. contents:: 
    :local:

Download InfoScan
--------------------
*InfoScan is free and open to all users.*

If you're here for the first time, download InfoScan first, and unzip it into a directory whatever you like.

`Download gRINN v.1.1.0 for Linux x64 <https://www.dropbox.com/s/rijb1em1q83b0kf/grinn_linux_v110.tar.gz?dl=1>`_

`Download gRINN v.1.1.0 for Mac OSX <https://www.dropbox.com/s/flywnhup8iedrwh/grinn_macosx_v110.zip?dl=1>`_

Windows support is currently a work-in-progress. Stay tuned and visit back for a Windows compatible executable.

.. note:: For users who want to remote operation a linux system in windows, the SSH client must be capable of X11-Forwarding, such as `MobaXterm <https://mobaxterm.mobatek.net/>`_ et al.

Download Genome annotation file
---------------------------------
Users should download the genome annotation file for the species of interest, and unzip these files into the directory of InfoScan.

`Download test <https://rna.sysu.edu.cn/dreambase2/InfoScanfiles/dotplot.zip>`_

`Download xxx <https://www.dropbox.com/s/flywnhup8iedrwh/grinn_macosx_v110.zip?dl=1>`_


Starting the software
---------------------------------
Once the InfoScan mian program and the Genome annotation are downloaded and unzipped properly, go to the directory of InfoScan:

.. code:: bash

    $ cd /the/directory/of/unzipped_InfoScan

The operation of InfoScan needs to grant executable permission to the script of the software. Please execute the following code before running the software:

.. code:: bash

 $ chmod 777 ./snakemake/script/*
 $ chmod 777 ./InfoScan

Then, upon executed the ./InfoScan, the following window appears:

.. code:: bash

	$ ./InfoScan

.. image:: /images/introduction.png

Configuration
---------------------------
Before uploading data, you should first configure the operating environment of the software, this step can be achieved through the *Configuration* button at the bottom of the main window.

.. image:: /images/Configuration.png

.. note:: This step will automatically install some software through `conda <https://docs.conda.io/en/latest/>`_\ . 

.. tip:: For support or questions please make a post on `Biostars <http://biostars.org>`__. For feature requests or bug reports please open an issue `on github <http://github.com/deeptools/deeptools>`__.
