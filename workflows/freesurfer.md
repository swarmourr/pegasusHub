---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/freesurfer-osg-workflow"
pegasus_version: ">= 5.0.0"
Topic: brain-imaging, freesurfer
license: "No license available"
last_verified: "Apr 11, 2023"
image: "https://github.com/pegasus-isi/freesurfer-osg-workflow/raw/master/images/freesurfer-osg-workflow.png"
---

# Title : freesurfer-osg-workflow

## Description
A Pegasus workflow for running FreeSurfer's `recon-all` analysis on the Open Science Grid (OSG). FreeSurfer is a software suite for the analysis and visualization of structural and functional neuroimaging data from cross-sectional or longitudinal studies.

## File Description
* **workflow_generator.py:** Python script that uses the Pegasus API to generate the abstract workflow (DAX/YAML), mapping input MRI scans to FreeSurfer processing tasks.
* **recon-all.sh:** A wrapper script designed to set up the FreeSurfer environment on OSG worker nodes and execute the `recon-all` command.
* **inputs/:** Directory containing the input MRI data (typically in NIfTI or DICOM format).
* **pegasus.properties:** Configuration file for the Pegasus engine, optimized for data staging and job submission on the OSG.

## How to run?
```bash
# Generate the abstract workflow
python3 workflow_generator.py

# Plan and submit the workflow to the OSG
pegasus-plan --conf pegasus.properties \
             --site condorpool \
             --output-sites local \
             --dir work \
             --submit workflow.yml
```