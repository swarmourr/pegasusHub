---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/orcasound-workflow"
pegasus_version: ">= 5.0.0"
Topic: machine learning
license: "No license available"
last_verified: "Dec 23, 2025"
image: "https://github.com/pegasus-isi/orcasound-workflow/raw/master//images/orcasound-workflow.png"
---

# Orcasound workflow

## Description
The Orcasound Workflow is a Pegasus-based pipeline designed to process and analyze hydrophone data from three locations in Washington state. It utilizes machine learning models to automatically detect and identify Orca calls and whistles from underwater audio recordings.

## File Description
* **workflow_generator.py:** Generates the abstract workflow (DAX) and defines the computational graph, including data dependencies for ML inference.
* **fetch_s3_catalog.py:** Catalogs audio data stored in Amazon S3 buckets to be used as input for the workflow.
* **Docker/Orca_Dockerfile:** Contains the environment setup for standard audio processing and data manipulation.
* **Docker/Orca_ML_Dockerfile:** Contains the deep learning environment (PyTorch, Pandas, NumPy) required for the Orca detection models.

## How to run?
```bash
# Generate the workflow
./workflow_generator.py

# Plan and submit the workflow
pegasus-plan --conf pegasus.properties --site condorpool --output-sites local --dir work --submit workflow.yml
```
## THE WORKFLOW VISUALISATION
