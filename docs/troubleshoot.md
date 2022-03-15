## 10. Troubleshooting runtime issues

#### 10.1. FAQs

-  General
1. How do I cite iCOMIC?

	Sithara, Anjana Anilkumar, Devi Priyanka Maripuri, Keerthika Moorthy, Sai Sruthi Amirtha Ganesh, Philge Philip, Shayantan Banerjee, Malvika Sudhakar, and Karthik Raman. “ICOMIC: A Graphical Interface-Driven Bioinformatics Pipeline for Analyzing Cancer Omics Data,” September 20, 2021. https://doi.org/10.1101/2021.09.18.460896

2. Where can I access the latest iCOMIC source code?

	You can access the codes [here](https://github.com/RamanLab/iCOMIC) and data [here](https://doi.org/10.5281/zenodo.5759698).  

3. As a Windows user, how do I set up iCOMIC?

	Same as other operating systems.
	
4. How to solve '**docker: Got permission denied while trying to connect to the Docker daemon socket at unix**' error while installing iCOMIC with Docker?
	
	Please change the permission of socket file by running the command 
	```
	$ sudo chmod 666 /var/run/docker.sock
	```
	It should solve the issue.
	
5. How to solve '**xhost:  unable to open display ":0"**' while Docker installation of iCOMIC?

	```
	$ xhost local:docker
	```
	or 
	```
	$ xhost local:root
	```

	Running either one of these commands should solve the issue
	
-  New Users

1. How do I report bugs and suggest improvements for iCOMIC?

	You can post the issues in this [link](https://github.com/RamanLab/iCOMIC/issues).

