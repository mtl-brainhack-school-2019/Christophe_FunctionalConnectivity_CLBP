How to download CairoSVG function (svg to pdf)

Fmriprep typically gave us an HTML file on to be able to assess quality control. However, since we don't have a browser, we cannotvisualize the HTML file on the cluster (nor the SVG). Here, we will convert the svg INSIDE the cluster. From there, we will be able to import these files as pdf.


To install the python package, you will need to do it on your virtual environment (see Repo 1. ..)
```pip3 install --user cairosvg```
#### Note that BOTH pip3** and --user** are essential for the command to run on the cluster. The package is only available in python>=3.5 and can not be download in compute canada bin, must be your own bin in home directory. ####

```
#!/bin/sh
cd /lustre03/project/6037352/tangsab8/CLBP_Network_Project/Placebo_1_Data_Copy/
fileNames=($(ls -d sub*))
shift
for isub in "${fileNames[@]}"
do
echo $isub
### Session loop
	for ises in ses-2 # list sessions
	do
	echo $ises
        for irun in run-1 # list runs
        do 
        echo $irun
        # Import .svg files in a new directory we will call FMRIPREP_FIGURES. Note that in the loop, we will be able to specify in our name the sub-#, ses-# and run-# in the names
        cp /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_OUTPUT/fmriprep/$isub/figures/*.svg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/
        cp /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_OUTPUT/fmriprep/$isub/$ises/figures/*.svg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/
        # Transform the .svg file in a pdf using the CairoSVG function. 
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_desc-reconall_T1w.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_desc-reconall_T1w.pdf
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_dseg.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_dseg.pdf
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_${ises}_task-rest_${irun}_desc-bbregister_bold.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_${ises}_task-rest_${irun}_desc-bbregister_bold.pdf
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_${ises}_task-rest_${irun}_desc-compcorvar_bold.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_${ises}_task-rest_${irun}_desc-compcorvar_bold.pdf
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_${ises}_task-rest_${irun}_desc-confoundcorr_bold.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_${ises}_task-rest_${irun}_desc-compcorvar_bold.pdf
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_${ises}_task-rest_${irun}_desc-rois_bold.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_${ises}_task-rest_${irun}_desc-rois_bold.pdf
        cairosvg /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/${isub}_space-MNI152NLin6Asym_T1w.svg -o /lustre03/project/6037352/tangsab8/CLBP_Network_Project/FMRIPREP_FIGURES/PDF/${isub}_space-MNI152NLin6Asym_T1w.svg.pdf
        done
    done
done
```

What is the result? Instead of copying the whole file for every subject for visual inspection, you will only have to load the pdf. For my sample size (~50 subjects), this is equivalent to having to download **0.380 GB** instead of **750GB** to inspect the data in html.

![IMAGE](https://github.com/mtl-brainhack-school-2019/Christophe_FunctionalConnectivity_CLBP/blob/master/Images/Screen%20Shot%202019-09-02%20at%209.24.39%20PM.png?raw=true)
