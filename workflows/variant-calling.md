---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/variant-calling-pegasus-workflow"
pegasus_version: ">= 5.0.2"
Topic: bioinformatics, genomics, workflow
license: "Apache License 2.0"
last_verified: "Nov 08, 2022"
image: "https://github.com/pegasus-isi/variant-calling-pegasus-workflow/raw/master/images/workflow.png"
---

# Title : variant-calling-pegasus-workflow

## Description
This workflow automates the "Variant Calling Workflow" from the Data Carpentry lesson "Data Wrangling and Processing for Genomics." It handles the process of identifying variants in genomic sequences, moving from raw sequence data to identified variants using standard bioinformatics tools.

## File Description
* **workflow_generator.py:** Python script that uses the Pegasus API to generate the abstract workflow (YAML), defining the data dependencies and bioinformatics tool execution steps.
* **data/:** Directory intended for raw sequence data (FASTQ files) and reference genomes.
* **scripts/:** Contains helper scripts for data processing or environment setup.
* **pegasus.properties:** Configuration file for the Pegasus engine, defining runtime parameters and data staging strategies.

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
