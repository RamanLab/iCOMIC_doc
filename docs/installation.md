## 2. Installation

  

Setting up iCOMIC is comparatively effortless across Linux or Mac platforms. iCOMIC works with Python 3.6 or above.

#### 2.1. Prerequisites

- Linux/Windows/Mac platform

- Python 3.6 and above

- Miniconda

- iCOMIC package downloaded from GitHub


#### 2.2. Github download and installation

The entire source code for the tool is available at [this link](https://github.com/RamanLab/iCOMIC). The user can either download as a zip file directly or git clone 

#### 2.3. Conda Installation
Create an environment and install the dependencies associated with iCOMIC by using the following command 

Step 1:
```
$ cd iCOMIC-main 
```
After cloning iCOMIC directory, move inside the directory where the environment file exists. 

Step 2:
```
$ conda env create -f icomic_env.yml #for the first time only
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
