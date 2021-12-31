Installation
=============

``Remember`` -- InfoScan are available for **Linux os** as well as for
**Mac os**!

.. contents:: 
    :local:

Download InfoScan
--------------------
*InfoScan is free and open to all users.*

If you're here for the first time, download InfoScan first, and decompress it into a directory whatever you like.

`Download InfoScan v.0.1 for Linux x64 <https://rna.sysu.edu.cn/InfoScan/InfoScan.zip>`_

`Download InfoScan v.0.1 for Mac OSX <https://rna.sysu.edu.cn/InfoScan/InfoScan_mac.zip>`_

Windows support is currently a work-in-progress. Stay tuned and visit back for a Windows compatible executable.

.. note:: For users who want to remote operation a linux system in windows, the SSH client must be capable of X11-Forwarding, such as `MobaXterm <https://mobaxterm.mobatek.net/>`_ et al.

Download Genome annotation file
---------------------------------

Users should download the genome annotation file for the species of interest, and decompress these files into the same directory of InfoScan.

.. There are two types of genome annotation file, one is the indexes with spike-in pre-built by us. The other is HISAT2 official indexes.

* **pre-built indexes**

`Download hg38 <https://mega.nz/file/E4lH3IRD#EcmYwJPJEi9T706fyUgejvA2AFBaejdjCA9ACP8uKiE>`_

`Download mm10 <https://mega.nz/file/Ess2gYAZ#PyfipRKvbL17OA6w6kh60rPDP-bNm3hyqbszxiS4et8>`_

.. **HISAT2 indexes**


.. `Download H. sapiens GRCh38 genome_snp <https://genome-idx.s3.amazonaws.com/hisat/grch38_snp.tar.gz>`_

.. `Download M. musculus GRCm38 genome_snp <https://cloud.biohpc.swmed.edu/index.php/s/grcm38_snp/download>`_

.. .. note:: This step will automatically install some software through `conda <https://docs.conda.io/en/latest/>`_\ . 

Download example data
-----------------------

InfoScan provide some example data (mouse) for the user to test. If want to do so, you should download the example data, and decompress these files into the same directory of InfoScan.

`Download example data <https://mega.nz/file/Axk3wa6S#eEXffvKWwFO3Zz07PaGr3elSSFdRF92swOeIJwUn05c>`_


Install conda
---------------------------------
InfoScan needs to use conda to configure the environment, please install conda first:

* *Linux*

.. code:: bash

    wget -c https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    chmod 777 Miniconda3-latest-Linux-x86_64.sh
    bash Miniconda3-latest-Linux-x86_64.sh
    source ~/.bashrc

* *Mac OS*

.. code:: bash

    curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
    chmod 777 Miniconda3-latest-MacOSX-x86_64.sh
    sh Miniconda3-latest-MacOSX-x86_64.sh
    source ~/.bash_profile


Starting the software
---------------------------------

* *Linux*

Once the InfoScan mian program and the Genome annotation are downloaded and unzipped properly, go to the directory of InfoScan:

.. code:: bash

    $ cd /the/directory/of/unzipped_InfoScan
    
    # see all files, don't run.
    $ tree -L 1
    .
    ├── AppRun -> InfoScan
    ├── CPAT-3.0.0
    ├── default.desktop
    ├── images
    ├── InfoScan
    ├── InfoScan.sh
    ├── lib
    ├── libexec
    ├── libstdc++.so.6
    ├── pack.sh
    ├── plugins
    ├── qss
    ├── qt.conf
    ├── resources
    ├── snakemake
    └── translations

    9 directories, 7 files


The operation of InfoScan needs to grant executable permission to the script of the software. Please execute the following code before running the software:

.. code:: bash

 $ chmod 777 ./snakemake/script/*
 $ chmod 777 ./InfoScan

Then, upon executed the ./InfoScan, the following window appears:

.. code:: bash

	$ ./InfoScan

.. image:: /images/introduction.png

* *Mac OS*

For Mac users, after decompressing the file, open the ``InfoScan`` file, enter the ``InfoScan.app/Contents/Macos directory``, and click ``InfoScan`` flie to run.

.. note:: Unlike Linux, you should place the downloaded genome file and/or the example data in the same directory of ``InfoScan`` flie mentioned above. (like ``InfoScan.app/Contents/Macos/genome`` and/or ``InfoScan.app/Contents/Macos/data``)

Configuration
---------------------------
Before uploading data, you should first configure the operating environment of the software, this step can be achieved through clicking the *Configuration* button at the bottom of the main window.

.. image:: /images/Configuration.png

.. note:: This step will automatically install some software through `conda <https://docs.conda.io/en/latest/>`_\ .  

.. tip:: For support or questions please make a post on `Biostars <http://biostars.org>`__. For feature requests or bug reports please open an issue on `github <https://github.com/worsteggs/InfoScan_readthedocs/issues>`__.
