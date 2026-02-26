---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/lung-instance-segmentation-workflow"
pegasus_version: ">= 5.0.0"
Topic: machine-learning
license: "No license available"
last_verified: "Aug 25, 2025"
image: "https://github.com/pegasus-isi/lung-instance-segmentation-workflow/blob/main/img/workflow.png?raw=true"
---

# Title : lung-instance-segmentation-workflow

## Description
Instance segmentation with U-Net/Mask R-CNN workflow using Keras & Ray Tune. This workflow uses Chest X-ray images for predicting lung masks, automating the process from dataset acquisition to model training and hyperparameter optimization.

## File Description
* **workflow.py:** The main Python script that utilizes the Pegasus API to generate the abstract workflow.
* **get-dataset.py:** A script to download the lung segmentation dataset from Kaggle or a backup location.
* **end-to-end.sh:** A shell script for executing the segmentation process in a standalone environment.
* **requirements.txt:** Lists all necessary Python dependencies (Keras, Ray Tune, etc.).

## How to run?
```bash
# Clone the repository
git clone https://github.com/pegasus-isi/lung-instance-segmentation-workflow.git

# Generate the workflow using sample data
python3 workflow.py --lung-img-dir inputs/train_images --lung-mask-img-dir inputs/train_masks

# Plan and submit the workflow
pegasus-plan --conf pegasus.properties --site local --output-sites local --dir work --submit workflow.yml
```