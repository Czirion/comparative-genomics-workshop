---
layout: page
title: Setup
---

## In a Data Carpentry Workshop

During a Data Carpentry Workshop, you'll be supplied with a server by CCM UNAM.
Your Instructor will provide instructions for connecting to an instance at the
workshop. You'll need an up-to-date web browser (Firefox, Safari, Chrome or
Edge), and a working spreadsheet program. If you don't have the latter, you can
install [LibreOffice](https://www.libreoffice.org/download/download-libreoffice/),
a free and open source office suite which includes a spreadsheet program called
Calc.

## Running the lesson by yourself (Not in a Data Carpentry Workshop)

### Required software and packages

The following tables lists all the required software for the workshop.

|Software|Version|Manual|Available for|Description|
|:--------|:------------|:------|:-------------|:-----------|
|[BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)|2.12|[BLAST Command Line Applications User Manual](https://www.ncbi.nlm.nih.gov/books/NBK279690/)|Linux, MacOS & Windows|Similarity regions identifier between biological sequences|
|[Prokka](https://github.com/tseemann/prokka)|1.14.6|[GitHub](https://github.com/tseemann/prokka#invoking-prokka)|Linux, MacOS & Windows|Bacterial, archaeal and viral assembly annotation|
|[ncbi-genome-download](https://github.com/kblin/ncbi-genome-download)|0.3.3|[GitHub](https://github.com/kblin/ncbi-genome-download#usage)|Linux, MacOS & Windows|Downloading genomes from the NCBI|
|[Anvi'o](https://anvio.org/)|7.1|[Pangenomics Workflow Manual](https://merenlab.org/2016/11/08/pangenomics-v2/)|Linux & MacOS|Multi-omics analysis including pangenomics|
|[GET_HOMOLOGUES](https://github.com/eead-csic-compbio/get_homologues)|3.6.2|[GitHub](http://eead-csic-compbio.github.io/get_homologues/manual/)|Linux, MacOS & Windows|Sequence clustering|
|[PPanGGOLiN](https://github.com/labgem/PPanGGOLiN)|2.0.5|[GitHub Wiki](https://github.com/labgem/PPanGGOLiN/wiki)|Linux & MacOS|Pangenomics|
|[RGI](https://github.com/arpcard/rgi/)|6.0.3|[GitHub](https://github.com/arpcard/rgi/)|Linux, MacOS & Windows|Resistome annotation|
|[Python](https://www.python.org/)|At least 3.7|[Python Docs](https://docs.python.org/)|Linux, MacOS & Windows|General-purpose programming language|

You will also need the following Python packages to be available: gudhi,
jupyter, matplotlib, networkx, numpy, pandas, plotly, requests, scikit-learn,
scipy, and seaborn.

While you could install each of these requirements manually, it is a highly
laborious process; thus we provide a ready-to-use
[Docker image](https://hub.docker.com/repository/docker/aapashkov/panworkshop)
with all of these dependencies included. A Docker **image** is a file used to
create a Docker **container**, which is an encapsulated environment storing
everything a project or software needs for it to function. Follow the
instructions of the section labeled **Option A** to learn how to set up a Docker
container for our workshop, or read the section **Option B** if you prefer to
install everything by yourself.

### Option A: Running the Docker image

1. If you haven't done so already, install Docker Engine or Docker Desktop on
your system by following [these instructions](https://docs.docker.com/engine/install/).
2. Next, open a terminal (in Linux and MacOS) or PowerShell (in Windows) in an
empty folder, and type the following command to start a container from our
image, replacing `NAME` with any memorable name you wish (the first time you
execute this command, it will take a while as it will download the entire
image):
    ~~~
    docker run -itv $(pwd):/root --name NAME aapashkov/panworkshop
    ~~~
    {: .language-bash}
3. You are now connected to the Docker container, and are ready to get started
with the workshop! Type `exit` to leave the container. If you wish to connect
back to it, please type the following two commands (replacing `NAME` with the
name you chose in step 2):
    ~~~
    docker start NAME
    docker attach NAME
    ~~~
    {: .language-bash}
4. To delete a container after you have exited it, run this command (once again,
use the same `NAME` as from step 2):
    ~~~
    docker rm NAME
    ~~~
    {: .language-bash}

### Option B: Installing dependencies manually

#### **Data**   
The data used in this workshop is available on Zenodo. Please read the Zenodo 
page linked below for information about the data and access to the data files. Because this workshop works 
with real data, be aware that file sizes for the data are large.
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7620503.svg)](https://doi.org/10.5281/zenodo.7620503)

More information about these data will be presented in the [first episode of the Pangenome Analysis in Prokaryotes lesson](https://paumayell.github.io/pangenomics/01-introduction/index.html).  

#### **Install a Bash terminal** 

> ## Windows
> - Download the [Git for Windows installer](https://git-for-windows.github.io/). Run the installer and follow the steps below:
>   + Click on "Next" four times (two times if you've previously installed Git). You don't need to change anything in the information, location, components, and start menu screens.
>   + Select "Use the nano editor by default" and click on "Next".
>   + Keep "Use Git from the Windows Command Prompt" selected and click on "Next". If you forget to do this, the programs that you need for the workshop will not work properly. If this happens, rerun the installer and select the appropriate option.
>   + Select "Use bundled OpenSSH" and click on "Next".
>   + Select "Use the OpenSSL Library" and click "Next".
>   + Keep "Checkout Windows-style, commit Unix-style line endings" selected and click on "Next".
>   + Select "Use Windows' default console window" and click on "Next".
>   + Select "Default (fast-forward on merge)" and click on "Next".
>   + Select "None" (Do not use a credential helper) and click on "Next".
>   + Select "Enable file system caching" and click on "Next".
>   + Ignore "Configuring experimental options" and click on "Install".
>   + Click on "Install".
>   + Click on "Finish".
>   + If your "HOME" environment variable is not set (or you don't know what this is):
>   + Open command prompt (Open Start Menu, then type `cmd` and press [Enter])
>   + Type the following line into the command prompt window exactly as shown: `setx HOME "%USERPROFILE%"`
>   + Press [Enter], and you should see `SUCCESS: Specified value was saved.`
>   + Quit the command prompt by typing `exit` and then pressing [Enter]
>   + See the [video tutorial](https://youtu.be/yo7Z-BEG62A) for an example of how to install Git on Windows 11.
>   
> - An **alternative option** is to install PuTTY
>  by going to the [the installation page](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html). For most newer computers, click on putty-64bit-X.XX-installer.msi to download the 64-bit version. If you have an older laptop, you may need to get the 32-bit version putty-X.XX-installer.msi. If you aren't sure whether you need the 64 or 32-bit version, you can check your laptop version by following [the instructions here](https://support.microsoft.com/en-us/help/15056/windows-32-64-bit-faq). Once the installer is downloaded, double-click on it, and PuTTY should install.
> - **Another alternative option** is to use the Windows Subsystem Linux (WSL). This option is available for Windows 10 and Windows 11 - detailed [instructions are available here](https://learn.microsoft.com/en-us/windows/wsl/install).
> See the [video tutorial](https://youtu.be/YoNdTuN-YWk) for an example of how to install WSL with Ubuntu 22.04 on Windows 11.
> 
{: .solution}

> ## macOS
> -  The default shell in some versions of macOS is Bash, and Bash is available in all versions, so no need to install anything. You access Bash from the Terminal Application (found in /Applications/Utilities). See how to open the terminal in the [video tutorial](https://www.youtube.com/watch?v=FuNsWg_VzeQ). You may want to keep the terminal in your dock for this workshop.
{: .solution}

> ## Linux
>  - The default shell is usually Bash, and there is usually no need to install anything. To see if your default shell is Bash type, echo $SHELL in a terminal and press the Enter key. If the message printed does not end with `/bash`, then your default is something else, and you can run Bash by typing `bash`.
{: .solution}  

#### Install Miniconda3

These instructions assume familiarity with the command line and with installation 
in general. There are different operating systems and many different versions
of operating systems and environments, so these may not work on your computer. If an 
installation doesn't work for you, please refer to the user guide for the tool listed in the table above.
If you have difficulties with the installations or find better ways to install things in your operating system, please raise an [Issue](https://github.com/carpentries-incubator/metagenomics/issues) to let us know.

To make a [Conda](https://conda.io/projects/conda/en/latest/index.html) environment, first, you need to install Conda. We recommend installing the [Miniconda3](https://docs.conda.io/en/latest/miniconda.html) version. Miniconda is a package manager that includes Conda and its dependencies and simplifies the installation process. Please first install Miniconda3 (installation instructions below) and then proceed to the installation of the environment.

> ## Linux
> 
> To install miniconda3, see the [video tutorial](https://youtu.be/0PqwShSDH20)
{: .solution}

> ## MacOSX
> In a terminal type:
> ~~~
> $ curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
> $ bash Miniconda3-latest-MacOSX-x86_64.sh
> ~~~
> {: .bash}
> Then, follow the instructions that you are prompted with on the screen to install Miniconda3.
{: .solution}

> ## WSL
> See the video tutorial, [installing Miniconda3 on WSL Ubuntu](https://youtu.be/owQgZoE-GrY)
{: .solution}  

#### Create the virtual environments

First, make sure to set a faster dependency solver, add necessary channels,
update conda, and install BLAST into your base environment.

~~~
conda config --set solver libmamba
conda config --add channels conda-forge
conda config --add channels bioconda
conda update --quiet --yes --all
conda install --yes --name base blast=2.12
~~~
{: .language-bash}

Download every `.yml` file found in
[this link](https://github.com/carpentries-incubator/pangenomics-workshop/tree/gh-pages/files/docker/env)
somewhere easily accessible. These files are environment definitions for the
virtual environments to be used during the workshop. Next, open a terminal
inside the directory where you downloaded these files, and create the virtual
environments using the following command:

~~~
for file in *.yml; do
    conda env create --quiet --yes --file "$file"
done
~~~
{: .language-bash}

After this step, if you list your conda environments, you should expect
something like the following:

~~~
conda env list
~~~
{: .language-bash}
~~~
# conda environments:
#
base                  *  /miniconda3
Pangenomics_Global       /miniconda3/envs/Pangenomics_Global
TDA                      /miniconda3/envs/TDA
anvio-7.1                /miniconda3/envs/anvio-7.1
ncbi-genome-download     /miniconda3/envs/ncbi-genome-download
rgi                      /miniconda3/envs/rgi
~~~
{: .output}

You should now perform two more steps to get up and running with your
environments.

#### Download and extract databases

Download the `panworkshop-databases.tgz` file from
[this Zenodo link](https://zenodo.org/records/11374283) and decompress it using
the following command:

~~~
tar -C / -zxf panworkshop-databases.tgz
~~~
{: .language-bash}

#### Test run RGI

Test RGI by running the following commands:

~~~
conda activate /miniconda3/envs/rgi/
rgi main --help
~~~
{: .language-bash}

If you get an error stating *"ImportError: libffi.so.6: cannot open shared
object file: No such file or directory"*, you will have to install the `libffi6`
package on your system. On Ubuntu and derivatives, you may install it as
follows:

~~~
wget https://mirrors.kernel.org/ubuntu/pool/main/libf/libffi/libffi6_3.2.1-8_amd64.deb
apt install ./libffi6_3.2.1-8_amd64.deb
rm libffi6_3.2.1-8_amd64.deb
~~~
{: .language-bash}

Retry test running RGI; you should not see the same error again.

## Connection to JupyterHub in servers from CCM UNAM (Notebooks and Terminal)

### User credentials

As stated in the beginning of this page, during a workshop you'll be provided
with user credentials for servers from CCM UNAM by your Instructor. If you wish
to run the lessons by yourself, or are planning to be an Instructor of this
workshop, please contact [nselem@matmor.unam.mx](mailto:nselem@matmor.unam.mx)
in order to access the user credentials for the servers.

### Open a Bash Terminal

Click on the button "New" (upper right within the "Files" section) and choose
the option "Terminal" from the drop-down menu. A new tab with a terminal will
open.

### Open a Jupyter Notebook with the TDA environment

Click on the button "New" (upper right within the "Files" section) and choose
the option "TDA" from the drop-down menu. A new tab with a notebook will open.

### Activating Conda environments

To activate a Conda environment in the Terminal of JupyterHub you need to
specify the absolute path of the environment:
`conda activate /miniconda3/envs/my-environment-name`    
