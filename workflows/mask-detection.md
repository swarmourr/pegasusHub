---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/mask-detection-workflow"
pegasus_version: ">= 5.0.0"
Topic: machine-learning, optuna, pytorch-cnn, transfer-learning
license: "No license available"
last_verified: "Mar 08, 2022"
image: "https://raw.githubusercontent.com/pegasus-isi/mask-detection-workflow/refs/heads/master/imgs/wf_graph2.png"
---

# mask-detection-workflow

## Description
This workflow performs Mask Detection and Classification using a pre-trained FastRCNN model with PyTorch. It integrates Optuna for hyperparameter optimization and is designed to identify individuals wearing or not wearing face masks in images through transfer learning.

## File Description
* **workflow_generator.py:** Python script that utilizes the Pegasus API to generate the abstract workflow, defining the sequence of data preprocessing, model training, and evaluation.
* **train.py:** The core training script that implements the FastRCNN model and transfer learning logic using PyTorch.
* **optimize.py:** Implements hyperparameter tuning using the Optuna framework to find the best model parameters.
* **requirements.txt:** Lists all necessary Python packages, including PyTorch, torchvision, and Optuna.

## How to run?
```bash
# Generate the abstract workflow
python3 workflow_generator.py

# Plan and submit the workflow
pegasus-plan --conf pegasus.properties \
             --site local \
             --output-sites local \
             --dir work \
             --submit workflow.yml
```
## THE WORKFLOW VISUALISATION


