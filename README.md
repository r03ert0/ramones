ramones
=======

Scripts for Neuroimaging and Genetic data analysis

Introduction
============

This repository aims to share scripts for Neuroimaging and Genetic data analysis. The goal is twofolds:

- for *studies*: **version and share scripts** to **process** individidual ( **imaging and genetic** ) **data** 
  as well as scripts for group-wise statistical/machine learning analysis. 

- for *tools*: version and share "cookbook" and examples of scripts using neuroimaging/genetic tools.

Remarks
-------

- Scripts are not intend to work or compile for other. Just provide softwares/libraries dependances.


Global organization
===================

    studies/
      YYstudy/
        doc/
        data/
        scripts/

    tools/
      tool_name/
        doc/
        data/
        scripts/

Studies
-------

In the studies directory create a new directory acording to the study name example: 12ABIDE.

Example:
~~~~~~~~

  studies/
    12ABIDE/     # Study name prefixed by the year
      data/      # Provide some samples of the dataset (1 subject) organized as 
      scripts/   # Use sub-dirs with modality keyword "anat" "dti", type of processing "individual" "stat".
        01_unpack_and_organize_data.sh
        anat-individual/ # put a readme file briefly describing what processing is done here and software dependecies/version.
                         # prefix each script with a number that clarify application order. If you use an rst format, html will
                         # automatically generated to fill some web-based cookbook wiki.
          readme.[rst|txt]
          01_segmentation_with_spm.m
          02_segmentation_with_fsl.sh
          03_quality-control_spm-vs-fsl.py
          04_quality-control_plot_tissue-proportion-per-site.R
        dti/
          ...
      anat-stat_vbm-spm/
        01_normalize_spm_create-dartel-template.m
      ...
  doc/
  
  tools/
    anatomist
      doc/
      data/
    scripts/
