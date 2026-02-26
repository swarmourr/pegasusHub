---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/split-workflow"
title: "split-workflow"
subtitle: "Split workflow example"
pegasus_version: ">= 5.0.0"
license: "No license available"
topics: ["Training"]
date: "2025-10-27"
last_verified: "Oct 27, 2025"
image: "https://user-images.githubusercontent.com/36110304/212753610-843a44c9-9703-4dd1-9e50-86bd2a4deba7.png"
---

# Split Workflow

A fundamental Pegasus training workflow demonstrating how to split data into parallel tasks and manage distributed execution dependencies.

## Description

The Split Workflow example illustrates how a dataset can be partitioned into multiple independent chunks and processed concurrently within a Pegasus workflow.

It demonstrates:

- Parallel execution of independent tasks  
- Data partitioning techniques  
- Aggregation of distributed results  
- Basic workflow graph construction  

This workflow is commonly used for training purposes to help new users understand how Pegasus handles job dependencies and scalable execution.

## Workflow Structure

1. Input data is partitioned into smaller segments.
2. Each segment is processed independently in parallel.
3. Results are optionally merged or aggregated.
4. Final outputs are produced after all jobs complete.

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
