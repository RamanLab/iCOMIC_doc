## 2. Installation

  

Setting up iCOMIC is comparatively effortless across Linux or Mac platforms. iCOMIC works with Python 3.6 or above.

#### 2.1. Prerequisites

- Linux/Windows/Mac(MacOS v10.15.5 or above) platform

- Python 3.6 and above

- Miniconda

- iCOMIC package downloaded from GitHub or Docker installed (only for Linux)


#### 2.2. Github download and installation

The entire source code for the tool is available at [this link](https://github.com/RamanLab/iCOMIC). The user can either download as a zip file directly or git clone and follow the steps in section 2.2.1

##### 2.2.1 Conda Installation
Create an environment and install the dependencies associated with iCOMIC by using the following command 

Step 1:
```
$ cd iCOMIC-main 
```
After cloning iCOMIC directory, move inside the directory where the environment file exists. 

Step 2 - **For Linux users**:
```
$ conda env create -f icomic_env.yml #for the first time only
```
This helps in creating an environment, which contains all the necessary requirements.

Step 2 - **For MacOS users**:
```
$ conda env create -f icomic_env_mac.yml #for the first time only
```
This helps in creating an environment, which contains all the necessary requirements.

Step 3:
```
$ conda activate icomic_env
```
Activating the created environment. 

Step 4:
```
$ pip install -e icomic #for the first time only
```
To install icomic

Step 5:
```
$ cd icomic #path/to/icomic directory
```
Move inside icomic directory to run the tool.

Step 6:
```
$ icomic
```
Opens the GUI by typing this command everytime.

step 7:
```
$ conda deactivate #after completing the analysis
```
Deactivates the environment

#### 2.3. Installation with Docker image

iCOMIC can be run in Linux system using docker image. Please [install the Docker](https://docs.docker.com/engine/install/) on your system and test the installation using 
```
$ docker -v
``` 

Running the following command, by default will launch iCOMIC and is ready to use. Make sure to add the path to your local directory containing samples. Docker support for Mac or Windows platforms will be extended in subsequent releases of iCOMIC.

```
$ docker run -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v </path/to/local/directory>:</path/to/local/directory> ramanlab/icomic:latest
```

Please visit [Troubleshooting](https://icomic-doc.readthedocs.io/en/latest/troubleshoot.html) section of this document if you encounter errors while docker installation of iCOMIC.

#### 2.4. Windows Installation

For iCOMIC, some dependencies are platform specific, and hence the environment file created in Linux failed when we tried to recreate it in Windows. The primary reason for this is that most NGS analysis tools are unix-based and consequently the conda environment for iCOMIC had to be created on an unix-based OS. Also, NGS analysis is computationally intensive and requires access to high performance computing (HPC) frameworks and since Linux is the most widely used OS for HPC systems, we feel that users won’t face any issue while running our pipelines. However, we have suggested a workaround in the documentation for users with a windows OS. This involves installing and opening iCOMIC by creating a Windows Subsystem for Linux (WSL) session inside MobaXterm, a widely-used toolbox for remote computing. Please find the steps mentioned below:

1. Install WSL. [Documentation](https://docs.microsoft.com/en-us/windows/wsl/install)
2. Install Miniconda inside WSL. [Reference](https://educe-ubc.github.io/conda.html)
3. Install MobaXterm Home edition. It is a free software that offers enhanced terminal for Windows with an X11 server. [Documentation](https://mobaxterm.mobatek.net/download.html)
4. Open a WSL terminal inside MobaXterm (Open MobaXterm --> Click on Sessions --> New Sessions --> WSL --> Select Linux distribution --> OK)
5. Follow the instructions in Section 2.2 of the iCOMIC documentation.

Note: While installing iCOMIC in Windows 11 Steps 3 and 4 can be skipped (if wanted) and this [documentation](https://docs.microsoft.com/en-us/windows/wsl/tutorials/gui-apps) can be followed instead.

