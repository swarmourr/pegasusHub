---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/montage-workflow-v3"
pegasus_version: ">= 5.0.0"
Topic: astronomy
license: "Apache License 2.0"
last_verified: "Aug 25, 2025"
image: "https://github.com/pegasus-isi/montage-workflow-v3/blob/master/docs/images/dax1.png?raw=true"
---

# Title : montage-workflow-v3

## Description
A new Python DAX generator version of the classic Montage workflow. This workflow uses the Montage toolkit to re-project, background correct and add astronomical images into custom mosaics.

## File Description
* **workflow_generator.py:** Creates the abstract Pegasus workflow using the Python API.
* **plan.sh:** Shell script used to plan and submit the workflow.
* **montage-setup.sh:** Script to handle the setup of the Montage environment.
* **data/:** Directory containing input astronomical datasets.

## How to run?
```bash
# Generate the abstract workflow
./workflow_generator.py

# Plan and submit the workflow
./plan.sh workflow.yml

```
## THE WORKFLOW VISUALISATION