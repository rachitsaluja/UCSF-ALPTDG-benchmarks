# UCSF-ALPTDG-benchmarks
The official nnUNet benchmarks for The University of California San Francisco Adult Longitudinal Post-Treatment Diffuse Glioma (UCSF-ALPTDG) dataset.


## Requirements - 

Please install [nnUNetV1](https://github.com/MIC-DKFZ/nnUNet/tree/nnunetv1) in developer mode.

## Code - 

Please look at the notebooks folder to conduct your own experminets using nnUNetv1. Using that code you can also reproduce the same model files that we are sharing in this paper. The notebook helps to perform standard nnUNetv1 experiments on the dataset.

## Pre-trained Models -

All important models are available [here](https://drive.google.com/file/d/1oAjm4FPG8gSkjRl1cRD8zDtPhd0_x8JT/) for download. 

These are nnUNetv1 models that have been exported to zip files using the `nnUNet_export_model_to_zip` command. To use them, all you have run is `nnUNet_install_pretrained_model_from_zip`, and you will be able to run any of the models. 

We provide 3 models for the UCSF-ALPTDG dataset as benchmarks.
- **UCSF_PostTreatmentGliomaSegModel**: Model that takes inputs as (1) FLAIR (2) T1 (3) T2 and (4) T1CE MR images. `['flair','t1','t2','t1ce']`
- **UCSF_FLAIRChangeSegModel**: Model that takes input as the (1) FLAIR image in Timepoint 1 (2) FLAIR image in Timepoint 2 and (3) FLAIR subtraction image (t2-t1). `['time1_flair','time2_flair','flair_subtraction']`
- **UCSF_FLAIRChangeSegModel**: Model that takes input as the (1) T1CE image in Timepoint 1 (2) T1CE image in Timepoint 2 and (3) T1CE subtraction image (t2-t1). `['time1_t1ce','time2_t1ce','t1ce_subtraction']`

We also provide 2 skull stripping models for FLAIR and T1Post skullstripping respectively. 

Following are the performance metrics for all the experiments performed in this project. 

![Performance Metrics for nnUNet Segmentation Models](extras/benchmarks_performance.png)

## Usage - 

Data and models cannot be used for commerical use. 
