<!--

author:   Tatiana Woller, Bruna Piereck, Alexander Botzki
email:    training@vib.de
version:  1.0.0
language: en
narrator: UK English Female

icon:     https://vib.be/sites/vib.sites.vib.be/files/logo_VIB_noTagline.svg

comment:  This document shall provide an entire compendium and course on the
          development of Open-courSes with [LiaScript](https://LiaScript.github.io).
          As the language and the systems grows, also this document will be updated.
          Feel free to fork or copy it, translations are very welcome...

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js
          https://felixhao28.github.io/JSCPP/dist/JSCPP.es5.min.js

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css
link:     https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css
link:     https://raw.githubusercontent.com/vibbits/material-liascript/master/img/org.css
link:     https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css
link:     https://fonts.googleapis.com/css2?family=Saira+Condensed:wght@300&display=swap
link:     https://fonts.googleapis.com/css2?family=Open+Sans&display=swap
link:     https://raw.githubusercontent.com/vibbits/material-liascript/master/vib-styles.css

@orcid: [@0](@1)<!--class="orcid-logo-for-author-list"-->

## Software
The easiest way to use software on the VSC, is to use the pre-installed software, that is installed as an Easy Build module.
Alternatively, you could create your own conda/mamba environment and use it in a python script or a jupyter notebook.
More advanced ways to user/run software are: - using singularity containers
- running nextflow workflow
  
### CPU vs GPU

Not all software are relying on GPU.
- CPU software: Fiji, QuPath
- GPU software: Cellpose, Omnipose, Napari and its plugins, Ilastik, ...

### Installed software

<!-- style="color: magenta ;" --> 
#### How to use a Easy Build module in command line (add a ! to use this command in a jupyter notebook)
- See loaded modules
```
ml
module list
```
- See available modules 
```
module avail
```
- Search for a module X
```
module av |& grep -i X
```
- Search for a module X and get details
```
module spider X
```
- Load a module X
```
module load x
```
- Unload a module X
```
module unload x
```
- Swap a module Y to X
```
module swap Y  X
```
- Remove all loaded modules except the cluster one
```
module purge
```
:warning: Do not load modules built with intel and foss toolchains

🗎 https://docs.vscentrum.be/software/software_stack.html#using-the-module-system

#### How to load module in jupyter notebook
Select the appropriate version of the jupyter notebook and load the easy build module accordingly

![image](https://github.com/vibbits/bioimaging-starting-grant/assets/103046100/70dfd6f5-becc-4fb5-9a8a-6b4274a54bad)

i.e. 6.4.0 GCC core 11.3.0 IPython 8.5.0 is compatible with foss-2022a or intel 2022a modules (see compatibility table below)
| FOSS  | GCC |  CUDA | OpenMPI | OpenBLAS | FFTW | ScaLAPACK |
| ------| --- | ----- | ------- | -------- | ---- | --------- |
| 2022b | 12.2.0 | 12.0.0 | 4.1.4 | 0.3.21 | 3.3.10 | 2.2.0-fb |
| 2022a | 11.3.0 | 11.7.0 | 4.1.4 | 0.3.20 | 3.3.10 | 2.2.0-fb |
| 2021b | 11.2.0 | - | 4.1.1 | 0.3.18 | 3.3.10 | 2.1.0-fb |
| 2021a | 10.3.0 | - | 4.1.1 | 0.3.15 | 3.3.9 | 2.1.0-fb |
| 2020b | 10.2.0 | - | 4.0.5 | 0.3.12 | 3.3.8 | 2.1.0 |
| 2020a | 9.3.0 | - | 4.0.3 | 0.3.9 | 3.3.8 | 2.1.9 |
| 2019b | 8.3.0 | - | 3.1.4 | 0.3.7 | 3.3.8 | 2.0.2 |

For more information about modules: https://hprc.tamu.edu/kb/Software/GNU-Compiler-Collection/ 

#### Compatibility python version - GCCcore on Tier-1 (Hortense)
 Table for jupyter notebook
 
| IPython version  | Python |GCCcore |
| ------------- | ------------- |-------------|
| 7.25.0-GCCcore-10.3.0 | Python 3.9.5 | GCCcore-10.3.0|
| 6.4.0-GCCcore-11.2.0  | Python 3.9.6 | GCCcore-11.2.0|
| 8.5.0-GCCcore-11.3.0 | Python 3.10.4 | GCCcore-11.3.0|
| 7.0.3 GCCcore 12.2.0 | Python 3.10.8 | GCCcore 12.2.0|
| 7.0.2 GCCcore 12.3.0 | Python 3.11.3 | GCCcore 12.3.0|


 How to see what is loaded with the module:
 ``` ml show  IPython/8.5.0-GCCcore-11.3.0 ```

#### Modules for bioimage analysis in python
1. [Napari](https://github.com/napari/napari): Napari/0.4.15-foss-2021b or Napari/0.4.18-foss-2022a
2. [Cellpose](https://github.com/MouseLand/cellpose): Cellpose/2.2.2-foss-2022a or Cellpose/2.2.2-foss-2022a-CUDA-11.7.0
3. Omnipose:  Omnipose/0.4.4-foss-2022a-CUDA-11.7.0 or  Omnipose/0.4.4-foss-2022a
4. [stardist](https://github.com/stardist/stardist): stardist/0.8.3-foss-2021b-CUDA-11.4.1 or stardist/0.8.3-foss-2021b
5. [AICSImageIO](https://github.com/AllenCellModeling/aicsimageio) : AICSImageIO/4.14.0-foss-2022a
6. [devbio-napari](https://github.com/haesleinhuepf/devbio-napari) : devbio-napari/0.10.1-foss-2022a-CUDA-11.7.0
7. [n2v](https://github.com/juglab/n2v) : n2v/0.3.2-foss-2022a-CUDA-11.7.0
8. Monai: MONAI/1.0.1-foss-2022a
9. QuPath: QuPath/0.5.0-GCCcore-12.3.0-Java-17
10. 

#### Module for spatial omics in python
1. [Scanpy](https://github.com/scverse/scanpy): scanpy/1.9.1-foss-2021b
2. Seurat: Seurat/4.3.0-foss-2021b-R-4.1.2
3. Squidpy: Squidpy/1.2.2-foss-2021b
4. [Giotto](https://drieslab.github.io/Giotto/): Giotto-Suite/3.0.1-foss-2022a-R-4.2.1

#### Module for bio-image analysis tools
1. Fiji: Fiji/2.9.0-Java-1.8
2. Cellprofiler: CellProfiler/4.2.4-foss-2021a

#### General libraries 
1. Scikit-learn: scikit-learn/1.1.2-foss-2022a or scikit-learn/1.0.1-foss-2021b
2. Scikit-image: scikit-image/0.19.3-foss-2022a or scikit-image/0.19.1-foss-2021b
3. scipy: SciPy-bundle/2022.05-foss-2022a, SciPy-bundle/2021.10-foss-2021b
4. seaborn: Seaborn/0.11.2-foss-2021b
5. tifftile: Scikit-image/0.19.1-foss-2021b 
6. tensorflow: TensorFlow/2.7.1-foss-2021b-CUDA-11.4.1 or TensorFlow/2.7.1-foss-2021b
7. R : R/4.2.1-foss-2022a or R/4.0.0-foss-2020a
8. R studio: RStudio-Server/1.3.959-foss-2020a-Java-11-R-4.0.0 
9. Jupyter notebook: JupyterLab/3.1.6-GCCcore-11.2.0
10. Matplotlib: matplotlib/3.5.2-foss-2022a or matplotlib/3.4.3-intel-2021b
11. Bioconductor:  R-bundle-Bioconductor/3.14-foss-2021b-R-4.1.2

### How to create your own conda or mamba environment

## Install miniconda    

- Connect to [Tier2 via ondemand](https://ondemand.hpc.kuleuven.be/) (or to [Tier2 Ghent](https://login.hpc.ugent.be/))
- Open an `Interactive Shell` 
  ![image](https://github.com/vibbits/reprohack_bioimaging/assets/1775952/270dfc7f-3cbf-4d4c-943f-fb276008e8c3)
- Go to the $VSC_DATA location and install miniconda
```
cd $VSC_DATA 
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh -b -p $VSC_DATA/miniconda3
```
-Make conda available to the path:
```
export PATH="${VSC_DATA}/miniconda3/bin:${PATH}"
```

## Install mambaforge
mamba is a reimplementation of the conda package manager in C++.
It allows parallel downloading of repository data and package files using multi-threading and use libsolv for much faster dependency solving
```bash
cd $VSC_DATA 
wget "https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-$(uname)-$(uname -m).sh"
bash Mambaforge-$(uname)-$(uname -m).sh
export PATH="${VSC_DATA}/mambaforge/bin:${PATH}"
```

## Create the conda environment
- Create the conda environment from the yaml file
```
conda env create -f cellpose-omnipose-gpu.yml
```
or
```
mamba env create -f cellpose-omnipose-gpu.yml
```
- Make it available for the jupyter notebook
```
source activate cellpose-omnipose-gpu
export PATH="${VSC_DATA}/miniconda3/bin:${PATH}
conda install ipykernel
python -m ipykernel install  --prefix=${VSC_HOME}/.local/ --name 'cellpose'
```
In this example, the conda envirmnemnt will be accessible under the name `cellpose`

## Use the conda enviroment with a jupyter notebook

:warning: **The ondemands interface doesn't wok well on Firefox, it's best to use Chrome**:warning:

- After connecting to JupyterLab
![image](https://github.com/vibbits/reprohack_bioimaging/assets/1775952/8ee777a7-2498-43a7-ade6-c063ea96d4de)
- Create a new notebook `File > New > Notebook`
![image](https://github.com/vibbits/reprohack_bioimaging/assets/1775952/39470a8d-424f-4c79-a9f6-d2a7a3f59774)
- Select the newly create conda enviroment (e.g. here, `cellpose`)
![image](https://github.com/vibbits/reprohack_bioimaging/assets/1775952/4db7fde7-ff6e-4287-b17c-decc1a641525)
- Start to write the notebook






