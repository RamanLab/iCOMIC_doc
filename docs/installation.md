## 2. Installation

  

Setting up iCOMIC is comparatively effortless across Linux or Mac platforms. iCOMIC works with Python 3.6 or above.

#### 2.1. Prerequisites

- Linux/Windows/Mac platform

- Python 3.6 and above

- Miniconda

- iCOMIC package downloaded from GitHub

- Memory requirement

#### 2.2. Github download and installation

The entire source code for the tool is available at “ [iCOMIC](https://github.com/RamanLab/iCOMIC) ”

#### 2.3. Conda Installation
Create an environment and install the dependencies associated with iCOMIC by using the following command 

Step 1:
```
$ conda env create -f icomic_env.yml #for the first time only
```

Step 2:
```
$ cd path/to/icomic/folder
```

Step 3:
```
$ conda activate icomic_env
```

Step 4:
```
$ pip install -e /path/to/iCOMIC folder #for the first time onl
```

Step 5:
```
$ icomic
```

step 6:
```
$ conda deactivate #after completing the analysis
```
