---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/merge-workflow"
title: "merge-workflow"
subtitle: "Merge workflow example"
pegasus_version: ">= 5.0.0"
license: "No license available"
topics: ["Training"]
date: "2023-01-06"
last_verified: "Jan 06, 2023"
image: "https://user-images.githubusercontent.com/36110304/212752962-59adc85a-ab1d-481a-bf30-13791df85428.png"
---

# Merge Workflow

A Pegasus training workflow demonstrating how to merge and aggregate results from parallel tasks into a final output.

## Description

The Merge Workflow example illustrates how independent parallel jobs can produce intermediate outputs that are later combined into a single consolidated result.

This workflow demonstrates:

- Parallel task execution
- Data aggregation patterns
- Result merging strategies
- Workflow dependency management
- Final reduction stage after distributed computation

It is commonly used as a foundational training example for understanding how Pegasus manages many-to-one task relationships.

## Workflow Pattern

    1. Multiple independent jobs execute in parallel.
    2. Each job produces intermediate output files.
    3. A merge job collects outputs from all parallel tasks.
    4. The final result is generated after successful aggregation.

This pattern is essential in scientific workflows that require distributed computation followed by a reduction phase.

## How to Run

```bash
# Generate the workflow (if applicable)
./workflow_generator.py

# Plan and submit the workflow
pegasus-plan --conf pegasus.properties \
             --site condorpool \
             --output-sites local \
             --dir work \
             --submit workflow.yml
```
## THE WORKFLOW VISUALISATION

