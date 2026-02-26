---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/compare-large-language-models-workflow"
pegasus_version: ">= 5.0.0"
Topic: machine learning
license: "No license available"
last_verified: "May 17, 2024"
image: ""
---

# Title : compare-large-language-models-workflow

## Description
This workflow is designed to benchmark and compare the performance of different Large Language Models (LLMs). It automates the process of sending queries to multiple models, collecting their responses, and evaluating them based on specific metrics to facilitate objective comparison.

## File Description
* **workflow_generator.py:** The main script that uses the Pegasus Python API to generate the abstract workflow, defining the models to be compared and the evaluation tasks.
* **compare_llms.py:** Core logic script that handles API calls to various LLM providers and aggregates the results.
* **evaluator.py:** Contains the metrics and logic used to evaluate and score the responses from the different models.
* **params.yml:** Configuration file where users can specify model names, API keys, and query parameters.

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