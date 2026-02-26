---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/sra-search-pegasus-workflow"
pegasus_version: "No version information available"
Topic: bioinformatics, genomics
license: "Apache License 2.0"
last_verified: "Feb 17, 2026"
image: ""
---

# Title : sra-search-pegasus-workflow

## Description
This workflow automates the retrieval and processing of genomic data from the Sequence Read Archive (SRA). It manages the downloading of raw reads, followed by alignment against a reference genome using a specialized toolstack. To ensure reproducibility and ease of deployment, all bioinformatics tools are encapsulated within an Apptainer/Singularity container.

## File Description
* **sra-search.py:** The primary workflow generator script. It takes a list of SRA identifiers and a reference genome to build the Pegasus abstract workflow.
* **container/sra.def:** The Apptainer definition file used to build the execution environment containing the SRA Toolkit, Samtools, and Bowtie2.
* **examples/:** Contains sample data including `sra_ids.txt` and reference sequences (`crassphage.fna`) for testing.
* **container/sra.sif:** The compiled Singularity Image File (built from the `.def` file) used during workflow execution.

## How to run?
```bash
# 1. Build the container (if sra.sif is not present)
cd container && apptainer build sra.sif sra.def
cd ..

# 2. Run the workflow generator with SRA IDs and a reference file
./sra-search.py --sra-id-list examples/10/sra_ids.txt --reference examples/10/crassphage.fna

# 3. The generator handles the internal pegasus-plan and submission
```
## THE WORKFLOW VISUALISATION