---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/1000genome-workflow"
pegasus_version: ">= 5.0.2"
Topic: bioinformatics
license: "Apache License 2.0"
last_verified: "Aug 25, 2025"
image: "https://github.com/pegasus-isi/1000genome-workflow/raw/master/docs/images/1000genome.png"
---

# Title : 1000genome-workflow

## Description
Bioinformatics workflow that identifies mutational overlaps using data from the 1000 genomes project. It fetches, parses, and analyzes Phase3 data by chromosome to provide a null distribution for statistical evaluation of potential disease-related mutations.

## File Description
* **daxgen.py:** Python script used to generate the abstract Pegasus workflow (DAX).
* **prepare_input.sh:** Script to unzip and prepare input data.
* **data.csv:** Configuration file listing the input data sources and chromosomes.
* **scripts/:** Contains the core analysis logic including individuals, populations, sifting, and mutation overlap tasks.

## How to run?
```bash
# Prepare input data
./prepare_input.sh

# Generate the workflow
./daxgen.py

# Plan and submit the workflow
pegasus-plan --conf pegasus.properties \
             --site local \
             --output-sites local \
             --dir work \
             --submit workflow.yml
```