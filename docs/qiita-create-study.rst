
This tutorial will walk you through creation of your account and a test study
in Qiita.

Getting CMI Workshop example data
---------------------------------

There are 2 separate data sets made available to you - *processing dataset* containing raw sequencing files which we will process to generate information
about the identity and relative amounts of microbes in our samples, and *analysis dataset* which contains more pre-processed samples which we will use
for statistical analyses.

Processing example data
~~~~~~~~~~~~~~~~~~~~~~~
You can `download example data <https://github.com/biocore/cmi-workshops/blob/master/docs/example_data/qiita-files.zip?raw=true>`__ directly from GitHub.
These files contain both 16S rRNA microbiome data for 14 skin microbiome samples. It is a subset of data which we will later use for analysis.
Real sequencing data can be tens of gigabytes in size!

The files are:

   * CMI_workshop_lane1_S1_L001_*_001.fastq.gz    # 16S sequences - forward (R1) and reverse (R2) reads and barcodes (I1)  
   * sample_information.txt                       # The sample information file  
   * prep_information_16S.txt                     # The prep information file


Analysis example data
~~~~~~~~~~~~~~~~~~~~~
Example data which you can use for analysis is available to you directly on Qiita. You don't need to download anything to your hard drive.
Instructions how to access this data are provided in the analysis `tutorial <http://cmi-workshop.readthedocs.io/en/latest/qiita-16S-analysis.html>`__.

Setting up Qiita
----------------

Signing up for a Qiita account
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Open your browser (it must be Chrome or Firefox) and go to `Qiita <https://qiita.ucsd.edu>`__ (https://qiita.ucsd.edu).

Click on "Sign Up" on the upper-right-hand corner.

.. figure::  images/sign_up.png
   :align:   center

The "New User" link brings you to a page on which you can create a new
account. Optional fields are indicated explicitly, while all other
fields are required. 

.. figure::  images/user_information.png
   :align:   center

Once the form is submitted, an email will be sent
to you containing instructions on how to verify your email address.

Logging into your account and resetting a forgotten password
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you have created your account, you can log into the system by
entering your email and password.

.. figure::  images/top_screen.png
  :align:   center

If you forget your password, you will need to reset it.  Click on
“Forgot Password”.

This will take you to a page on which to enter your email address; once
you click the “Reset Password” button, the system will send you further
instructions on how to reset your lost password.

.. figure::  images/forgot_password.png
  :align:   center

Updating your settings and changing your password
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you need to reset your password or change any general information in
your account, click on your email at the top right corner of the menu
bar to access the page on which you can perform these tasks.

.. figure::  images/forgot_password.png
  :align:   center

Creating a test study
---------------------

Studies are the source of data for Qiita. Studies can contain only one set
of samples but can contain multiple sets of raw data, each of which can have a
different preparation -- for example, 16S, shotgun metagenomics, and
metabolomics, or even multiple preparations of the same type
(e.g., a plate rerun, biological and technical replicates, etc).

In this tutorial, our study contains 30 samples, each with two types of data:
16S and metabolomic. To represent this project in Qiita, you will need
to create a single study with a single sample information file that contains all
30 samples. Then, you will link separate preparation files for each data type.

Creating an example study
-------------------------

To create a study, click on the "Study" menu and then on "Create Study".
This will take you to a new page that will gather some basic information
to create your study.

.. figure::  images/create_study.png
   :align:   center

The "Study Title" has to be unique system-wide. Qiita will check this
when you try to create the study, and may ask you to alter the study
name if the one you provide is already in use.

.. figure::  images/create_new_study3.png
   :align:   center

A principal investigator is required, and a list of known PIs is
provided. If you cannot find the name you are looking for in this
list, you can choose to add a new one.

Select the environmental package appropriate to your study. Different
packages will request different specific information about your samples.
For more details, see the `publication <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3367316>`__.

There is also an option to specify time series type ("Event-Based Data") if you
have such data. In our case, the samples come from a time series
study design, so you should select "multiple intervention, real".
For more information on time series types, you can check out the
`in-depth tutorial <https://qiita.ucsd.edu/static/doc/html/tutorials/getting-started.html#creating-a-study>`__
on the Qiita website.

Once your study has been created, you will be informed by a green
message; click on the study name to begin adding your data.

.. figure::  images/green_message2.png
   :align:   center


Adding sample information
-------------------------

**Sample information** is the set of metadata that pertains to your biological
samples: these are the measured variables that are motivating you to look for
response variables in the microbiome. **IMPORTANT**: your metadata are your
study; it is imperative that those data are consistent, correct, and
sufficiently detailed. (To learn more, including how to format your own sample
info file, check out the `in-depth documentation <https://qiita.ucsd.edu/static/doc/html/tutorials/prepare-information-files.html#sample-information-file>`__
on the Qiita website.)

The first point of entrance to a study is the study description
page. Here you will be able to edit the study info, upload files, and
manage all other aspects of your study.

.. figure::  images/new_study_link4.png
   :align:   center

The first step after study creation is uploading files. Click on the
"Upload Files" button: as shown in the figure below, you can now drag-and-drop
files into the grey area or simply click on "select from your computer"
to select the fastq, fastq.gz or txt files you want to upload.

Uploads can be paused at any time and restarted again, as long as you do
not refresh or navigate away from the page, or log out of the system
from another page.

Drag the file named "sample_information.txt" into the upload box. It should
upload quickly and appear with a checkbox next to it below.

.. figure::  images/upload_box4.png
   :align:   center

Once your file has uploaded, click on "Go to study description" and, once
there, click on the "Sample Information" tab.  Select your sample information
from the dropdown menu next to "Upload information" and click "Create".

.. figure::  images/sample_information_upload4.png
   :align:   center

If something is wrong with the sample information file, Qiita will let you know
with a red banner at the top of the screen.

.. figure::  images/sample-information-failure.png
   :align:   center

If the file processes successfully, you should be able to click on the "Sample
Information" tab and see a list of the imported metadata fields.

.. figure::  images/sample_information_works4.png
   :align:   center


You can also click on "Sample and preparation summary" to check out the different metadata
values. Select a metadata column to visualize in the "Add sample column information to table" dropdown menu and click
"Add column."

.. figure::  images/sample_summary5.png
   :align:   center


Next, we'll add 16S raw data and process it.

----

Next: :doc:`qiita-16S-processing`
