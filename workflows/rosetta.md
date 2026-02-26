---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/rosetta-pegasus"
pegasus_version: ">= 5.0.0"
Topic: protein-folding
license: "Apache License 2.0"
last_verified: "May 01, 2023"
image: ""
---

# Title : rosetta-pegasus

## Description
This is a Pegasus workflow for running Rosetta's De novo structure prediction on the OSG (Open Science Grid). The workflow predicts the 3-dimensional structure of a protein starting with an amino acid sequence, using the Abinitio Relax algorithm.

## File Description
* **workflow_generator.py:** The main script that generates the abstract Pegasus workflow (DAX/YAML), defining the parallel Rosetta jobs.
* **input_files/:** Contains necessary input data such as protein sequences and fragment files required by the Abinitio Relax algorithm.
* **bin/rosetta_scripts:** Wrappers or binaries used to execute the Rosetta suite within the grid environment.
* **pegasus.properties:** Configuration file for the Pegasus engine, tuned for OSG execution.

## How to run?
```bash
# Generate the workflow
python3 workflow_generator.py

# Plan and submit the workflow to the OSG or local pool
pegasus-plan --conf pegasus.properties \
             --site condorpool \
             --output-sites local \
             --dir work \
             --submit workflow.yml
 ```