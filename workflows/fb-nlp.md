---
github_owner: "pegasus-isi"
github_repo: "https://github.com/pegasus-isi/pegasus-fb-nlp"
pegasus_version: ">= 5.0.0"
Topic: machine-learning, nlp
license: "No license available"
last_verified: "Nov 12, 2026"
image: "https://github.com/pegasus-isi/pegasus-fb-nlp/raw/master/img/fb-nlp.svg"
---

# Title : pegasus-fb-nlp

## Description
This workflow implements an example of the Facebook (Meta) NLP pipeline based on the "Unsupervised Machine Translation" research. It demonstrates how to automate complex natural language processing tasks, such as word-by-word initialization, language modeling, and back-translation, within a distributed computing environment.



## File Description
* **run.sh:** The primary entry-point script that automates the deployment and planning of the workflow.
* **workflow_generator.py:** Python script using the Pegasus API to generate the abstract workflow (DAX/YAML), defining the NLP processing steps and container dependencies.
* **input/mono:** Local directory for monolingual input archives (EN/FR). If missing, the workflow includes logic to download them from public WMT14 mirrors.
* **Dockerfile:** Used to build the `lpottier/fb-nlp:0.1` container which encapsulates the environment (Moses, fastBPE, fastText) required for the NLP tasks.

## How to run?
```bash
# Ensure you have an HTCondor pool and Pegasus installed.

# 1. Clone the repository
git clone [https://github.com/pegasus-isi/pegasus-fb-nlp.git](https://github.com/pegasus-isi/pegasus-fb-nlp.git)

# 2. Execute the run script
./run.sh
```

## THE WORKFLOW VISUALISATION