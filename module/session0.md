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

# Bioimage analysis on HPC

> This material in under active development at the moment

**Hello and welcome to our HPC workshop, we are very happy to have you here!** 
================================================================================
**This workshop is jointly organised by the VIB Technologies and VIB Bioimaging Core.**
========================================================================================

> This materia is a distributed way of creating and sharing educational content hosted on github.
> To see this document as an interactive LiaScript rendered version, click on the
> following link/badge:
>
> [![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://raw.githubusercontent.com/tatianawoller/Training_prep_290524/main/overview.md?token=GHSAT0AAAAAACM5JJ7CACQBVWAOQOVXRGNWZOCHBHA#1)

<section>

### Lesson overview

> <i class="fa fa-bookmark"></i> **Description**  
> This is our interactive hands-on course about the use of HPC (High Performance Computing).
> 
> <i class="fa fa-arrow-left"></i> **Prerequisites**  
> To be able to follow the **General** HPC course, you should:
> 
> 1. Have notions of command line and scripting
> 2. Be comfortable working with remote desktop
>
> To be able to follow the **Bioimaging** HPC course, you should:
>
> 1. Knowledge of image analysis 
>
> <i class="fa fa-arrow-right"></i> **Learning Outcomes (LO's):**  
> 
> <svg xmlns="http://www.w3.org/2000/svg" height="14" width="16" viewBox="0 0 576 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2023 Fonticons, Inc.--><path d="M384 64c0-17.7 14.3-32 32-32H544c17.7 0 32 14.3 32 32s-14.3 32-32 32H448v96c0 17.7-14.3 32-32 32H320v96c0 17.7-14.3 32-32 32H192v96c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32h96V320c0-17.7 14.3-32 32-32h96V192c0-17.7 14.3-32 32-32h96V64z"/></svg> **Level:** Beginner   
> 
> **By the end of the course, learners will be able to:**
>
>> - **General LO's**
>> 
>> 1. Explain the (potential) use of scientific high-performance computing
>> 2. Learn how to access existing supercomputer infrastructures in Flanders (VSC)
>> 2. Know the different environments they can use in the VSC to store, analysis and debug
>> 3. Find and use modules that are available in the VSC for their analysis
>> 4. Create and adapting scripts to run jobs and check information based on the submission method
>
>**Target Audience:** Scientific staff, trainers, training providers
>
>> - **Bioimaging Specific LO's:**  
>>
>> 1. Discuss how scientific high-performance computing enables to scale up bioimage analysis and opens new avenues for research>
>> 1. Identify which online and reusable resources are available for your Bioimaging problem (i.e., bioimage model zoo or other resources)
>> 2. Run image analysis jupyter notebook and dedicated software's through Open On Demand
>> 3. Discuss how to improve reproducibility in image analysis
>
>**Target Audience:** Bioimaging Researchers and technical support, trainers, training providers

> <i class="fa fa-hourglass"></i> **Time estimation General session**: 1/2 day 
>
> <i class="fa fa-hourglass"></i> **Time estimation General session + Bioimaging**: 1 day 

<i class="fa fa-lock"></i> **License:** 

<img src="https://raw.githubusercontent.com/vibbits/rdm-course-2022/main/images/logos/CC-by.png" title="" alt="" width="143">

[**Creative Commons Attribution 4.0 International  License**](https://creativecommons.org/licenses/by/4.0/)

<i class="fa fa-money-bill"></i> **Funding:**  ....

<i class="fa fa-asterisk"></i> **General Requirements (Technical):** 

You can find here a list of technical details you need to get prepared in oder to follow this course. You can find some help on ***HOW?*** in the specific sessions in the material of this course. 

 - Create a VSC account 
 - Create and enable SSH key
 - Globus

<i class="fa fa-asterisk"></i> **Bioimaging Requirements (Technical):** 

 - Experience in image analysis

<i class="fa fa-life-ring"></i> **Acknowledgement**: 

 * [ELIXIR Belgium](https://www.elixir-belgium.org/)
 * [VIB Technologies](https://www.vib.be/)

<i class="fa fa-anchor"></i> **PURL**: to be added 

### Authors

| | | |
|---|---|---| 
| [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0001-6691-4233)Alexander Botzki | [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0000-0000-0000)Benjamin Pavie | [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0000-0000-0000)Sebastian Munck |
| [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0000-0000-0000)Tatiana Woller | [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0001-5958-0669)Bruna Piereck | [![ORCID](https://raw.githubusercontent.com/vibbits/rdm-introductory-course/main/images/logos/32px-ORCID_iD.svg.png)](https://orcid.org/0000-0000-0000-0000)Janick Mathijs |

### Contributors

Part of this training was reused from the [NextFlow](https://github.com/vibbits/nextflow-workshop) course from VIB/ELIXIR-BE session.

### Citing this lesson

Please cite as:

  1. ....

## Schedule

Schedule day 1:

| Time | Session |
|  --- |   ---   |
| 09:30 - 11:00 | Introduction  and HPC infrastructure |
| 11:00 - 11:15 | break   |
| 11:15 - 12:45 | HPC infrastructure and Data transfer |
| 12:45 - 13:15 | lunch   |
| 13:15 - 15:00 | Napari and Napari plugins |
| 15:00 - 15:15 | break   |
| 15:15 - 16:00 | Napari plugins, Cellpose, QuPath |
| 16:00 - 16:30 | Jupyter notebook |
| 16:30 - 17:00 | Conclusion and outlook|
_We aim to complete up to and including exercise 2.5 during this day_

</section>
