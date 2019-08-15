#### Functional Connectivity on Chronic Low Back Pain (CLBP) patients ####
## By Christophe Tanguay-Sabourin (GitHub: CTanguay-Sabourin)##

Here is my project for the Brain Hack School 2019. 


## Which dataset do I want to analyze? ##
For my project, I will use a dataset available on **OpenPain**, an open access data sharing platform for brain imaging studies of human pain. You can find the data set *Placebo_1* on http://www.openpain.org/index.html, provided by the Apkarian Lab, situated in Northwestern University.

*NOTE: The structural data are currently not available on OpenPain (only functional data), but they should be in September.*

![CLBP](http://dev.www.health.harvard.edu/media/content/images/L0714e-1.jpg)

This dataset comes from an RCT study investigating the determinants of placebo response. I will use the control group (i.e without placebo treatment; 68 participants) using their structural (T1w) and functioncal (rsfMRI) scans, during their first scanning session. For more information about the dataset, you may also refers to its original study:

#### Vachon-Presseau, E., Berger, S. E., Abdullah, T. B., Huang, L., Cecchi, G. A., Griffith, J. W., … Apkarian, A. V.         (2018). Brain and psychological determinants of placebo pill response in chronic pain patients. *Nature communications*,       9(1), 3397. ####

## Which tools do I want to learn? ##

* **Fmiprep**, as my pre-processing pipeline.

![fmriprep](https://pbs.twimg.com/media/Dbt_hXeVQAEZHTS.jpg)

* **Compute Canada (Beluga)**, as my computing platform

![ComputeCanada](https://www.ace-net.ca/wp-content/uploads/2018/03/Compute_Canada2.png)

* **Python**, as my programming language

![Python](https://content.techgig.com/thumb/msid-67886887,width-860,resizemode-4/How-Developers-use-Python-Programming-Language.jpg?50999)

* **Jupyter**, as my notebook for codes, visualizations and narratives.

![JupyterNotebook](https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/250px-Jupyter_logo.svg.png)

* **Nilearn**, for my neuroimaging analysis and brain parcellations.

![Nilearn](https://danilobzdok.de/wp-content/uploads/sites/521/ni-learn.jpg)

                  Schaeffer & Yeo, 2018. 400 Brain Parcellations derived within the 7 Network Modules
                  
![Schaeffer](https://pbs.twimg.com/media/Dz2u7WCU8AIxNJ4.jpg)

                  Power & Peterson, 2011. 264 Brain Parcellations; network modules can also be mapped.
                  
![Power](https://ars.els-cdn.com/content/image/1-s2.0-S0896627311007926-gr1.jpg)


* **Netneurotools**, for some of my functional connectivity analysis (tools from *Bratislav Mišić*), using PLS and *bootstrap ratios* as a cross-validation method.

![Netneurotools](https://avatars0.githubusercontent.com/u/31446908?s=400&v=4)



I will be associating the brain connectivity with classics questionnaires in clinical pain, descriptive of the severity:

* **McGill Pain Questionnaire (MPQ)**, assess the quality and intensity of pain.

![MPQ](https://ars.els-cdn.com/content/image/3-s2.0-B9781416058939002227-gr4.jpg)

* **Beck Depression Inventory (BDI)** to measure the severity of depression symptoms

![BDI-II](https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwj64KO7uYXkAhWuiOAKHdlfCxAQjRx6BAgBEAQ&url=https%3A%2F%2Fwww.pearsonassessments.com%2Fstore%2Fusassessments%2Fen%2FStore%2FProfessional-Assessments%2FPersonality-%2526-Biopsychosocial%2FBeck-Depression-Inventory-II%2Fp%2F100000159.html&psig=AOvVaw0xVutWVCupW3El7hmhMn2p&ust=1565978178385891)

* **Ecological Momentary Assessement**, to sample pain daily in real time, in subject's environment for 2 weeks.
    * Mean
    * Peak
    * Standard Deviation

![EMA](https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwiYyLXSuYXkAhVSU98KHQftAF4QjRx6BAgBEAQ&url=https%3A%2F%2Filumivu.com%2Fsolutions%2Fecological-momentary-assessment-app%2F&psig=AOvVaw2AyVledoIzTBriL7mW_5rQ&ust=1565978228121062)

## Which kind of deliverable do I want to implement: analysis, code, data, tutorial...? ##

- [x] [ **Code** ] Scripts to install and operate (*sbatch*) fmriprep on Compute Canada

- [ ] [ **Code & Analysis** ] Python script of my functional connectivity & cross-validation analysis

- [ ] [ **Data** ] Present my output data obtained from fmriprep

- [ ] [ **Notebook** ] Make the script on a Jupyter Notebook, with all the relevant explanations of the analysis.

- [ ] [ **Notebook & Analysis** ] Provide some vizualizations of my preliminary results from nilearn and netneurotools

## What kind of medium will I use to present my results? ##

#### A Jupyter Notebook presenting all my preliminary results, visualizations and explanations ####

#### A folder on my repository with a copy of all my scripts used in this project ####








