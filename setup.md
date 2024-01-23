---
layout: page
title: Setup
---

## In a Data Carpentry Workshop  
This workshop is designed to be run on pre-imaged Amazon Web Services (AWS)
instances (a computer with all the required programs and files to which you will have access from your computer). 
Except for a spreadsheet program and an internet browser, all of the command 
line software and data used in the workshop are hosted on an Amazon 
Machine Image (AMI). If you are signed up to take 
a Pangenomics Data Carpentry Workshop, **you do not need to worry about setting
up an AMI instance.** The Carpentries staff will create an instance 
for you, which will be provided at no cost. 
This setup is true for both self-organized and centrally-organized workshops. 
Your Instructor will provide instructions for connecting to the AMI instance at the workshop.

If you are in The Carpentries-Workshop, you do not even need to install a bash terminal; the R-studio terminal provided in the AWS-AMI is enough to run all the commands in the lesson. 
Instead of connecting by `ssh`, users can simply use the R-studio AMI terminal. 

This lesson requires a working spreadsheet program. 
If you don't have a spreadsheet program already, you can use LibreOffice. 
It's a free, open-source spreadsheet program.

## Running the lesson by yourself (Not in a Data Carpentry Workshop)

### Required  software  
If you are not in a Data Carpentry Workshop, the software you need is listed in the table below. **Follow the instructions in Option A *or* Option B** to have access to these programs.  


| Software | Version | Manual | Available for | Description |
| -------- | ------------ | ------ | ------------- | ----------- |
| [Prokka](https://github.com/tseemann/prokka) | 1.14.6 | [GitHub](https://github.com/tseemann/prokka#invoking-prokka) | Linux, MacOC, Windows | Bacterial, archaeal and viral assembly annotation |
|[ncbi-genome-download](https://github.com/kblin/ncbi-genome-download)  | version | [GitHub](https://github.com/kblin/ncbi-genome-download#usage) | Available for | Downloading genomes from the NCBI |
|[Anvi'o](https://anvio.org/)| version |[Pangenomics Workflow Manual](https://merenlab.org/2016/11/08/pangenomics-v2/)|Linux & MacOS| *multi-omics* analysis including Pangenomics|
|[GET_HOMOLOGUES](https://github.com/eead-csic-compbio/get_homologues)|version|[GitHuB](http://eead-csic-compbio.github.io/get_homologues/manual/)|Available for| Sequence clustering|
|[PPanGGOLiN](https://github.com/labgem/PPanGGOLiN)|version |[GitHub Wiki](https://github.com/labgem/PPanGGOLiN/wiki)|Available for| Pangenomics |
|[RGI](https://github.com/arpcard/rgi/)|6.0.3|[GitHub](https://github.com/arpcard/rgi/)|Windows, MacOS, Linux|Resistome annotation|


### Option A: Using the lessons with Amazon Web Services (AWS)

Follow these [instructions on creating an Amazon instance](https://czirion.github.io/pangenomics-workshop/AMI-setup/index.html). Use the AMI `FIXME` named `FIXME` listed on the Community AMIs page. Please note that you must set your location as `N. Virginia` to access this community AMI. You can change your location in the upper right corner of the main AWS menu bar. The cost of using this AMI for a few days, with the t2.medium instance type, is very low (about USD $2.00 per user per day). Data Carpentry has *no* control over AWS pricing structure and provides this cost estimate without guarantees. Please read AWS documentation on pricing for up-to-date information. 

If you're an Instructor or Maintainer or want to contribute to these lessons, please contact us at [team@carpentries.org](mailto:team@carpentries.org), and we will start instances for you. 

In this instance, you can use the terminal available in RStudio, and users won't need
to install their own terminals or use `ssh` (see [Instructor Notes](https://czirion.github.io/pangenomics-workshop/guide/index.html)). **If, nevertheless, you
prefer that the users install their own terminals**, directions to install them are included 
for each Windows, Mac OS X, and Linux below in the Option B section. For Windows, you will need to install Git Bash, PuTTY, or the Ubuntu Subsystem.

### Option B: Following the lessons on your local machine  
If you trust that your computer is powerful enough and want to have all the programs installed, you can follow all the workshops without using an
AWS remote machine. To do this, you will need to install all of the software used in the workshop and obtain a copy of the
dataset. Instructions for doing this are below.  


#### **Data**   
The data used in this workshop are available on Zenodo. Please read the Zenodo 
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


#### **Install Miniconda3**

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

#### **Install NCBI-genome-download**

There are two ways to install this package. The first one is with `pip`. It is recommended to upgrade the `pip` version to the newest one.
Pip installation:
~~~
pip install --upgrade pip
pip install .
pip install ncbi-genome-download
~~~
{: .language-bash}

The other installation option is with Conda, you can refer to the website (highly recommended).
Conda installation:
~~~
conda install -c bioconda ncbi-genome-download
~~~
{: .language-bash}  


#### **Install Prokka**

Conda installation:
~~~
conda install -c conda-forge -c bioconda -c defaults prokka
~~~
{: .language-bash}  
MacOS installation:
~~~
sudo cpan Time::Piece XML::Simple Digest::MD5 Bio::Perl
git clone https://github.com/tseemann/prokka.git $HOME/prokka
$HOME/prokka/bin/prokka --setupdb
~~~
{: .language-bash}  

You can test your installation by typing `prokka` and it should display its help screen.  


#### **Install Anvi'o**
Options:  
* Install a stable release of anvi’o on a Mac, Linux, or Windows-running computer (best option for end users).  
* Use anvi’o from the active development branch (best option for developers).  
* Run anvi’o through its Docker containers without any installation (best option for the lazy).  

#### **Install RGI**

To conda install RGI, you must install mamba in base environment. Afterwards, create a new
environment and install RGI into it using mamba:

~~~
conda activate base
conda install mamba
mamba create -n rgi -c anaconda -c bioconda -c conda-forge rgi
~~~
{: .language-bash}

Test RGI by running the following commands:

~~~
conda activate /miniconda3/envs/rgi/
rgi main --help
~~~
{: .language-bash}

If you get an error stating *"ImportError: libffi.so.6: cannot open shared object file: No such file or directory"*,
you will have to install the `libffi6` package on your system. On Ubuntu and derivatives, you may install
it as follows:

~~~
wget https://mirrors.kernel.org/ubuntu/pool/main/libf/libffi/libffi6_3.2.1-8_amd64.deb
apt install ./libffi6_3.2.1-8_amd64.deb
rm libffi6_3.2.1-8_amd64.deb
~~~
{: .language-bash}

Retry test running RGI; you should not see the same error again.

## Connection to JupyterHub in CCM's servers (Notebooks and Terminal)
Open the JupyterHub server login site in a new tab with [this link](https://lab.matmor.unam.mx:8443/hub/login).
Open this [Google sheet](https://docs.google.com/spreadsheets/d/1Lg633gpV8KrUqTn34PDM8V0glAkTZpHcm4CViRRz1N0/edit#gid=1473209790) in a new tab and write your name in a user.
Use this user information to log in to the JupyterHub site that you opened in the previous step.

### Open a Bash Terminal
Click on the button "New" (upper right within the "Files" section) and choose the option "Terminal" from the drop-down menu. A new tab with a terminal will open.

### Open a Jupyter Notebook with the TDA environment
Click on the button "New" (upper right within the "Files" section) and choose the option "TDA" from the drop-down menu. A new tab with a notebook will open.

## Activating Conda environments

To activate a Conda environment in the Terminal of JupyterHub you need to specify the absolute path of the environment: `conda activate /miniconda3/envs/my-environment-name`    

