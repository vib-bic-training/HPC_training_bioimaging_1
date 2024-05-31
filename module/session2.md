# Infrastructure

## OOD on the VSC
### Tier 2 KUL
- How to connect: https://ondemand.hpc.kuleuven.be/ 
- Which services are available: code-server, shell, jupyterlab, nvidia rapids, RStudio Server, Tensorboard

### Tier 2 UGent
- How to connect: https://login.hpc.ugent.be
- Which services are available: BAND, Neurodesk, Cluster Desktop, shell, Jupyter Notebook, RStudio, Jupyter Lab, VS Code Tunnel, Code server

### Tier1 compute
- How to connect: https://tier1.hpc.ugent.be/ 
- Which services are available: BAND, Neurodesk, Cluster Desktop, Shell, Jupyter Notebook, RStudio, Jupyter Lab, VS Code Tunnel
  
## BAND
Bioimage Analysis Desktop is a virtual desktop developed by EMBL where software (cellpose, omnipose, fiji, cellprofiler and qupath, napari) are installed as containers.
![image](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/ec5c0fd3-b142-45c2-b241-a3baf84a449f)

It can be accessed through a webinterface and is ideal for training
How to launch BAND:
![Screenshot 2024-05-31 143602](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/cd52179f-08c1-4fec-9c15-d7b6157628ec)
![Screenshot 2024-05-31 143756](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/c8147424-9bbd-4aa5-bbc6-5b2234766a77)
Contact us if you have any doubt with the specification you need to feel in



## Neurodesk

Virtual desktop for data analysis in neuroimaging and it can be launched in a similar way than BAND.
![image](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/a9536c03-747e-46e7-a402-f4724248de78)

Interesting notebook or tutorials are:
- https://www.neurodesk.org/tutorials-examples/tutorials/
- [GitHub - NeuroDesk/example-notebooks: examples for using Neurodesk within Notebooks](https://github.com/NeuroDesk/example-notebooks)
For instance, slicer, vesselvio and ilastik are installed on neurodesk

To start Neurodesk:
![image](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/3e26569e-83ec-4497-a8e9-d0f55ea408ef)
![image](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/9283576b-b03e-4eb3-a4b9-dd64d504ae69)

Feel free to contact us if you want to Neurodesk

## Jupyter Notebook
How to run a notebook for denoising with n2v

![Screenshot 2024-05-31 145403](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/7b43dd8d-508d-456b-acd3-c37aa0fb661e)
![Screenshot 2024-05-31 143756](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/3f532e69-7c2e-4746-8fce-2710351ec1eb)

## Jupyter Lab

![image](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/184b607d-7702-447a-8874-457feb7c2e49)
![image](https://github.com/vib-bic-training/HPC_training_bioimaging_1/assets/103046100/a44c2822-06f2-44c7-9eee-4d97f658a4b4)



### How to load software for Jupyter Notebook or Jupyter Lab
- either use easybuild module but take care with compatibility with GCC core (see software.md)
- use own conda environment and make your own kernel but take care with compatibility with GCC core




