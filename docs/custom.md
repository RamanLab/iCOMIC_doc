## 7. Creating a custom pipeline

#### 7.1. Shell scripts to be written by the user
iCOMIC integrates most of the best practise tools for Whole Genome sequencing and RNA-seq data analysis. The toolkit provides the user the complete freedom to choose any compatible combination of tools for analysis. iCOMIC permits a user to add a new tool as well. If you are a developer, adding a new tool is easy as iCOMIC relies on Snakemake where the codes are very readable. The primary thing to be done for integrating an additional tool is to create a rule file inside the directory `iCOMIC/rules`. Name the file as `[TOOL_NAME].smk`. The major thing to be taken care of is the name of input and output files. It should match the other tools of the corresponding analysis step.

  ![](https://github.com/anjanaanilkumar1289/iCOMIC_doc/blob/master/docs/rule_snpeff.png?raw=true)
    
  

Parameters can be specified in the rule itself in the section `params`. If a snakemake wrapper is available for your choice of tool, that can be used, otherwise you need to write a shell command. List of snakemake wrappers are available in [Snakemake wrapper repository](https://snakemake-wrappers.readthedocs.io/en/stable/index.html). 

#### 7.2. How to run a custom pipeline
The user should create the rule for the new pipeline as mentioned in Section 7.1 . The user can either run the pipeline without GUI or with GUI.
To run without GUI the user should save the created rule as snakefile and can simply type the following command in the terminal. 

```
$ snakemake --use-conda -S snakefile_name
```

For running with iCOMIC, the user should edit icomic_v0.py file. The user should first choose the pipeline and edit accordingly. 
